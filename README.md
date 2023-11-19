# E-Commerce Project SETUP:


This guide is segregated into 3 main parts. 
1. The first part of the guide talks about installing the MySQL database, MySQL WB and finally running the SQL scripts required for the e-commerce project. 
2. The second part talks about running the Spring Boot E-Commerce App.
3. The third part talks about running the Angular Frontend E-Commerce App.

**Running MySQL Server:**
1. Download the source code attached to lecture 217 and extract the directory from the zip.
2. Open 01-starter-files directory. Let's run the scripts under the `01-starter-files/db-scripts` directory. To run those scripts and look at the results later, you have to install a MySQL client on your machine. So, We will install MySQL Workbench.
3. Install [choco](https://chocolatey.org/install). choco is a prominent package manager for Windows. Note: Please make sure you open Windows PowerShell as Administrator for all software installations.
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/7c65396a-2c23-4bc7-88bb-9dc4b9259196"/>
4.  Download MySQL community server from power shell using  `choco install mysql`. Note: While installing the software with choco, accept to run all scripts by giving `A`.
    <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/e21b4be6-4cb9-4c51-b931-b4a2c6365a74"/>
5. You can start MySQL as follows: hit  `windows key + R`   
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/5c7fa0bd-0dcd-413a-b5ef-736703c04768"/>
   
7. Once you're in `Services`, find `MySQL` and start it.
   
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/f2ec4ea4-ca6d-485e-94ac-9c1fa0ec8dca"/>
   
9.  Now, in order to run those starter SQL scripts under `01-starter-files/db-scripts` , let's install MySQL Workbench.  Download MySQL Workbench using `choco install mysql.workbench`. You should see MySQL WB on start in Windows. Now, to run all the scripts, open all the SQL scripts one-by-one and run execute them by clickingon the ⚡️.

    <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/7d27efaf-d7e4-4cd1-9d8e-48b92b83faca"/>
    
    <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/d17fcad1-2a77-40c8-93d2-3661a8a7ba27"/>


**Running the Spring Boot App:**
1. Install JDK on your machine from the power shell using `choco install zulu11`. Open your cmd prompt, and do `java --version` which should give you the java version.
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/1870473f-cbbb-4dea-a1b4-e4beb79cce68"/>
2. Set JAVA_HOME (as Administrator) from cmd. `setx -m JAVA_HOME "C:\Program Files\Zulu\zulu-11"`. If you've installed Java using choco, it should be installed in the above-specified path. If not, make sure you have the right path to the JDK. To check if you've set the path right, run `refreshenv` in the same cmd prompt and then run `echo %JAVA_HOME%` gives you the path you've just set.
3. Now, `cd` into `02-backend/spring-boot-ecommerce`. Now, run `mvnw clean install`. This might take a couple of minutes.
4. Once everything goes well in step 3, to start your application run `mvnw spring-boot:run`. This will run your backend application. Once your application is up, go hit `http://localhost:8080/api/` on your browser and you should see something as follows: (Note: Make sure your mysql server is up)
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/e1d6e894-866e-4dee-bb3c-fb38529cc9a4" />

**Running the Angular App:**
1.  Install node on your machine using choco. `choco install nodejs-lts` . This will install install nodejs v16 (lts). **NOTE please install nodejs v16. This project is made using nodejs v16 and doesn't support latest nodejs versions.**
2. Running `node -v` && `npm -v` from cmd should give you their respective version numbers.
3. **IMP: To install angular. Install the angular version supported by nodejs v16. Try angular-cli 16.1.0 `npm i @angular/cli@16.2.6`**
4. Install the angular-cli globally from the cmd prompt by running:  `npm install -g @angular/cli`. `ng version` should give you angular-cli version number.
5. Now, navigate to our front-end app at `03-frontend/angular-ecommerce`. Once you're inside the `angular-ecommerce` directory, run `npm install`.
6. Now, run `ng build`  (this might take a couple of minutes) and then `ng serve`.
7. You should have the front-end e-commerce app up and running at `http://localhost:4200`. 
With that, you should have a fully functional E-Commerce App running on your machine.
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/2727dae3-137c-44a3-850d-43eff3ad3112"/>
