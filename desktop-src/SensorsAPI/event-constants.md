---
description: La Windows sensor e location definisce le costanti per gli eventi del driver. Le manifuacture dei sensori possono anche definire le proprie costanti.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Costanti di evento (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b16be770777c8e679e74123ce1c40c385893afee11ff3792dd58df007ae4c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890229"
---
# <a name="event-constants-sensorsh"></a>Costanti di evento (Sensors.h)

La Windows sensor e location definisce le costanti per gli eventi del driver. Le manifuacture dei sensori possono anche definire le proprie costanti.

**Tipi di evento del sensore**

La piattaforma definisce gli identificatori del tipo di evento del sensore seguenti.



| Tipo di evento del sensore                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**SENSORE \_ EVENT \_ ACCELEROMETER \_ SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Indica che il dispositivo è stato scosso.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**SENSORE \_ DATI \_ \_**</dt> DEGLI EVENTI AGGIORNATI <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Indica che sono disponibili nuovi dati.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**SENSORE \_ PROPRIETÀ \_ \_ DELL'EVENTO**</dt> <dt>MODIFICATA {2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Indica che il valore di una proprietà è stato modificato. Controllare [l'interfaccia IPortableDeviceValues,](/previous-versions//ms740012(v=vs.85)) passata tramite il *parametro pEventData* a [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), per determinare quale proprietà è stata modificata e il nuovo valore.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**SENSORE \_ STATO \_ EVENTO \_ MODIFICATO**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Indica una modifica dello stato operativo, ad esempio da SENSOR \_ STATE \_ INITIALIZING a SENSOR \_ STATE \_ READY.<br/>                                                                                                                                                                                            |



**Proprietà degli eventi del sensore**

Le chiavi di proprietà definite dalla piattaforma per gli eventi sono basate sul GUID seguente:

{64346E30-8728-4B34-BDF6-4F52442C5C28}

La piattaforma del sensore definisce le **proprietà PROPERTYKEY** seguenti che identificano i parametri degli eventi del sensore.



| Evento del sensore PROPERTYKEY e PID                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**SENSORE \_ ID \_ EVENTO DEL PARAMETRO \_ \_ DI**</dt> <dt>EVENTO (PID = 2)</dt> </dl> | Indica che il **valore GUID** in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) è un ID del tipo di evento, ad esempio SENSOR \_ EVENT DATA \_ \_ UPDATED.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**SENSORE \_ STATO \_ DEL \_ PARAMETRO DI**</dt> EVENTO <dt>(PID = 3)</dt> </dl>           | Indica che il valore intero senza segno in **IPortableDeviceValues** è uno stato del sensore, ad esempio SENSOR \_ STATE \_ READY.<br/>                                                  |



**Proprietà degli errori del sensoreKEYS**

Le chiavi di proprietà definite dalla piattaforma per gli errori saranno basate sul GUID seguente:

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

La piattaforma del sensore riserva questo GUID per un uso futuro.

<dl></dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

