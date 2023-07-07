# Lab 18: Setting Up for Capacity Scheduler Labs

---
## Creating Linux Groups
  Create Linux groups named promo, sales, dev, and qa using the groupadd command on ALL NODES in your cluster. Login to each of your cluster nodes and switch to the root user.

**sudo su -**

 #groupadd promo

 #groupadd sales 

 #groupadd dev 

 #groupadd qa

*Script for creating HDFS home directory for each user*  
---
Bash

#vim hdfs.sh

        //edit and write below simple code and save as a hdfs.sh file extenstion.
        
        #!/bin/bash
        hdfs dfs -mkdir /user/dev01 
        hdfs dfs -chown dev01:dev01 /user/dev01
        
        hdfs dfs -mkdir /user/dev02 
        hdfs dfs -chown dev02:dev02 /user/dev02
        
        hdfs dfs -mkdir /user/dev13 
        hdfs dfs -chown dev13:dev13 /user/dev13
        
        hdfs dfs -mkdir /user/qa01 
        hdfs dfs -chown qa01:qa01 /user/qa01
        
        hdfs dfs -mkdir /user/qa02 
        hdfs dfs -chown qa02:qa02 /user/qa02
        
        hdfs dfs -mkdir /user/qa05 
        hdfs dfs -chown qa05:qa05 /user/qa05
        
        hdfs dfs -mkdir /user/sales01 
        hdfs dfs -chown sales01:sales01 /user/sales01
        
        hdfs dfs -mkdir /user/sales02 
        hdfs dfs -chown sales02:sales02 /user/sales02
        
        hdfs dfs -mkdir /user/sales04 
        hdfs dfs -chown sales04:sales04 /user/sales04
        
        hdfs dfs -mkdir /user/promo01 
        hdfs dfs -chown promo01:promo01 /user/promo01
        
        hdfs dfs -mkdir /user/promo02
        hdfs dfs -chown promo02:promo02 /user/promo02
        
        hdfs dfs -mkdir /user/support01
        hdfs dfs -chown support01:support01 /user/support01
        
        hdfs dfs -mkdir /user/support02
        hdfs dfs -chown support02:support02 /user/support02
        
        hdfs dfs -mkdir /user/support09
        hdfs dfs -chown support09:support09 /user/support09
        
---

#### Script for Create Linux groups named promo, sales, dev, and qa using the groupadd command on ALL NODES in your cluster. Login to each of your cluster nodes and switch to the root user. ####
---
Bash

vim groupadd.sh   
    
    #!/bin/bash
    groupadd promo
    groupadd sales
    groupadd dev
    groupadd qa
    
    useradd dev01 -G dev
    useradd dev02 -G dev
    useradd dev13 -G dev
    
    useradd promo01 -G promo
    useradd promo02 -G promo
    
    
    useradd qa01 -G qa
    useradd qa02 -G qa
    useradd qa05 -G qa
    
    useradd sales01 -G sales
    useradd sales02 -G sales
    useradd sales04 -G sales
    
    useradd support01
    useradd support02
    useradd support09
    



