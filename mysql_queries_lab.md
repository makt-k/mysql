1. find the average CTR for zn_count > 20

	**select avg(ctr) from example where zn_count > 20;**

	0.5635162990311582

2. find the distributions of queries for each form_name

	**select form_name, count(*) from example group by form_name; **

3. find the average ctr for queries with 1, 2, 3, 4 words.

	**select avg(ctr) from example where length(iv_submitted_keyword) - length(REPLACE(iv_submitted_keyword, ' ',''))+1 = 1;**
	
	1 word =  0.5793985537438217 

 	**select avg(ctr) from example where length(iv_submitted_keyword) - length(REPLACE(iv_submitted_keyword, ' ',''))+1 = 2;**
 	
	2 words = 0.5793814279832865

	**select * from example where length(iv_submitted_keyword) - length(REPLACE(iv_submitted_keyword, ' ',''))+1 = 3;**
		
	3 words = 0.5824381961782129

	**select avg(ctr) from example where length(iv_submitted_keyword) - length(REPLACE(iv_submitted_keyword, ' ',''))+1 = 4;**

	4 words =  0.584951936384523