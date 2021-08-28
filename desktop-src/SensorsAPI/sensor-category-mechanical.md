---
description: La categoria SENSOR \_ CATEGORY MECHANICAL contiene sensori che forniscono informazioni relative ai dispositivi \_ meccanici e alle misurazioni.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbac9a00895b08bd99106af7f0b6986118b4645dac690fd190f734e1499940dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666711"
---
# <a name="sensor_category_mechanical"></a>CATEGORIA \_ DI SENSORI \_ MECCANICO

La categoria SENSOR \_ CATEGORY MECHANICAL contiene sensori che forniscono informazioni relative ai dispositivi \_ meccanici e alle misurazioni.

**Tipi di sensori definiti dalla piattaforma**

Questa categoria include i tipi di sensori definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                                           | Descrizione                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**SENSORE \_ TYPE \_ BOOLEAN \_ SWITCH**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | Commutatori a due stati (disattivati o attivati).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**SENSORE \_ TYPE \_ BOOLEAN \_ SWITCH \_ ARRAY**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | Matrice di commutatori a due stati (disattivata o attivata).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**SENSORE \_ TYPE \_ FORCE**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | Forzare i sensori.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**SENSORE \_ TYPE \_ MULTIVALUE \_ SWITCH**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Commutatori in più posizioni.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**SENSORE \_ TYPE \_ PRESSURE**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Sensori di pressione.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**SENSORE \_ TYPE \_ SCALE**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Sensori di peso.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**SENSORE \_ \_CEPPO**</dt> <dt>DI TIPO {C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Sensori di pressione.<br/>                          |



**Campi dati definiti dalla piattaforma**

Le chiavi di proprietà definite dalla piattaforma per questa categoria sono basate su SENSOR \_ DATA TYPE GUID MECHANICAL \_ \_ \_ \_ GUID:

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                         | Descrizione                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI ABSOLUTE PRESSURE \_ \_ \_ PASCAL**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Pressione assoluta, in pascal.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI BOOLEAN SWITCH ARRAY \_ \_ \_ \_ STATES**</dt> <dt>(PID = 10)</dt> </dl> | **VT \_ UI4**<br/> Campi di stato per una matrice di opzioni booleane.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI BOOLEAN SWITCH \_ \_ \_ STATE**</dt> <dt>(PID = 2)</dt> </dl>                       | **VT \_ BOOL**<br/> Campo State per SENSOR \_ TYPE \_ BOOLEAN \_ SWITCH.<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI FORCE \_ \_ NEWTONS**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Force, in newtons.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**SENSORE \_ DATA \_ TYPE GAUGE PRESSURE \_ \_ \_ PASCAL**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Pressione relativa del misuratore, in pascal.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**SENSORE \_ TIPO \_ DI \_ DATI \_ MULTIVALORE SWITCH \_ STATE**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Campo State per SENSOR \_ TYPE \_ MULTIVALUE \_ SWITCH.<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**SENSORE \_ CEPPO \_ \_ DEL TIPO DI**</dt> DATI <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Ceppo.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**SENSORE \_ PESO \_ \_ DEL TIPO DI DATI \_ IN KILOGRAMMI**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Peso, in chilogrammi.<br/>                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




