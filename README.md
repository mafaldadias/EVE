In our recent article [Large-scale clinical interpretation of genetic variants using evolutionary data and deep learning](https://www.biorxiv.org/content/10.1101/2020.12.21.423785v1.abstract) we presented a deep learning model that trains on evolutionary data to predict the clinical significance of human variants. We make predictions for all single amino acid variants of 1,088 genes. These predictions come in the form of a score that ranges from 1, most pathogenic, to 0, least pathogenic or in other words most benign.

![Score Matrix](https://marks.hms.harvard.edu/disease_risk_prediction/SCN1B_HUMAN_singles_heatmap_full.png)
> Model score heatmap for SCN1B. The x-axis represents position along the protein, and the y axis all possible amino acid variants. 


You can download the 1,088 score heatmaps [here](https://marks.hms.harvard.edu/disease_risk_prediction/singles_heatmaps.zip). Receiver operating characteristic and precision-recall curves for these scores against clinical labels from [ClinVar](https://www.ncbi.nlm.nih.gov/clinvar/) can be found [here](https://marks.hms.harvard.edu/disease_risk_prediction/ROC_PRC.zip). After accounting for modelling uncertainty, we bin these scores into Benign, Pathogenic and Uncertain variants, and combine these predictions with orthogonal sources of evidence according to [ACMG-AMP guidelines](https://www.nature.com/articles/gim201530) in order to reclassify 72k variants of unknown significance. 

![Sankey](https://marks.hms.harvard.edu/disease_risk_prediction/flow.png)
> Classification, in terms of P: Pathogenic, LP: Likely Pathogenic, B: Benign, LB: Likely Benign and U: Uncertain, of human variants seen in the population according to ClinVar (left), to our model (middle) and to our model combined with orthogonal evidence following the ACMG-AMP criteria (right). 

Files per gene containing all variant model scores, as well as previously known labels from ClinVar, orthogonal sources of evidence, and final classification labels can be downloaded [here](variant_files.zip).

  
  
  
  
  
      

Project funded by:
![czi logo](https://marks.hms.harvard.edu/disease_risk_prediction/logos_website.jpg)
