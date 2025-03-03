# 10-475

# Entry Thurs Feb 8, 2024 
      # Lab meeting minutes: 
        # 1) redo metadata files and check and make sure all of them have (smoker status) 
        # 2) and if needed, convert some data types (e.g. if the smoking level is classified in numbers, convert it) 
        # 3) and give each data line a “source” file to cleanly say which study it came from 
        # 4) And finally combine the metadata files 
              # Try to do it on R, but if not, do it on Excel 
        # 5) Run the chime process for the data sets independently - don't trim them all the same. Trim them as you need to
              # ^if the datasets were all single/paired-end reads and their reads were the same length, you could treat them all the same from the import, but unlikely 
        # 6) Use the Qiime command to merge the data files 
        # 7) DataWrangling section on the proposal: describe how the metadata tables were consolidated 

        #entry Thurs Feb 15, 2024
        #Lab meeting agenda: 
        # 1) Talk about compiled metadata file 
        # 2) Task split
        # 3) Demultiplexing and Quiime
        # 4) Solidify research questions

        # Lab meeting minutes: 
        # 1) Went over compiled metadata files
        # 2) Discussed research question (add more detail)
        # 3) Examined sample sizes (400+ in total; EC 35; QC quite low, might need to be skipped)
        # 4) Suggested doing diversity matrix in R instead of Quiime, to factor in different sample types
        # 5) Outline of aimes for proposal (Due 25th Feb): 1. Metadata wrangling (replace all spaces on the sheet with underscores, simplify the column names); 2. Quiime 2 pipeline (analyze each file separately, merge at .qza, make alpha refraction curve) 3. Alpha and Beta diversity, all of the matrix, done in R. Use alpha and beta diversity to find confounding variables (e.g. locations of samples, location of city change to just country) 4. Do a coremicrobiome analysis 5. Do differential abundance analysis
        # 6) Meeting is optional next week
        # 7) Going through proposal outline
        
# Entry Thurs Feb 29, 2024
        #Lab meeting agenda: 
        # 1) Talk about proposal 
        # 2) Exact approaches to the research aims

        #Lab meeting minutes: 
        # 1) We come to the following conclusion:
        # 2)  This analysis answers the question of whether buccal swabs and saliva samples' microbiomes are sufficiently similar so that they can be treated as the same sample. Now let’s assume we CAN combine the buccal swaps and saliva samples, our next step is to assess the Shannon diversity and dominant species between NS and S for all 3 geographical locations. This analysis answers the question of whether the change in oral microbiota as a result of smoking and vaping is different across the sampled regions. We expect to see that the change in oral microbiota is consistent across the sampled regions, due to the applied stressor to the oral microbiome being the same from the behaviour of smoking and vaping regardless of the geographical location. If the change is similar, we can combine the data sets for a more comprehensive analysis of our objectives.
    

