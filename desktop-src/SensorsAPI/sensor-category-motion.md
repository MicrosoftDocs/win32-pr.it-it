---
description: La categoria SENSOR \_ CATEGORY MOTION contiene sensori che forniscono informazioni correlate al movimento \_ fisico.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d57c8406ad1344d696f63e574484943ea68a6654f63c3d7d38e904aaa44e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889489"
---
# <a name="sensor_category_motion"></a>MOVIMENTO \_ CATEGORIA \_ SENSORE

La categoria SENSOR \_ CATEGORY MOTION contiene sensori che forniscono informazioni correlate al movimento \_ fisico. Gli accelerometri misurano l'accelerazione del sensore, inclusa l'accelerazione gravitazionale. I rilevatori di movimento, ad esempio il rilevamento del movimento umano in un sistema di sicurezza, rilevano gli oggetti in movimento. I giroscopi misurano i cambiamenti nella velocità angolare. I tachimetri misurano la velocità.

**Tipi di sensori definiti dalla piattaforma**

Questa categoria include i tipi di sensori definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                              | Descrizione                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**SENSORE \_ TYPE \_ ACCELEROMETER \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | Accelerometri a un asse.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**SENSORE \_ TYPE \_ ACCELEROMETER \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Accelerometri a due assi.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**SENSORE \_ TYPE \_ ACCELEROMETER \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Accelerometri a tre assi.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**SENSORE \_ TIPO \_ GYROMETER \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Giroscopi a un asse.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**SENSORE \_ TIPO \_ GYROMETER \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Giroscopi a due assi.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**SENSORE \_ TIPO \_ GYROMETER \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Giroscopi a tre assi.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**SENSORE \_ RILEVAMENTO \_ \_ DEL MOVIMENTO**</dt> <dt>DEL TIPO {5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Rilevatori di movimento, ad esempio quelli usati nei sistemi di sicurezza.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**SENSORE \_ TYPE \_ SPEEDOMETER**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Sensori di velocità di movimento.<br/>                                   |



**Campi dati definiti dalla piattaforma**

Le chiavi di proprietà definite dalla piattaforma per questa categoria sono basate su SENSOR \_ DATA \_ TYPE MOTION \_ \_ GUID:

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                                                                                               | Descrizione                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**SENSORE \_ ACCELERAZIONE \_ DEL TIPO DI DATI X \_ \_ \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accelerazione dell'asse X, in g's.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**SENSORE \_ ACCELERAZIONE \_ \_ DEL TIPO DI DATI \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accelerazione dell'asse Y, in g's.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**SENSORE \_ ACCELERAZIONE \_ \_ DEL TIPO DI DATI \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accelerazione dell'asse Z, in g's.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**SENSORE \_ TIPO \_ DI \_ DATI ANGULAR \_ ACCELERATION X DEGREES PER SECOND \_ \_ \_ \_ \_ SQUARED**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Accelerazione dell'asse x girometrico, in gradi al secondo al quadrato.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**SENSORE \_ TIPO \_ \_ DI DATI ANGULAR \_ ACCELERATION Y DEGREES PER SECOND \_ \_ \_ \_ \_ SQUARED**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Accelerazione dell'asse y girometrico, in gradi al secondo al quadrato.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**SENSORE \_ TIPO \_ DI \_ DATI ANGULAR \_ ACCELERATION Z DEGREES PER SECOND \_ \_ \_ \_ \_ SQUARED**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Accelerazione dell'asse z girometrico, in gradi al secondo al quadrato.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**SENSORE \_ TIPO \_ \_ DI DATI ANGULAR \_ VELOCITÀ X GRADI AL \_ \_ \_ \_ SECONDO**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Velocità dell'asse x girometrico, in gradi al secondo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**SENSORE \_ TIPO \_ \_ DI DATI ANGULAR \_ VELOCITÀ Y GRADI AL \_ \_ \_ \_ SECONDO**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Velocità dell'asse y girometrico, in gradi al secondo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**SENSORE \_ TIPO \_ \_ DI DATI ANGULAR \_ VELOCITÀ Z GRADI AL \_ \_ \_ \_ SECONDO**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Velocità dell'asse z girometrico, in gradi al secondo.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI MOTION \_ \_ STATE**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **VT \_ BOOL**<br/> **TRUE** se viene rilevato il movimento. in caso contrario, **FALSE.**<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**SENSORE \_ METRI \_ DI VELOCITÀ DEL TIPO DI DATI AL \_ \_ \_ \_ SECONDO**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Velocità in metri al secondo.<br/>                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




