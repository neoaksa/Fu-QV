# Fu-QV
### @20190110
1. add physician dashboards
![img](/imgs/physician.PNG)


### @20190107
#### Task
* Section section: physician analysis
* wechat should arrgraged by day rather than month
* historial org data


### @20181230
#### First Version
![img](/imgs/Capture1.PNG)

#### Problem
* In order to calculate `send#`, `open#`, `click#` and their corresponding ratios, we need to know the scope of physicians. e.g, when I design the `Opt in status` and `Interaction`, I use the number of all physicians including whom are not target. But in the section of `KPI Analysis`, I filtered target physicians(call_plan > 0). 
* equation of `user day`
* Only one month data in `wechat summary`
* compared with the opt-in/out physicians, the size of all physicians is too huge, so that we barely see the other three ones underneath( I hide the block for all physicians).
* Give me more details about `Trend` in the container. `Opt in`- no time dimension
* equation of `Sent Covera%`, does it mean send#/all target physician?
* ADD Time dimension in QV
* Only few org can be matched to wechat records, which leads to pretty hard to do verification work.

### @20181229
#### Problem:
* How could `events` map to `org`? It seems they are matching each other in RM level, but the data is a mess which mixed other information. 
* Clarify the defination of `User Day` and `CFR`


#### QV model v0.1
![img](/imgs/QV_Modelv0.2.jpg)


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
  