# Entry Thurs Mar 7, 2024
        #Lab meeting agenda: 
        # 1) Analysis plan 
        # 2) Examine proposal aim 1

        #Lab meeting minutes: 
      #/
      Aim 1
      * Metadata 
      * Qiime 
      Aim 2
      * Alpha diversity between buccal and saliva
      * Beta diversity between buccal and saliva
                * Taxonomic bar plots
      * Do in R and isolate based on cohort 
      * Effect of sampling location 
      Aim 3
      * Look at Alpha diversity between all 3 NS
      * Look at Alpha diversity between all 3 S
      * Look at Alpha diversity between all 2 V
      * Look at dominant species between all 3 NS
                * Taxonomic bar plots
      * Look at dominant species between all 3 S
                * Taxonomic bar plots
      * Look at dominant species between all 2 V
                * Taxonomic bar plots
      * Effect of geography 
      Aim 4
      * Compare Shannon between NS and S within all 3 cohorts 
      * Compare dominant species between NS and S within all 3 cohorts 
                * Taxonomic bar plots
      * Compare Shannon between NS and V within all 2 cohorts 
      * Compare dominant species between NS and V within all 2 cohorts 
                * Taxonomic bar plots
      * Do in R 
      * Looking at delta between NS and S in all cohorts, and comparing 
      * Effect of smoking or vaping
      -------
        # Also Ran american and uk core alpha diversity measures (evenness and faith-ph) 
        # Also Decided not to combine buccal and saliva for both america and uk cohorts

 # Entry Thurs Mar 14, 2024
        #Lab meeting agenda: 
        # 1) R phyloseq script troubleshoot 

        #Lab meeting minutes: 
        # 1) R phyloseq script troubleshoot
        # 2) Fixing TAX table 
        # 3) Plan to filter phyloseq
        # 4) Plan to make bar graph for the taxonomic composition of each cohort colored by phylum

 # Entry Thurs Mar 21, 2024
        #Lab meeting agenda: 
        # 1) Discuss alpha and beta diversity graphs of each dataset separately 

        #Lab meeting minutes: 
        # 1) Examine the alpha and beta diversity of each dataset
        # 2) Examine the compiled PCoA plot of merged dataset
        # 3) Plan to modify the PCoA plots (shape by other variables, color by smoking status)
        # 4) Make PCoA plot of the merged dataset by coloring by location, using a lower alpha value
        # 5) Plan to make PCoA plots for each datasets in general
        # 6) Discuss plan moving forward: 
              make rarefication parameters the same for all datasets, pick a number regardless of the Chinese dataset. 
              it is ok to delete chinese dataset --> requires justification, e.g. low sampling depth 
              only look at saliva samples for all analysis
              remake all R to make all the alpha and beta diversities with significance with Wilcoxon/Mann-Whitney test or Kruskall-wallis test
              is there significant alpha diversities within each cohort (saliva, smoking status)
              beta diversities for america and uk datasets 
              PCoA plot for each dataset distinguishing smoking status with significance with PERMANOVA 
              core-microbiome and indicator species with non-rarefied phyloseq object 

# Entry Thurs Mar 28, 2024
        #Lab meeting agenda: 
        # 1) Discuss alpha and beta diversity graphs of each dataset 
        # 2) Discuss indicator species and core microbiome analysis

        #Lab meeting minutes: 
        # 1) Focus on American as it had significant difference between EC and C and all 3 smoking status
        # 2) Redo venn diagram 
        # 3) Why is smoking not doing much to alpha diversity
        # 4) Do differential abundance 
        # 5) Comparing the C and NS of the other dataset too
        # 6) By next week meeting have the figure done
        # 7) Discuss the figure plan (JUST ONE DATASET):
        figure 1: alpha observed shannon and faith as 3 panels and stats 
        figure 2: 3 way venn diagram 
        figure 3: taxa bar plot 
        figure 4: DESeq: 4 panels one volcano S vs NS, corresponding bar plot, EC vs NS volcano, corresponding bar plot 
        figure 5: PiCrust: 2 panels: C vs NS, V vs NS bar plots.
        table 1: indicator taxa, only keep the 2 unique to each taxa 

        figure s1: beta diversity of the 3 status cohort 
        
# Entry Thurs Apr 4, 2024
        #Lab meeting agenda: 
        # 1) Discuss figures  
        # 2) Plans for presentation and manuscript

        #Lab meeting minutes: 
        # 1) Examine existing figure 1 and 2 
        # 2) For the lack of difference in alpha diversity, there might still be other differences. The current figure 1 did not account for any confounding variables
        # 3) PiCrust no significant/known pathways implicated but enough -> key points there is a difference. 
        # 4) Figure 2: more shared species between C and EC -> good
        # 5) Have the ppt ready by next Monday meeting
        # 6) Discuss the figure plan (JUST ONE DATASET):
        Same plan
        figure 3 taxa bar plot of each smoking status, phylum (usually easier) or family
        figure s2: PiCrust heat map potentially
         
             
