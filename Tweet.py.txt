import re
import urllib.request as ur
from bs4 import BeautifulSoup as BS
from selenium import webdriver

#Gives User A variety of Options

print('#{:^24s}'.format("Welcome To Twitter Gif Scrapper#"))
print("########################################")
print("Please Select One of the Options Below:")
print("1) See All Available Image Links on Website" )
print("2) Download Files:(Zip)" )
print ("3) Exit")
print('\n')
x = input()

#driver = webdriver.Chrome()
#Parses Tweet
if x  == "1":
  
  url = input("Type in url")
  driver = webdriver.Chrome('/path/to/chromedriver')
  driver.get(url)
  html = driver.page_source
  for tag in soup.find_all("video"):
    print tag.text
  #downloads and prompt
if x == 2:
  url = input("Type in url")
  driver = webdriver.Chrome('/path/to/chromedriver')
  driver.get(url)
  html = driver.page_source
  
  for link in soup.find("videos"):
      
 
        #obtain filename by splitting url and getting last string
        file_name = link.split('/')[-1]   
 
        print("Downloading file:%s"%file_name)
 
        #create response object
        r = requests.get(link, stream = True)
 
        #download started
        with open(file_name, 'wb') as f:
            for chunk in r.iter_content(chunk_size = 1024*1024):
                if chunk:
                    f.write(chunk)
 
        print ("%s downloaded!\n"%file_name)
 
    print("Download Complete!")



  
    
 
   
  
   
   
   

