---
description: La \_ \_ categoria meccanica categoria sensore contiene sensori che forniscono informazioni correlate a dispositivi e misure meccaniche.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2446559820141b65a70bc75d25680da79563388c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306351"
---
# <a name="sensor_category_mechanical"></a>categoria di sensori \_ \_ meccanica

La \_ \_ categoria meccanica categoria sensore contiene sensori che forniscono informazioni correlate a dispositivi e misure meccaniche.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                                           | Descrizione                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**Sensore \_ di Digitare \_ l' \_ opzione booleana**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | Commutatori a due stati (disattivato o attivato).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**Sensore \_ di Digitare \_ la \_ \_ matrice del commutire booleano**</dt> <dt>{545C8BA5-b143-4545-868F-CA7FD986B4F6}</dt> </dl> | Matrice di opzioni a due stati (off o on).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**Sensore \_ di Digitare \_ Force**</dt> <dt>{C2AB2B02-1A1C-4778-a81b-954A1788CC75}</dt> </dl>                                                | Forza i sensori.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**Sensore \_ di Digitare \_ il \_ comswitch multivalore**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Opzioni a più posizioni.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**Sensore \_ di \_Pressione del tipo**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Sensori di pressione.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**Sensore \_ di TIPO \_ scala**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Sensori di peso.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**Sensore \_ di \_Strain di tipo**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Sensori di tensione.<br/>                          |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ GUID meccanico del tipo di dati Sensor \_ \_ \_ :

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                         | Descrizione                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ \_ pressione assoluta \_ Pascal**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Pressione assoluta, in Pascal.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**Sensore \_ di Tipi di dati \_ \_ Stati di \_ \_ matrici \_ di commutiri booleani**</dt> <dt>(PID = 10)</dt> </dl> | **\_UI4 VT**<br/> Campi di stato per una matrice di commutatori booleani.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**Sensore \_ di \_ \_ \_ \_ Stato switch booleano tipo di dati**</dt> <dt>(PID = 2)</dt> </dl>                       | **\_bool VT**<br/> Campo di stato per \_ l' \_ opzione booleana del tipo di sensore \_ .<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ forza \_ Newton**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Forzare, in Newton.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ pressione del misuratore \_ \_ Pascal**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Pressione del misuratore relativa, in Pascal.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**Sensore \_ di \_ \_ \_ \_ Stato switch multivalore del tipo di dati**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Campo di stato per \_ l' \_ opzione multivalore del tipo di sensore \_ .<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**Sensore \_ di \_ \_ Strain tipo di dati**</dt> <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Ceppo.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ peso \_ chilogrammi**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Peso, in chilogrammi.<br/>                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




