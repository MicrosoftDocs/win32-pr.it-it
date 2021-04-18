---
description: La categoria del movimento della categoria del sensore \_ \_ contiene sensori che forniscono informazioni correlate allo spostamento fisico.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edcb1b5f0a6d02c481774d18ee111ad4ca5e5cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306349"
---
# <a name="sensor_category_motion"></a>\_movimento categoria \_ sensore

La categoria del movimento della categoria del sensore \_ \_ contiene sensori che forniscono informazioni correlate allo spostamento fisico. Gli accelerometri misurano l'accelerazione del sensore, inclusa l'accelerazione gravitazionale. I rilevatori di movimento, ad esempio il rilevamento di movimenti umani in un sistema di sicurezza, hanno senso spostare gli oggetti. Gyrometers Sense changes nella velocità angolare. Velocità di misura tachimetri.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                              | Descrizione                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**Sensore \_ di Digitare \_ accelerometro \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | Accelerometri a un asse.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**Sensore \_ di DIGITARE l' \_ accelerometro \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Accelerometri a due assi.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**Sensore \_ di Digitare \_ accelerometro \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Accelerometri a tre assi.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**Sensore \_ di Digitare \_ giroscopio \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Gyrometers di un asse.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**Sensore \_ di Digitare \_ giroscopio \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Gyrometers a due assi.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**Sensore \_ di Digitare \_ giroscopio \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Gyrometers a tre assi.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**Sensore \_ di TYPE \_ Motion \_ Detector**</dt> <dt>{5C7C1A12-30A5-43b9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Rilevatori di movimento, ad esempio quelli utilizzati nei sistemi di sicurezza.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**Sensore \_ di Digitare \_ tachimetro**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Sensori di velocità di movimento.<br/>                                   |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate sul GUID di movimento del tipo di dati del sensore \_ \_ \_ \_ :

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                                                                                               | Descrizione                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**Sensore \_ di Accelerazione del tipo di dati \_ \_ \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accelerazione dell'asse X, in *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**Sensore \_ di \_Accelerazione tipo di dati \_ \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accelerazione dell'asse Y, in *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**Sensore \_ di \_Accelerazione tipo di dati \_ \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Accelerazione dell'asse Z, in *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**Sensore \_ di \_ \_ Accelerazione angolare del tipo di dati \_ \_ X \_ gradi \_ al \_ secondo \_ quadrato**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Gyrometric-accelerazione asse x, in gradi al secondo quadrato.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**Sensore \_ di \_ \_ Accelerazione angolare del tipo di dati \_ \_ Y \_ gradi \_ al \_ secondo \_ quadrato**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Gyrometric-accelerazione asse y, in gradi al secondo quadrato.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**Sensore \_ di \_ \_ Accelerazione angolare del tipo di dati \_ \_ Z \_ gradi \_ al \_ secondo \_ quadrato**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Gyrometric accelerazione asse z, in gradi al secondo quadrato.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**Sensore \_ di \_ \_ Velocità angolare del tipo di dati \_ \_ X \_ gradi \_ al \_ secondo**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Velocità dell'asse x Gyrometric, in gradi al secondo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**Sensore \_ di \_ \_ Velocità angolare del tipo di dati \_ \_ Y \_ gradi \_ al \_ secondo**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Velocità dell'asse y Gyrometric, in gradi al secondo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**Sensore \_ di \_ \_ Velocità interangolare del tipo di dati \_ \_ Z \_ gradi \_ al \_ secondo**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Velocità dell'asse z Gyrometric, in gradi al secondo.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**Sensore \_ di \_Stato del \_ movimento \_ del tipo di dati**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **\_bool VT**<br/> **True** se viene rilevato un movimento; in caso contrario, **false**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**Sensore \_ di \_Contatori velocità del tipo di dati \_ \_ \_ al \_ secondo**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Velocità in metri al secondo.<br/>                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




