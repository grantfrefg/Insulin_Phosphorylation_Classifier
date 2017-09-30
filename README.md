# Insulin_Phosphorylation_Classifier
Positive Unlabelled Classification


######The main aim of the project is measure a body's fat cell's sensitivity to insulin. Insulin is used in the body to activate a cell's ability to absorb sugar from the blood. When you have diabetes, you're insulin resistant. That means your body requires more insulin to be produced by the pancreas (or by injection) in order to absorb the same amount of sugar. The sensitivy of the cell to insulin is measured by the phosphorylation, more phosphorylaiton, more sensitive.

######Phosphorylation is the transfer of energy, ATP - Adenonosine TRI PHOSPHATE is the unit of energy, Phosphory-lation is the cutting of this bond, this releases energy. This will happen at a specific binding point on the protein. It is the result of the binding process. We are measuring how much and how fast of the phosphrylation is happening.

######The identifier is split into 2 parts, and is separated via a semi-colon. The first part is the protein or the gene. The second part is the binding site on the gene where phosphorylation occurs.

######A kinase is the enzyme in the reaction between the fat cell protein and insulin. Enzymes act by lowering the energy needed for reactions to occur. So these cells can either be phosphorylated by two kinases AKT and mTOR. It is our job to predict which kinase is phosphorylating which cell/site.

######Substrates, are the points at which a particular kinase binds i.e their potential matches. So we are given some labels that are AKT Substrates, in our project, these will be the positive labels. We are assuming that the phosphorylation rate is heavily dependant on the kinase, whether it be AKT or mTOR.

######The higher the AUC, the higher the response. Each time-point is an indication of where the majority of the reaction occurs. The higher the AUC, you'd expect that the reaction is fast and then plateaus.

######No Insulin is 0 time point, and then a measure of 15, 30 etc. log2 of the number vs time 0? Not too sure what he was saying.

######The second column is the amino acid sequences, proteins are made up of a sequence of amino acids, the order is very important as it determines how they fold. So given that enzyme is kind of like a key that goes into a lock (the substrate (the binding site)), keys can't really change shape/size so the amino acid sequence will likely be similar.

######The phosphorylation site is likely to be in the middle of the amino acid chain, we also factor in the next 6 amino acids to the left and the right. When you see an example of an underscore, it is because the protein chain has ended. In which case, each underscore is just saying there are 2 amino acids to the right then 4 blanks (underscores). A good example of this are rows 3656-7 so DP1 (the cell) 188 (the binding site) has a mid point of 'S', i.e 6 amino acids to the left. Then on the right it has a T and 5 underscores. Then the row below has the same cell but one amino acid over, we knew that the amino acid to the right was a T, now it is the end and we expect 6 underscores to the right.

######AKT is upstream and mTOR is downstream and therefore won't crossover.
