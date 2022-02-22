# ReviewSimilarity
Review ranking with the help of NLP , Text Mining and SOLR



Steps Of project :
1. Analsyis of the dataset .
2. Preprocessing of review text :
    -> Remove Stop words 
    -> Special char
    -> Remove Duplicate tokens 
    
 3. Read the data from CSV by using csv reader
 4. Insert the data into SOLR by using SOLRJ
 5. Algorithms uses :
 6.   Calculate the similarity 
 7.   Enabled LTR 
 8.   Boost the reiews basis of Rating , Pos feedback count , Recomand IND
 
 Index the data into SOLR .
 
 #Queries :
 
 #ALL documnent :
 http://localhost:8983/solr/reviews/mainselect1?q=*:*
 
 # Limit of documnet 
 http://localhost:8983/solr/reviews/mainselect1?q=*:*&rows=10
 here rows according to user_input 
 # Most positive 
 http://localhost:8983/solr/reviews/mainselect1?q=*:*&rows=10&fq={!frange%20l=50}field(pos_feedback_count,min)
 
 
