# SIEM - Splunk
> SIEM tools such as Splunk are important for a security analyst's toolbox as they provide a platform for storing, analyzing, and reporting on data from different sources.

## Scenario
You are a security analyst working at the e-commerce store Buttercup Games. You've been tasked with identifying whether there are any possible security issues with the mail server. To do so, you must explore any failed SSH logins for the root account.  

The following are the details of the data in a zipped file which you will upload it into Splunk: 
* `mailsv` - Buttercup Games' mail server. Examine events generated from this host.
* `www1` - This is one of Buttercup Games' web applications.
* `www2` - This is one of Buttercup Games' web applications.
* `www3` - This is one of Buttercup Games' web applications.

vendor_sales - Information about Buttercup Games' retail sales.
## Expectation
* Upload sample log data
* Search through indexed data
* Evaluate search results
* Identify different data sources
* Locate failed SSH login(s) for the root account

## Step-by-step
1. Login/signup to Splunk.
2. Add Data on the Splunk bar. 
3. Upload data into Splunk.
4. Select file and upload `tutorialdata.zip`. Please visit this [link](https://drive.google.com/file/d/1nDz_DZB4ADbD4tvaDa54_l1FoT_jtVy4/view) for more information.

<img width="1440" alt="Screenshot 2025-03-27 at 10 03 06 PM" src="https://github.com/user-attachments/assets/5e08b6df-38e3-4c4a-880a-f0820857d6bd" />

5. Navigate to Search and Reporting tab, type on the search bar index=main to view repository for data and select All time to view all the events across all time.
> Notice that there are more than 100,000 events
   <img width="1421" alt="Screenshot 2025-03-27 at 10 11 49 PM" src="https://github.com/user-attachments/assets/6eb40e54-3fe4-4c9b-ba6b-4c08271d0316" />

6. Evaluate the fields `host`, `source`, and `sourcetype`

* `host`: Specifies the name of the network host from which the event originated.
  
   <img width="1422" alt="Screenshot 2025-03-27 at 10 24 42 PM" src="https://github.com/user-attachments/assets/a4443d2b-db3a-41cf-a507-1b39afb11863" />

* `source`: This field indicates the file name from which the event originates

  <img width="1422" alt="Screenshot 2025-03-27 at 10 30 50 PM" src="https://github.com/user-attachments/assets/a835cbc7-a19a-4df6-a258-52b611bea290" />

* `sourcetype`: Sourcetype determines how data is formatted

  <img width="1423" alt="Screenshot 2025-03-27 at 10 32 45 PM" src="https://github.com/user-attachments/assets/b95fcea9-43da-453e-97ec-ae46da2c0421" />

7. Lets narrow the search results by looking for the host `mailsv`
> Notice the search results narrowed from over 100,000 to under 10,000
   <img width="1427" alt="Screenshot 2025-03-27 at 10 44 50 PM" src="https://github.com/user-attachments/assets/35e8e607-7d4c-4603-9777-624e38bf7f9e" />

8. Finally, we'll search for any failed SSH logins for the root account

   <img width="1422" alt="Screenshot 2025-03-27 at 10 55 41 PM" src="https://github.com/user-attachments/assets/5466d963-87d1-4d89-b0c4-bda368217817" />

## Summary
* There were over 100,000 events contained in the main index across all time
* The `host` specifies the name of the host, such as a network device, that an event originates from
* The `vendor_sales` host provides information about Buttercup Games' retail sales, such as the number of products sold.
* There are over 100 failed SSH logins for the root account on the mail server.




