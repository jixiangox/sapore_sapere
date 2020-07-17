# sapore_sapere
Objective
  Turn a smartphone into a mobile BLE device in restricted internet-accessible environment.
  An reduced features of Exposure Notifications System of Google and Apple
  No central server architecture design; implement it in a Mobile App.
  In current architecture PHA App interface with Google Play Service and Internet-accessible server (Exposure Notifications Server),
  We plan to implement this Internet-accessible server as a Mobile App or a component of the PHA App (Probabile the first one)
  Or deploy this Internet-accessible server in Private network (e.g. in company, airplan, or factory)
  It helps HR to lower the cost and risk to secure company (Once a member in company is dignosis positive, the affected area and scope will be shorten)
  Especially for huge orgnization.


Phase I:  w/ Infra

I.1: Retain Exposure Notifications System and Implement it in Intranet and wait for Google and Apple to free the restriction
  Similar architectue:
  https://developer.apple.com/wwdc20/10113
The architecture of Exposure Notifications System is the same; to deploy the Internet-restricted server in Intranet.
People in private sector install the PHA App.
This architecture does rely on the to free the restriction of only one PHA App in one country/region; otherwise the Exposure Notifications APIs wont work.

Phase II: w/o Infra

II.1 : Singapore way
Or re-implement the undergo APIs to bypass the restriction set by Apple and Google. It takes time to do so and not sure it will work or not.
In Singapore way, the roll out mobile device shall not depend on the underlying APIs supported by iOS/Android.
In this architecture, Infra is not required. It includes PHA people in the whold process. The rolled out mobile device collect proximity TEKs and store them in device's data store. The assumption is the diagnosis is tested only in hospital like Taiwan. Once the person with wearable mobile device diagnosis positive, the one has been isloated in hospital, PHA People can extract the TEKs (now we call them Diagnosis Keys) out and do the comparision out of the box. I am not quite sure where to execute the algorithm. maybe PHA people is good by asking right questions to get the track back in past 14-28 days in cooperating with the telco's mobile signal calculation. It might be performed within telco's server room. Those extraced Diagnosis Keys can then be the assistance logs and help to verify what the tools PHA people are using currently (recall the memory of diagnosis positive person, and compare with the mobile station's signal trace). Nothing changes in this mode but provide additional info to reduce the manpower of police.

