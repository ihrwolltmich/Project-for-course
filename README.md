# The aim of the project is to see if obesity is linked to happiness. 
The first step i have taken is to download the global happiness report  as csv  
hs=pd.read_csv(r"C:\OD\OneDrive - Enel Spa\Keypass\Downloads\world-happiness-report-2019.csv")
# My next step is to identify the top 20 and bottom 20 countries. Fortunatly, the dataframe was already sorted from top to bottom. 
top_20=hs.head(20)
print(top_20)
bottom_20=hs.tail(20)
print(bottom_20)
#Now for my second data fram i want to check out the obesity rate for different countries. The file that i could find however contains data from 1976 to 2016. 
#However i want to focus on 2016 only. 
#If i look at the original file, it has various headers with 2016. As i only want to focus on the combined number i renamed the headers. 
#Can i do that? 
#To see the results for that particular collum only i do the following 
obs2016mf=obesity['2016mf']
print(obs2016mf)
#That shows me the collum but now i got the following issue, the countries are sorted alphabetically, so i cannot use the head function, the sort funciton is causing
#similiar problems it just sorts it by alphabet not by number 
obs2016mf=obesity['2016mf']
print(obs2016mf)
print(obs2016mf.sort_values())
# My main issue is, how can i make sure that i get the top 20 and the bottom 20 countries? 
#Another issue is that the the collum i want to view contains a lot of uncessary information. I just want to see the total value not the value in brakets. 
#How can i clean this and other entries that are invalid? ( countries that have no data or cells that are empty)? roject-for-course
