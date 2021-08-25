---
description: La categoria SENSOR \_ CATEGORY ENVIRONMENTAL contiene sensori che forniscono informazioni \_ sull'ambiente circostante o sulle condizioni meteorologiche.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7cc2a6ca1d2832045a77f0a2ffa1902732e484700afaacd757719e99d667c55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126611"
---
# <a name="sensor_category_environmental"></a>CATEGORIA \_ DI SENSORI \_ AMBIENTALE

La categoria SENSOR \_ CATEGORY ENVIRONMENTAL contiene sensori che forniscono informazioni \_ sull'ambiente circostante o sulle condizioni meteorologiche.

**Tipi di sensori definiti dalla piattaforma**

Questa categoria include i tipi di sensori definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                                                                                     | Descrizione               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**SENSORE \_ TIPO \_ \_ DI \_**</dt> PRESSIONE ATMOSFERICA <dt>AMBIENTALE {0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barometri.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**SENSORE \_ \_UMIDITÀ \_**</dt> AMBIENTALE <dt>DI TIPO {5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Igrometri.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**SENSORE \_ TIPO \_ TEMPERATURA \_ AMBIENTALE**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Termometri<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**SENSORE \_ TYPE \_ ENVIRONMENTAL \_ WIND \_ DIRECTION**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Furgoni meteo.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**SENSORE \_ DIGITARE \_ ENVIRONMENTAL \_ WIND \_ SPEED**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemometri.<br/>   |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate su SENSOR \_ DATA \_ TYPE ENVIRONMENTAL \_ \_ GUID:

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI BARRA DI PRESSIONE \_ \_ \_ ATMOSFERICA**</dt> <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Pressione atmosferica nelle atmosfere (barre).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI TEMPERATURE \_ \_ CELSIUS**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Temperatura in gradi Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**SENSORE \_ PERCENTUALE \_ \_ \_ UMIDITÀ \_ RELATIVA DEL**</dt> TIPO DI DATI <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Umidità relativa come percentuale.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI WIND DIRECTION DEGREES \_ \_ \_ \_ ANTICLOCKWISE**</dt> <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Direzione del vento rispetto al nord magnetico, in gradi. North è rappresentato come 0,0 (parte superiore dell'asse X), con valori che aumentano in una rotazione in senso antiorario. L'asse Z punta verso l'alto. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI WIND SPEED METERS AL \_ \_ \_ \_ \_ SECONDO**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Velocità del vento in metri al secondo.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




