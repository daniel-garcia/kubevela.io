---
title:  AWS ROUTE53-RECORDS
---

## 描述

Terraform module which creates Route53 resources on AWS

## 参数说明


### 属性

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 records | List of maps of DNS records | any | false |  
 create | Whether to create DNS records | bool | false |  
 zone_id | ID of DNS zone | string | false |  
 zone_name | Name of DNS zone | string | false |  
 private_zone | Whether Route53 zone is private or public | bool | false |  
 writeConnectionSecretToRef | The secret which the cloud resource connection will be written to | [writeConnectionSecretToRef](#writeConnectionSecretToRef) | false |  


#### writeConnectionSecretToRef

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 name | The secret name which the cloud resource connection will be written to | string | true |  
 namespace | The secret namespace which the cloud resource connection will be written to | string | false |  
