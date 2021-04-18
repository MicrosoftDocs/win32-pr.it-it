---
description: I dispositivi portatili Windows definiscono i valori di evento seguenti.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Costanti di evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328858"
---
# <a name="event-constants-portabledeviceh"></a>Costanti di evento (PortableDevice. h)

I dispositivi portatili Windows definiscono i valori di evento seguenti.



| Costante                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**\_funzionalità del \_ dispositivo evento WPD \_ \_ aggiornate**</dt> </dl> | Questo evento indica che le funzionalità del dispositivo sono state modificate. I client devono eseguire una query sul dispositivo se hanno preso decisioni in base alle funzionalità del dispositivo.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_dispositivo evento \_ WPD \_ rimosso**</dt> </dl>                                         | Questo evento viene inviato quando viene scaricato un driver per un dispositivo. In genere si tratta di un risultato del dispositivo scollegato.<br/> I client devono rilasciare l'interfaccia **IPortableDevice** e tutte le interfacce [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) specificate nel **parametro dell' \_ evento WPD \_ \_ \_ \_ ID del dispositivo PNP**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**reimpostazione del \_ dispositivo evento WPD \_ \_**</dt> </dl>                                               | Questo evento indica che il dispositivo sta per essere reimpostato e che tutti i client connessi devono chiudere le connessioni al dispositivo.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_oggetto evento \_ WPD \_ aggiunto**</dt> </dl>                                               | Questo evento indica che nel dispositivo è disponibile un nuovo oggetto.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**\_oggetto evento \_ WPD \_ rimosso**</dt> </dl>                                         | Questo evento viene inviato dopo la rimozione di un oggetto precedentemente esistente dal dispositivo.<br/> L'oggetto potrebbe essere un oggetto contenuto, ad esempio un file di immagine è stato eliminato. oppure potrebbe trattarsi di un oggetto funzionale, ad esempio un nuovo dispositivo di archiviazione è stato scollegato dal dispositivo.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**è \_ stato \_ \_ richiesto il trasferimento dell'oggetto evento WPD \_**</dt> </dl>       | Questo evento viene inviato per richiedere a un'applicazione di trasferire un oggetto specifico dal dispositivo.<br/> L'oggetto è in genere un oggetto contenuto, ad esempio un file di immagine.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**\_oggetto evento \_ WPD \_ aggiornato**</dt> </dl>                                         | Questo evento viene inviato dopo l'aggiornamento di un oggetto e qualsiasi client connesso deve aggiornare la visualizzazione di tale oggetto.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**\_metodo del \_ servizio eventi WPD \_ \_ completato**</dt> </dl>             | Questo evento viene inviato quando un driver ha completato la chiamata a un metodo del servizio. Questo evento deve essere inviato anche quando il metodo ha esito negativo. Si tratta di un evento di DDI WPD interno e non sarà disponibile per le applicazioni tramite [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) o [**IPortableDeviceService:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**\_formato di \_ archiviazione \_ eventi WPD**</dt> </dl>                                         | Questo evento indica lo stato di un'operazione di formattazione su un oggetto di archiviazione.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
</dt> </dl>

 

 




