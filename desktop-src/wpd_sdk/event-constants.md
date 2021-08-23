---
description: Windows Dispositivi portabili definisce i valori degli eventi seguenti.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Costanti evento (PortableDevice.h)
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
ms.openlocfilehash: 5ae8a0a519af32a68bd65241f847cadcaa3d623be932a747e21a3b86338d680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704791"
---
# <a name="event-constants-portabledeviceh"></a>Costanti evento (PortableDevice.h)

Windows Dispositivi portabili definisce i valori degli eventi seguenti.



| Costante                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**FUNZIONALITÀ DEL DISPOSITIVO EVENTI WPD \_ \_ \_ \_ AGGIORNATE**</dt> </dl> | Questo evento indica che le funzionalità del dispositivo sono state modificate. I client devono eseguire di nuovo una query sul dispositivo se hanno preso decisioni in base alle funzionalità del dispositivo.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**DISPOSITIVO EVENTI WPD \_ \_ \_ RIMOSSO**</dt> </dl>                                         | Questo evento viene inviato quando viene scaricato un driver per un dispositivo. In genere questo è il risultato della scollegamento del dispositivo.<br/> I client devono rilasciare **l'interfaccia IPortableDevice** e tutte le interfacce [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) specificate in **WPD \_ EVENT PARAMETER \_ \_ PNP \_ DEVICE \_ ID**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**REIMPOSTAZIONE DEL DISPOSITIVO EVENTI WPD \_ \_ \_**</dt> </dl>                                               | Questo evento indica che il dispositivo sta per essere reimpostato e che tutti i client connessi devono chiudere le connessioni al dispositivo.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**AGGIUNTA DELL'OGGETTO EVENTO WPD \_ \_ \_**</dt> </dl>                                               | Questo evento indica che un nuovo oggetto è disponibile nel dispositivo.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**OGGETTO EVENTO WPD \_ \_ \_ RIMOSSO**</dt> </dl>                                         | Questo evento viene inviato dopo che un oggetto esistente in precedenza è stato rimosso dal dispositivo.<br/> L'oggetto potrebbe essere un oggetto contenuto, ad esempio un file di immagine è stato eliminato. o potrebbe essere un oggetto funzionale, ad esempio un nuovo dispositivo di archiviazione scollegato dal dispositivo.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**TRASFERIMENTO DI OGGETTI EVENTO WPD \_ \_ \_ \_ RICHIESTO**</dt> </dl>       | Questo evento viene inviato per richiedere a un'applicazione di trasferire un determinato oggetto dal dispositivo.<br/> L'oggetto è in genere un oggetto contenuto, ad esempio un file di immagine.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**OGGETTO EVENTO WPD \_ \_ \_ AGGIORNATO**</dt> </dl>                                         | Questo evento viene inviato dopo l'aggiornamento di un oggetto e qualsiasi client connesso deve aggiornare la visualizzazione dell'oggetto.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**METODO DEL SERVIZIO EVENTI WPD \_ \_ \_ \_ COMPLETATO**</dt> </dl>             | Questo evento viene inviato quando un driver ha completato la chiamata di un metodo del servizio. Questo evento deve essere inviato anche quando il metodo ha esito negativo. Si tratta di un evento DDI WPD interno e non sarà disponibile per alcuna applicazione tramite [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) o [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**FORMATO DI ARCHIVIAZIONE EVENTI WPD \_ \_ \_**</dt> </dl>                                         | Questo evento indica lo stato di avanzamento di un'operazione di formattazione su un oggetto di archiviazione.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
</dt> </dl>

 

 




