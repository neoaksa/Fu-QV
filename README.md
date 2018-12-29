# Fu-QV
### @20181229
#### Problem:
* How could `events` map to `org`? It seems they are matching each other in RM level, but the data is a mess which mixed other information. 
* Clarify the defination of `User Day` and `CFR`


#### QV model v0.1
![img](/imgs/QV_Model.jpg)


### @20181228
1. Overview-page1
* Opt in# = the number of physician marked with `opt in`, then what is `opt out` if we've never keep the historical data?
* send% = #optin / total number of physician or the ones in the target list(sales or call alignment?). 
* send# = the number of physician who received any message in the given period?
* Open% = open#/send#
* what are the indexes in `user status` section?
* How many of tabs(containers)? what are their names? which dashboards do they include?
* what is `subject` and `evolution` in the table underneath? ranking by which column?
* what is `region`,`area` and `Buyer Provi`? and what is `call plan` filter?

2. Overview-page2
* Is this page all about opt-in?
* How to retrieve the data "所有曾经认证的医生"?

3. Overview-page3
* what does the table left side about?
* what is `"Event Trand` and its value?

4. Overview-page4
* what does the table left side about?
* how to calculate Mass send? 

5. Others:
* where do we use `sales` tables? I only found the some relationship pointing to `call`. 

6. Drafted tables
* org(rd id, rd name,ad id, ad name, dm id, dm name, mr id, mr name)
* time(month, mtd, circle, cycle, ytd)
* physician(id, gender, department, title, segment, hospital id, hospital name, call plan, dbgm, device, is_opt_in,) can a doctor register more than one device?
* physician_mr(mr id, physician id, brand id, brand name, opt_in)
* wechat(id, mr id, brand id, brand name, physician id, is_read, duration, content) 
  
