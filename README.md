# DxQSO-API-Demo
DxQSO is a ham radio cloud logbook repository **(It is not a ham radio logbook app!)** which acts as a QSO clearinghouse integrating logbook data from multiple ham radio logbook applications as well as to/from LoTW and QRZ.com and the the DxQSO website and DxQSO mobile applications (Android and IOS).

Through a high speed serverless architecture built on AWS, DxQSO provides a unified view of all logbook data (through a modern API) as well as email and mobile push alerts for new QSLs and new State, DXCC and Grid square QSL achievements. It also includes DxSocial, a social media site built for teams/clubs to share realtime operating QSO data and QSL achievements as well as club based discussions, blogs, files and web links.

The DX-TQSL Windows/Mac application provides realtime DxQSO logbook integration for users whether they use LoTW or not. As a replacement for TQSL, it provides cloud based certificate management and stations and backs up all local TQSL information and uploads to either LoTW and DxQSO or just to DxQSO. 

Users may upload their existing logbooks through the DxQSO website, mobile application or DX-TQSL and maintain all detailed logbook data. When downloaded, Logbook records are automatically converted into target logbook application formats (N1MM, HRD, MacLogger, Polo, etc).

The DxQSO mobile app provides instant access to your entire logbook, real time local logbook updates, QSL alerts for new confirmations, alerts for new QSL Achievements for DXCC, States or Gridsquares and allows you to upload QSOs directly from your mobile via ADIF upload or directly from other mobile apps through the N1MM listener.

**This demo website demonstrates the DxQSO client API which can be used by ham software applications to directly upload ham logbook data, view DxQSO station info and download QSOs.** 

This website is running live on **https://demo.dxqso.net**.

You must have a Vendor Key (Provided by DX Development) and Station Key (provided to DxQSO users for each station they have setup) in order to connect to your DxQSO account data through this demo website.
