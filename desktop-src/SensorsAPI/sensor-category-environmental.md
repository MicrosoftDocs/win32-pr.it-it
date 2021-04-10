---
description: La \_ categoria sensore \_ Environment Category contiene sensori che forniscono informazioni sull'ambiente o sul meteo circostante.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5c41d4c117dc27a3303210a485b2233cf24cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878909"
---
# <a name="sensor_category_environmental"></a>categoria di sensori \_ \_ ambiente

La \_ categoria sensore \_ Environment Category contiene sensori che forniscono informazioni sull'ambiente o sul meteo circostante.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                                                                                     | Descrizione               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**Sensore \_ di Digitare \_ la \_ \_ pressione atmosferica ambientale**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barometri.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**Sensore \_ di Digitare \_ \_ umidità ambientale**</dt> <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Igrometri.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**Sensore \_ di Digitare \_ la \_ temperatura ambiente**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Termometri<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**Sensore \_ di Digitare \_ la \_ \_ direzione del vento ambientale**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Alette Meteo.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**Sensore \_ di Digitare \_ la \_ \_ velocità del vento Environment**</dt> <dt>{DD50607B-A45F-42cd-8EFD-EC61761C4226}</dt> </dl>                               | Anemometri.<br/>   |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ GUID ambientale del tipo di dati del sensore \_ \_ :

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**Sensore \_ di \_ \_ \_ \_ Barra pressione atmosferica del tipo di dati**</dt> <dt>(PID = 4)</dt> </dl>                                      | **\_R4 VT**<br/> Pressione atmosferica in ambienti (barre).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**Sensore \_ di Temperatura del tipo di dati \_ \_ \_ Celsius**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **\_R4 VT**<br/> Temperatura in gradi Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**Sensore \_ di \_ \_ \_ \_ Percentuale umidità relativa del tipo di dati**</dt> <dt> (PID = 3)</dt> </dl>                                  | **\_R4 VT**<br/> Umidità relativa come percentuale.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**Sensore \_ di Tipo di dati di direzione del vento in senso \_ \_ \_ \_ \_ antiorario**</dt> <dt>(PID = 5)</dt> </dl> | **\_R4 VT**<br/> Direzione del vento rispetto al nord magnetico, in gradi. Il Nord è rappresentato come 0,0 (parte superiore dell'asse X), con valori che aumentano in una rotazione in senso antiorario. L'asse Z punta verso l'alto. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ \_ contatori velocità del vento \_ \_ al \_ secondo**</dt> <dt>(PID = 6)</dt> </dl>                        | **\_R4 VT**<br/> Velocità del vento in metri al secondo.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




