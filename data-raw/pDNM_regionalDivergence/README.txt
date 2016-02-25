A brief overview of the regional divergence adjustment:

    For a given transcript, the probability of mutation is adjusted to incorporate the                                 
    divergence score of that transcript. Divergence score is based on the number of                                    
    divergent sites between humans and macaques for ~1Mb on either side of the                                         
    transcript boundaries. The adjustment is currently:                                                                
    p_mut2 = p_mut1*(1 + (0.31898*div_score))                                                                          
                                                                                                                       
    For genes with no divergence score, the average divergence score is used.                                          
    That value is 0.0564635.                                                                                          
                                                                                                                       
    Additionally, this script adjusts all probabilities of mutation to account for the                                 
    fact that the divergence adjustment systematically raises all probabilities. In                                    
    this version, all probabilities are multiplied by 0.9822219.

Divergence scores are located in <divsites_gencodev19_all_transcripts.txt>
There should be a score for each coding transcript in GENCODE
"." denotes NAs.



