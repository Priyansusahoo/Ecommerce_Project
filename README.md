# E-Commerce Project SETUP:


This guide is segregated into 3 main parts. 
1. The first part of the guide talks about installing the MySQL database, MySQL WB and finally running the SQL scripts required for the e-commerce project. 
2. The second part talks about running the Spring Boot E-Commerce App.
3. The third part talks about running the Angular Frontend E-Commerce App.

**Running MySQL Server:**
1. Download the source code attached to lecture 217 and extract the directory from the zip.
2. Open 01-starter-files directory. Let's run the scripts under the `01-starter-files/db-scripts` directory. To run those scripts and look at the results later, you have to install a MySQL client on your machine. So, We will install MySQL Workbench.
3. Install [choco](https://chocolatey.org/install). choco is a prominent package manager for Windows. Note: Please make sure you open Windows PowerShell as Administrator for all software installations.
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/ce2eec5c-0936-4e86-8f23-1c3296fa568e"/>
4.  Download MySQL community server from power shell using  `choco install mysql`. Note: While installing the software with choco, accept to run all scripts by giving `A`.
    <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/3dcfb1e7-6458-4ed0-b737-a5c3d462db4a"/>
5. You can start MySQL as follows: hit  `windows key + R`   
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/64cc5d45-628e-4b6d-b071-0f975587e9cb"/>
   
7. Once you're in `Services`, find `MySQL` and start it.
   
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/f6a1dba7-9983-463e-8994-e3066377135b"/>
   
9.  Now, in order to run those starter SQL scripts under `01-starter-files/db-scripts` , let's install MySQL Workbench.  Download MySQL Workbench using `choco install mysql.workbench`. You should see MySQL WB on start in Windows. Now, to run all the scripts, open all the SQL scripts one-by-one and run execute them by clickingon the ⚡️.

    <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/3f5aa2ba-82aa-40f4-99f9-2a54cce49ab4"/>
    
    <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/2d303c80-c1cd-4588-8d13-32768619a220"/>


**Running the Spring Boot App:**
1. Install JDK on your machine from the power shell using `choco install zulu11`. Open your cmd prompt, and do `java --version` which should give you the java version.
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/56d79b59-cb38-4884-b656-0dfd49afcc6b"/>
2. Set JAVA_HOME (as Administrator) from cmd. `setx -m JAVA_HOME "C:\Program Files\Zulu\zulu-11"`. If you've installed Java using choco, it should be installed in the above-specified path. If not, make sure you have the right path to the JDK. To check if you've set the path right, run `refreshenv` in the same cmd prompt and then run `echo %JAVA_HOME%` gives you the path you've just set.
3. Now, `cd` into `02-backend/spring-boot-ecommerce`. Now, run `mvnw clean install`. This might take a couple of minutes.
4. Once everything goes well in step 3, to start your application run `mvnw spring-boot:run`. This will run your backend application. Once your application is up, go hit `http://localhost:8080/api/` on your browser and you should see something as follows: (Note: Make sure your mysql server is up)
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/0bcab7ed-fd36-48d9-ab8f-a88dedb1f9fe" />

**Running the Angular App:**
1.  Install node on your machine using choco. `choco install nodejs-lts` . This will install install nodejs v16 (lts). **NOTE please install nodejs v16. This project is made using nodejs v16 and doesn't support latest nodejs versions.**
2. Running `node -v` && `npm -v` from cmd should give you their respective version numbers.
3. **IMP: To install angular. Install the angular version supported by nodejs v16. Try angular-cli 16.1.0 `npm install -g @angular/cli@16.2.6`**
4. Install the angular-cli globally from the cmd prompt by running:  `npm install -g @angular/cli`. `ng version` should give you angular-cli version number.
5. Now, navigate to our front-end app at `03-frontend/angular-ecommerce`. Once you're inside the `angular-ecommerce` directory, run `npm install`.
6. Now, run `ng build`  (this might take a couple of minutes) and then `ng serve`.
7. You should have the front-end e-commerce app up and running at `http://localhost:4200`. 
With that, you should have a fully functional E-Commerce App running on your machine.
   <img src="https://github.com/Priyansusahoo/Ecommerce_Project/assets/78722016/5e2aed54-48a1-4c42-8887-73d3482ad7ed"/>
