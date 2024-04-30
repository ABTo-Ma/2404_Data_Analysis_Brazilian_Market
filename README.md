# 2404_Data_Analysis_Brazilian_Market
As part of a learning exercise at WBS-Coding School, a fictitious case study was created. An online marketplace specializing in high-end technology products based in Spain is considering entering the Brazilian market. For this purpose, a partnership with a Brazilian company is under consideration.
Using data analysis, a decision has to be made about the potential partnership. The results will be presented in a business presentation.
## About the project: resources, tools and colaboratores
# Resources: 
Database provided by the Brazilian company
# Tools:
MySQLWorkbench with SQL-Language and Tableau
# Colaboratores:
Teams of 3 people
# Time span:
32 hours
## About the project: Challenges  
The extensive amount of provided data went uncommented, uncorrected, and unfiltered. There was no opportunity to query the dataset provider. Additionally, entries may be in a foreign language.
Mastering the analysis would require good teamwork.
To accurately identify key aspects for decision-making within realistic financial expectations, conducting research in the Brazilian market was crucial.
The insights gained from the analysis had to be condensed into a 5-minute business presentation.
## About the project: Result
A successful analysis of the given data was conducted. Clear recommendations for business decisions, as well as future insights, were provided. Good teamwork was facilitated through communication and clear division of tasks. Expectations were met.
## Examples
# Filtered SQL-Queries were implemented for substracting the key data:
```
/* Total amount earned by Tech sellers */
SELECT
    ROUND(
			(SELECT
				SUM(i.price) 
                FROM
					order_items i
				JOIN
					products p
				USING (product_id)
                JOIN
					product_category_name_translation t
				USING (product_category_name)
                WHERE t.product_category_name_english IN
                ('audio','consoles_games','electronics','computers_accessories'
					,'computers','signaling_and_security','tablets_printing_image',
					'telephony')),2
    ) AS 'Earnings for sellers in Tech in the whole data set [€]';
```  
# Langauge challenges were also tasked by implementing special queries or understanding the organizational system in the database.
# For visualization, graphs were made with condensed information
<img width="586" alt="Screenshot 2024-04-30 at 16 54 33" src="https://github.com/ABTo-Ma/Analysis.Visualization_Brazilian_Market/assets/168551372/69e1ad74-48a4-4bbc-bb57-04d1eafdd8bd">
