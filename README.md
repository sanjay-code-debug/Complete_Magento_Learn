# Complete_Magento_Learn
All core details of Magento only for Quick Understading


Concept
=======

Service Contract
----------------
![Service_contract](https://user-images.githubusercontent.com/78407424/170829619-146e2aa8-2507-4f36-bfaa-718794394412.png)


- Avoid use of Deprecated Method

Proxies(Proxy Class)
--------------------
![Screenshot from 2022-05-18 10-11-56](https://user-images.githubusercontent.com/78407424/168958702-ba6a1bfc-3b9f-460f-9209-383d8542991d.png)

- di.xml is having higher priority rather than constructor 

Factories(Factory Class)
------------------------
![Screenshot from 2022-05-18 12-30-48](https://user-images.githubusercontent.com/78407424/168977431-5c30fa5c-9c27-4488-b32b-d60612abcb22.png)

Indexing
--------
![Screenshot from 2022-05-19 03-27-55](https://user-images.githubusercontent.com/78407424/169162720-4ab582e3-7583-4596-ad91-634d2eefba9d.png)

Caching
-------
![Screenshot from 2022-05-17 14-21-50](https://user-images.githubusercontent.com/78407424/168771375-42c89091-3ad8-4f98-96ed-baf03a24e506.png)


EAV
---

















#Backend
 --------
 
 Dependency Injection
 ---------------------
              Dependency Injection 
             --------------------
                 |-----deffination
                 |-----diff ways or types of injection(constructor,method, by declaring di.xml way)
                 |-----require file to implement the injection
                 |-----types of dependency class
                 |                          |-----Injectable 
                 |                                      |---------what is singleton(cache memory)
                 |                          |-----Non-Injectable
                 |                                      |----------what is Factory class(entity table)
                 |                                      |                    |-------------when we need to use factory class
                 |                                      |                    |-------------advantage of factory class
                 |                                      |----------what is Proxy Class(Lazy loading, Object chaining)
                 |                                                      |--when we need to use proxy class
                 |                                                      |--where we need to declare the proxy class(di.xml)
                 |                                                          |----why we did not use proxy class directly inside constructor inject
                 |-----which two types of node di.xml file support 
                 |                                      |--------type
                 |                                      |--------virtual type
                 |
                 |-----what is the use type
                 |-----what is the use of virtual type
                 |-----Difference bewteen type and virtual type
                 |                                     |---------when to use type 
                 |                                     |---------when to use virtual type
                 |-----What are all the concept we can use to modify the magento core functionality without touching core files
                 |                             |
                 |                             |
                 |                             |----Type
                 |                             |
                 |                             |----Virtual Type
                 |                             |
                 |                             |----Plugin
                 |                             |         |-------what is plugin
                 |                             |         |-------how to declare plugin(folder way)
                 |                             |         |-------where exactly we can apply the plugin(rule's)
                 |                             |         |-------advantage and limitation of plugin
                 |                             |         |-------types of plugin
                 |                             |                         |------what is before plugin(changing method input parameter)
                 |                             |                         |------what is after plugin(changing method output parameter)
                 |                             |                         |------what is around pluign(changing actuall implementation of original code)
                 |                             |
                 |                             |----Preference
                 |                             |            |----what is preference
                 |                             |            |----how to declare plugin(folder way)
                 |                             |            |----where exactly we can apply the preference(rule's)
                 |                             |            |----advantage and limitation of plugin
                 |                             |
                 |                             |----Event and Observer(no modification to original class. need to communicate with other classes)
                 |                                          |---------what is event and observer
                 |                                          |---------how to declare plugin(folder way)
                 |                                          |---------where exactly we can apply the preference(rule's)
                 |                                          |---------advantage and limitation of plugin
                 |
                 |-----Why magento doe's not create object using new keyword
                 |-----Why magento did not allow direct use of Object Manager
                 |-----Why we did not specify Proxy in the Class Constructor Directly
                 |-----When we put Factory to Any Class -- how magento will knowing this and when    
                 |
                 |------------What is Object Manager in Magento(to mange the object by checking from di.xml(all the things declare here)
                                                          |----------what is the use of create() method (for non-injectable class)
                                                          |----------what is the use of get() method (for injectable class)
                 


Indexing
--------
      Indexing
      ========
        |
        |---What is Indexing in Magento
        |               |-------Why we need Indexing
        |               |-------How many types of Indexing mode
        |                                 |-----How Update on Save is working
        |                                 |-----How Update on Schedule is working
        |                                           |----Explain end to end how schedule work based on cron job
        |                                                          |------what is change_log table and how it tigger      
        |                                                          |------what is tigger function
        |                                                                  
        |---What all file require to implement indexing concept in magento
                                        |----------what is the use of indexer.xml
                                        |----------what is the use of mview.xml 
                                                          |-----how mview file is link with other files and help cron job to work                                  
Caching
-------
    Caching 
    =======
      |
      |----------what is caching
      |                    |-------why we need caching in magento 
      |                    |-------how to know is cache is enable for particular section in magento
      |                    |-------if we declare cache is false then what happen 
      |                    |-------how to know is the site is full cache enabled
      |
      |----------What are all the way to know is the page is cache enable and how to achieve 
      |
      |---------how many types of cache mechanism
      |                           |---------------what is public content(server side)
      |                           |                            
      |                           |---------------what is private content(client side) 
      |                                                      |------------what type of data is called private content
      |--------how cahce is related with
                                      |------varnih
                                      |------redis
                                      |------Opchache
                                      |------JIT
                                      |------Zend Engine 
                   
                   
                   
Declarative Schema
------------------       
    Declarative Schema
    ==================
        |
        |-----What is declarative schema
        |                          |-------what all files need to implemnt the declare schema in magento
        |                          |-------how we can perform crud operation using db_schema.xml only
        |
        |----what is the use of db_schema_whitelist.json
        |                          |-----------------------Is mantory to keep the db_schema_whitelist if no then why 
        |
        |----What is Patchs
        |             |-------how many types of patchs available
        |             |                            |----------------what is Data patch
        |             |                            |              
        |             |                            |----------------what is Schema patch
        |             |
        |             |------If we need to create attribute then which patch we need to use
        |             |------If we need to insert data into table then which patch we need to use
        |


Service Contract
----------------
    Service Contract
    ================
       |
       |------What is Service contract
       |                 |-----------why should any one implement Service contract in magento
       |                 |-----------Benefit of Service Contract 
       |------types of interface service contract concept implement
       |                        |-------what is Data interfaces
       |                        |                        |---------what is data integrity
       |                        |-------what is service interfaces 
       |                                                 |----------types of service interfaces
       |                                                 |----------what is  Repository interfaces(CRUD)
       |                                                 |----------what is Management interfaces(send the email, manage related)
       |                                                 |----------what is Metadata interfaces(Eg-name has --first_name, last_name)
       |          
                  
    
      
EAV 
===
                             
       EAV 
      =======
        |--------what is EAV
        |                 |----Why Magento implement EAV concept why not other concept to manage the data
        |                 |----How many types of entity table in magento(9)
        |                 |----How many types of data types table for entity table in magneto(5)
        |                 |----From Which table we will get the complete details of eav_table(eav_entity_type)    
        |                 |----Explain the complete eav_table relation in magento
        |                 |---If we need to add simple customer attribute then explain 
        |                                                                  |----complete flow table including attribute creation from code
        |  
        |--------types of eav attribute 
        |          |--------Custome attribute
        |          |                     |---------
        |          |                     |---------
        |          |
        |          |--Extension Attribute
        |                 |               
        |                 |
        |                 |---What is extension attribute
        |                 |---what all folder structure need to implemnt extension attribute
        |                 |---what is the use of resource in extension_attribute in magento
        |                 |                |-------------------what is the use of join in extension_attribute
        |                 |                |-------------------what are all type of extension attribute (string, init, float or Object)
        |                 |---If we need to add extension attribute for customer then what we need to do.
        |                 |--For getting and set the extension attribute which interface we need extends in service contract design.
                
                
                
                
                

































Magento Command with output 
---------------------------
     Magento Command with output
     ===========================
         |
         |--------------------What is console command in magento
         |                                  |------------------how to check all magento console command
         |                                  |------------------how to create custom console command in magento
         |
         |------------------What happen if we run 
                                  |
                                  |-------------sudo bin/magento se:di:co 
                                  |                                    |----------how setup decompile command is related with di.xml file 
                                  |-------------sudo bin/magento setup:upgrade
                                  |-------------sudo bin/magento cache:flush
                                  |-------------sudo chmod -R 777 var/ pub/ generated/
                                  |                          |----------------why we need to give the permision to var and pub and generated file
                                  |
                                  |-------------what will happen if we remove generated folder 
                                                                                |-----If no then explain what actual requirement of generated folder










Ground Level
------------


    - How magento is taking memory.
            |-------From Which File Magento Code get Executed
            |-------How i can find particular route in magento by folder(code) structure way internally
            |-------Why magento keep this much folder 
            |-------Explain all the folder present in magento and their uses
            |-------If we delete some of the folder then what happen if not then why 
                            |-------Based on Which mechanism magento is Working
                            |-------What all concept magento is implementing  and When




   

             - Use of Elasticsearch. why magento use elasticsearch
                                                 |--------what is elasticsearch
                                                 |--------advantage of elasticsearch
                                                 |--------how elasticsearch work internally
                                                 |--------It is necessary to use elasticsearch
                                                 |--------If We need to change anything in elasticsearch then how can we change 
                                                 |--------Which port it is taking and how it detect the port 
                                                 |-------Why anyone choose elasticsearch
                                       
  
              - Use of Varnish. Why magento use varnish
                                         |--------what is varnish
                                         |--------advantage of varnish
                                         |--------how varnish work internally
                                         |--------It is necessary to use varnish
                                         |--------If We need to change anything in varnish then how can we change 
                                         |--------Which port it is taking and how it detect the port 
                                         |-------Why anyone choose varnish
  
              - Use of Redis . Why magento use Redis
                                      |--------what is Redis
                                      |--------advantage of Redis
                                      |--------how Redis work internally
                                      |--------It is necessary to use Redis
                                      |--------If We need to change anything in redis then how can we change 
                                      |--------Which port it is taking and how it detect the port
                                      |-------Why anyone choose redis 



                   - How to Know In Which File or Which Mechanism Magento Configure Varnish, Redis and Elasticseaerch along with Php
                                                        |
                                                        |-------How Varnish and Redis is Related with Cache and Indexing
                                                        |-------Is it mandotory to use varnish and redis at the same time for magento if yes then Why 
                                                                                         
                                                                                        
                                    
       

                 - What all Application Mode in Magento
                                 |-------By default which application mode magento have 
                                 |-------How to know which application mode we will use and When
                                 |-------What advantage we will get by Application Mode
                                 |-------Is it Helpfull for  Magento 
                               

                - What is Indexing
                            |----------------What are all Indexing mode in magento
                            |----------------How Indexing is Usefull for Magento
   
PHP
===          
       PHP
       ===
        |------ How Php code get executed
        |------ Php is a which type of language compiled or interpreted
        |------ Difference between Compiled and Interpreted Language
        |------ Functional Programming vs Object oriented 
        |------ What all mechanishm Php follow for better Performance Result
        |------ What are all the Step Require to Compile the Php Code
        |------ What is Opchace Mechanism in Php
        |------ What JIT concept in Php and Where it Require
        |------ What is the use of Zend Engine in Php
        |------ What all file contain Zend Engine
        |------ What is the Difference between Zend Engine and Zend Framework
        |------ What is the use of PEAR and PECL
        |------ What is the use of Auto_load() method in Php
        |------ Why any one need to use namespaces in Php
        |------ What are all magic method Present in Php and what is magic method
        |
        |------------------OOPS
        |                    |------What is Class
        |                    |                |------variable
        |                    |                |          
        |                    |                |------constructor
        |                    |                |             |------default
        |                    |                |             |------parameterized
        |                    |                |------methods
        |                    |                
        |                    |------What is Object
        |                    |                |--------what is state 
        |                    |                |--------what is behaviour
        |                    |                |--------what is identity
        |                    |------What is Methods
        |                    |                |--------final and static method
        |                    |------What is Variables
        |                    |                 |-------What all variable Scope in Php
        |                    |-------What is Abstraction
        |                    |                    |-----------What is abstract class
        |                    |                    |-----------What is abstract method 
        |                    |                    |-----------Explain exact rule to implement abstraction concept in Php
        |                    |-------What is Encapsulation
        |                    |                      |--------Explain the encapsulation by giving proper code representation
        |                    |-------What is Inheritance
        |                    |                   |---------How many types of inheritance support by Php
        |                    |                   |---------What is the use of Traits in Php
        |                    |-------What is Polymorphisim
        |                    |                     |----------compiled time(static)or(overloading)
        |                    |                     |----------run time(dynamic)or(overriding)
        |                    |
        |                    |-------What is Interface in Php
        |                    |                    |---------------Explain complete implementation of Interface
        |                    |------What is the Difference betweeen Interface and Abstraction  
        |
        |-------------What are all Access Specifier in Php
        |                                      |-------------What is Public and its Scope
        |                                      |-------------What is Protected and its Scope
        |                                      |-------------What is Private and its Scope
        |
        |
        |-----comming soon......
        
        
        
        
        
        


Magento Related Commands
========================

   - bin/magento 


   - bin/magento list | grep mode
   - bin/magento deploy:mode:show
   - 

        
        
 
 
 
 
  



