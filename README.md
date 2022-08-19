# CleanWhatsappText
## A Power Query custom function that cleans Whatsapp Chat data that has been exported as a text file

![CleanWhatsAppData](https://user-images.githubusercontent.com/107071538/185690043-c694349d-e9af-4858-a08b-1aab24ea325b.jpg)

## User Guide
### Preface
The Power Query custom function would help you clean WhatsApp Chats (Direct Chat or Group Chats) exported via the mobile app ([see here](https://faq.whatsapp.com/196737011380816/?helpref=uf_share)). The output of this export is a text file in a structure not suited for analysis. With this custom function you would be able to take that text data and transform it into a well formatted table for your analysis.
### Parameters
- TextFilePath - This is the file path of the exported chat on your PC.
- Message Separator - This is the character separating the actual message sent from the DateTime info from the Contact's Name. In the sample image above, this is an hypen (-).
- Contact Separator - This is the character separating the Contact's Name (Person) from the actual message sent. In the sample image above, this a colon (:).
- Date Format - This an option to select whether the date format in the exported file is "DD/MM/YYYY" or "MM/DD/YYYY". In the sample image above, this is "MM/DD/YYYY". This is option is neccessary because, based on feedback, the date format of the exported chats tends to differ by device type and region settings.
- Date Enclosed in [ ] - This a TRUE or FALSE option to specify whether the DateTime info from the exported chats are enclosed in sqaure brackets. This option is neccessary because, based on feedback, exports from iPhone devices seem to have the DateTime part enclosed in square brackets while export from Android devices do not. For example, the sample image above is based on an Android device. The iPhone export might be "[2/26/2021, 9:32 PM] David: Hey Man". 
In that iPhone sample, Message Separator would be a space ( ); Contact Separator would be a colon (:); Date Format would be MM/DD/YYYY; and Date Enclosed in [ ] would be TRUE.
### How to Use
Simply copy the code and paste in a blank query in the Power Query Editor
## Conclusion
This data cleaning step is a part of a WhatsApp Data Analysis project. Check that out [here](https://github.com/BolajiBI/WhatsAppPowerBIReport)
