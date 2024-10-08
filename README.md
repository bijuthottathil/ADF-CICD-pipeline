# ADF-CICD-pipeline

![image](https://github.com/user-attachments/assets/ba19f481-c12b-4f93-a4fe-742e8b45a3d0)


Created Organization in Azure Devops
![image](https://github.com/user-attachments/assets/93905ec3-f669-4f83-a53b-e591e6c8f5dd)

Organization settings- connect to default Azure directory
![image](https://github.com/user-attachments/assets/6c47406f-4924-4539-b722-87fe5319506f)

Created new project and repo main
![image](https://github.com/user-attachments/assets/7078bf63-2af1-4945-98ba-e23d2898282f)

Connect to Azure--> Azure Data Factory-- Load ADF Studio--> From git configuration--> connect to Azure Devops Organization and Repo
![image](https://github.com/user-attachments/assets/432e559b-a2f9-40e6-bfdc-16546de2de13)

![image](https://github.com/user-attachments/assets/dd3b06d2-44d0-40d1-9121-92601ba1db3a) ![image](https://github.com/user-attachments/assets/30fb3e79-b4c9-4dc9-8223-71af3adf23bb)

creating adf pipeline to copy arrayed json file to flatten and store it in adls storage account ![image](https://github.com/user-attachments/assets/f105a5bf-3cfc-43bc-b553-5f42e4da528f)


![image](https://github.com/user-attachments/assets/18a4b87a-7a07-409d-9560-be41a18e6124)

Dataflow is created 

![image](https://github.com/user-attachments/assets/888d28a8-b05b-4a57-b71f-6ce8f8c85f06)

New pipeline ready to execute

![image](https://github.com/user-attachments/assets/a328a0e0-0b03-4a4d-b549-968516ad6081)

Trigger in place
![image](https://github.com/user-attachments/assets/97388e94-25d6-4bf5-9225-e778930af44f)

Job executed successfully
![image](https://github.com/user-attachments/assets/627e8f38-b510-420a-9580-8cdcec32f2dc)



csv file is generated in adls storage
![image](https://github.com/user-attachments/assets/55040b30-ec6b-4c1c-9792-7e365ad0af51)

![image](https://github.com/user-attachments/assets/b027e702-f676-4f72-b5bb-b0982ed2246d)

Now will checkin these changes to main branch



![image](https://github.com/user-attachments/assets/2c557255-7937-4005-9d39-1ca6cf5a2f03)

After approval

![image](https://github.com/user-attachments/assets/8c0e8f53-f9a1-4684-a7ee-9c88e5bf3a2c)

After merging ADF allowed to publish changes to run pipeline

![image](https://github.com/user-attachments/assets/041bb9c9-b59f-47bd-99f9-7dc389407b9f)

Executed pipeline again. you can see successful pipeline run and result

![image](https://github.com/user-attachments/assets/10ca3dc2-016c-4d29-8e7e-f7db7238be59)

![image](https://github.com/user-attachments/assets/1229eee2-1638-4ce9-8060-7e0e4d05766d)


Azure Devops repository will looks like below

![image](https://github.com/user-attachments/assets/874ea144-fa91-40d8-9660-f7c371657068)

additionally Azure Devops will create additional repository with ARM Templates

![image](https://github.com/user-attachments/assets/fbc5d528-e5d3-42d3-8f13-6408572970ac)


Next we will focus on creating release pipeline in Azure Devops to push code to Test environment. Make sure to disable below options from organization settings ![image](https://github.com/user-attachments/assets/e6a90637-14e1-4ea9-8754-01af849de131)

select Releases-- Pipeline

![image](https://github.com/user-attachments/assets/095bbd98-f127-42be-87a6-fd9fe2d74866)

![image](https://github.com/user-attachments/assets/1bc7d5ff-491d-4245-ae56-c0cc0b5d5105)
Adding artifacts- it means source. our source is ARM template
![image](https://github.com/user-attachments/assets/52a97c9b-7690-4c99-a2c0-052dc03fed9c)

Adding stages
![image](https://github.com/user-attachments/assets/2d231518-2bd4-4004-af38-64027206efdd)
![image](https://github.com/user-attachments/assets/4940d464-8f25-4f40-a414-a513515e96aa)

Adding settings for stages
![image](https://github.com/user-attachments/assets/7014d99b-f619-4c3e-8be2-ff185c333cdb)

![image](https://github.com/user-attachments/assets/7ca9c258-2548-4556-b93c-4dfd99f5e200)

![image](https://github.com/user-attachments/assets/7339f479-baa2-4742-8648-6fee89edf280)

For deployment, click trigger from Artifacts and update trigger details like below

![image](https://github.com/user-attachments/assets/11fecdcb-3935-44e9-ad87-057c4ba66530)

Testing relase manually from Azure Devops for testing

![image](https://github.com/user-attachments/assets/78ec180d-3148-467c-957e-3f5cf98ffab3)

I got error, because parallism was not enabled. For that we need to submit request to microsoft using  this link and provide organization url https://forms.office.com/pages/responsepage.aspx?id=v4j5cvGGr0GRqy180BHbR5zsR558741CrNi6q8iTpANURUhKMVA3WE4wMFhHRExTVlpET1BEMlZSTCQlQCN0PWcu&route=shorturl

![image](https://github.com/user-attachments/assets/379c53f8-80bc-4fb8-9803-96a58a199660)

Microsoft approved my request
Take a look on  build

Create Release from below. Or do a change in the pipeline and publish 

![image](https://github.com/user-attachments/assets/68faf935-52df-4648-935a-0a4b73925e8c)


Before release. no pipeline will be available in test env adf

Release started

![image](https://github.com/user-attachments/assets/1f65d404-91d6-48cf-b2ba-9c33875bb66c)

![image](https://github.com/user-attachments/assets/2d598e25-5725-4de1-ad97-582acdd092e2)

![image](https://github.com/user-attachments/assets/5e675fcb-e119-492b-b6c5-37cea58a25f4)
![image](https://github.com/user-attachments/assets/6524546e-191e-4796-ab27-0cfe71c69a3b)

![image](https://github.com/user-attachments/assets/3c311177-feb3-4f2f-8a85-8c48ab3200a5)

Build and deployment is successfule

All pipelines in Dev environment is deployed to Test environment now

![image](https://github.com/user-attachments/assets/2324792a-1f24-40c7-9ffd-007edb47065c)









