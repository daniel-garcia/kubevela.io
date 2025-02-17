---
title:  AWS ELB
---

## 描述

Terraform module which creates ELB resources on AWS

## 参数说明


### 属性

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 internal | If true, ELB will be an internal ELB | bool | false |  
 idle_timeout | The time in seconds that the connection is allowed to be idle | number | false |  
 connection_draining_timeout | The time in seconds to allow for connections to drain | number | false |  
 create_elb | Create the elb or not | bool | false |  
 subnets | A list of subnet IDs to attach to the ELB | list(string) | true |  
 access_logs | An access logs block | map(string) | false |  
 number_of_instances | Number of instances to attach to ELB | number | false |  
 tags | A mapping of tags to assign to the resource | map(string) | false |  
 name | The name of the ELB | string | false |  
 security_groups | A list of security group IDs to assign to the ELB | list(string) | true |  
 connection_draining | Boolean to enable connection draining | bool | false |  
 health_check | A health check block | map(string) | true |  
 instances | List of instances ID to place in the ELB pool | list(string) | false |  
 name_prefix | The prefix name of the ELB | string | false |  
 cross_zone_load_balancing | Enable cross-zone load balancing | bool | false |  
 listener | A list of listener blocks | list(map(string)) | true |  
 writeConnectionSecretToRef | The secret which the cloud resource connection will be written to | [writeConnectionSecretToRef](#writeConnectionSecretToRef) | false |  


#### writeConnectionSecretToRef

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 name | The secret name which the cloud resource connection will be written to | string | true |  
 namespace | The secret namespace which the cloud resource connection will be written to | string | false |  
