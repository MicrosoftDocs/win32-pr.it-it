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
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="9e308-103">Costanti di evento (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="9e308-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="9e308-104">I dispositivi portatili Windows definiscono i valori di evento seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e308-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="9e308-105">Costante</span><span class="sxs-lookup"><span data-stu-id="9e308-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="9e308-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e308-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="9e308-107"><dt>**\_funzionalità del \_ dispositivo evento WPD \_ \_ aggiornate**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="9e308-108">Questo evento indica che le funzionalità del dispositivo sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="9e308-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="9e308-109">I client devono eseguire una query sul dispositivo se hanno preso decisioni in base alle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e308-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="9e308-110"><dt>**\_dispositivo evento \_ WPD \_ rimosso**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="9e308-111">Questo evento viene inviato quando viene scaricato un driver per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e308-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="9e308-112">In genere si tratta di un risultato del dispositivo scollegato.</span><span class="sxs-lookup"><span data-stu-id="9e308-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="9e308-113">I client devono rilasciare l'interfaccia **IPortableDevice** e tutte le interfacce [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) specificate nel **parametro dell' \_ evento WPD \_ \_ \_ \_ ID del dispositivo PNP**.</span><span class="sxs-lookup"><span data-stu-id="9e308-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="9e308-114"><dt>**reimpostazione del \_ dispositivo evento WPD \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="9e308-115">Questo evento indica che il dispositivo sta per essere reimpostato e che tutti i client connessi devono chiudere le connessioni al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e308-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="9e308-116"><dt>**\_oggetto evento \_ WPD \_ aggiunto**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="9e308-117">Questo evento indica che nel dispositivo è disponibile un nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e308-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="9e308-118"><dt>**\_oggetto evento \_ WPD \_ rimosso**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="9e308-119">Questo evento viene inviato dopo la rimozione di un oggetto precedentemente esistente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e308-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="9e308-120">L'oggetto potrebbe essere un oggetto contenuto, ad esempio un file di immagine è stato eliminato. oppure potrebbe trattarsi di un oggetto funzionale, ad esempio un nuovo dispositivo di archiviazione è stato scollegato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e308-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="9e308-121"><dt>**è \_ stato \_ \_ richiesto il trasferimento dell'oggetto evento WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="9e308-122">Questo evento viene inviato per richiedere a un'applicazione di trasferire un oggetto specifico dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e308-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="9e308-123">L'oggetto è in genere un oggetto contenuto, ad esempio un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="9e308-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="9e308-124"><dt>**\_oggetto evento \_ WPD \_ aggiornato**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="9e308-125">Questo evento viene inviato dopo l'aggiornamento di un oggetto e qualsiasi client connesso deve aggiornare la visualizzazione di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e308-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="9e308-126"><dt>**\_metodo del \_ servizio eventi WPD \_ \_ completato**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="9e308-127">Questo evento viene inviato quando un driver ha completato la chiamata a un metodo del servizio.</span><span class="sxs-lookup"><span data-stu-id="9e308-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="9e308-128">Questo evento deve essere inviato anche quando il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9e308-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="9e308-129">Si tratta di un evento di DDI WPD interno e non sarà disponibile per le applicazioni tramite [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) o [**IPortableDeviceService:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span><span class="sxs-lookup"><span data-stu-id="9e308-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="9e308-130"><dt>**\_formato di \_ archiviazione \_ eventi WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="9e308-131">Questo evento indica lo stato di un'operazione di formattazione su un oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e308-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="9e308-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e308-132">Requirements</span></span>



| <span data-ttu-id="9e308-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e308-133">Requirement</span></span> | <span data-ttu-id="9e308-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9e308-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e308-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e308-135">Header</span></span><br/> | <dl> <span data-ttu-id="9e308-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e308-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e308-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e308-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e308-138">Costanti</span><span class="sxs-lookup"><span data-stu-id="9e308-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




