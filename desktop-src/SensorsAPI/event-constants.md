---
description: La piattaforma sensore e posizione di Windows definisce le costanti per gli eventi del driver. Il sensore manfuactureres può anche definire le proprie costanti.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Costanti evento (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315332"
---
# <a name="event-constants-sensorsh"></a>Costanti evento (Sensors. h)

La piattaforma sensore e posizione di Windows definisce le costanti per gli eventi del driver. Il sensore manfuactureres può anche definire le proprie costanti.

**Tipi di eventi del sensore**

La piattaforma definisce gli identificatori del tipo di evento del sensore seguenti.



| Tipo di evento del sensore                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**Sensore \_ di \_ \_ Scuotimento dell'accelerometro evento**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Indica che il dispositivo è stato agitato.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**Sensore \_ di \_Dati evento \_ aggiornati**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Indica che i nuovi dati sono disponibili.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**Sensore \_ di \_Proprietà evento \_ modificata**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Indica che un valore della proprietà è stato modificato. Controllare l'interfaccia [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , passata tramite il parametro *PEventData* a [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), per determinare quale proprietà è stata modificata e il nuovo valore.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**Sensore \_ di \_Stato evento \_ modificato**</dt> <dt>{BFD96016-6BD7-4560-ad34-F2F6607E8F81}</dt> </dl>                   | Indica una modifica dello stato operativo, ad esempio, dall' \_ inizializzazione dello stato del sensore \_ allo stato del sensore \_ \_ pronto.<br/>                                                                                                                                                                                            |



**PROPERTYKEYs evento sensore**

Le chiavi di proprietà definite dalla piattaforma per gli eventi si basano sul GUID seguente:

{64346E30-8728-4B34-BDF6-4F52442C5C28}

La piattaforma del sensore definisce i **PropertyKey** seguenti che identificano i parametri degli eventi del sensore.



| Evento del sensore PROPERTYKEY e PID                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**Sensore \_ di \_ \_ \_ ID evento parametro evento**</dt> <dt>(PID = 2)</dt> </dl> | Indica che il valore **GUID** in [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) è un ID del tipo di evento, ad esempio \_ i dati degli eventi del sensore \_ \_ aggiornati.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**Sensore \_ di \_ \_ Stato parametro evento**</dt> <dt>(PID = 3)</dt> </dl>           | Indica che il valore Unsigned Integer in **IPortableDeviceValues** è uno stato del sensore, ad esempio \_ stato del sensore \_ pronto.<br/>                                                  |



**Errore del sensore PROPERTYKEYs**

Le chiavi di proprietà definite dalla piattaforma per gli errori saranno basate sul GUID seguente:

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

La piattaforma del sensore riserva questo GUID per un uso futuro.

<dl></dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

