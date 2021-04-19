---
description: I dispositivi portatili Windows supportano le seguenti proprietà dell'evento.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Proprietà evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333528"
---
# <a name="event-properties"></a><span data-ttu-id="3579a-103">Proprietà dell'evento</span><span class="sxs-lookup"><span data-stu-id="3579a-103">Event Properties</span></span>

<span data-ttu-id="3579a-104">I dispositivi portatili Windows supportano le seguenti proprietà dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3579a-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3579a-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3579a-105">Property</span></span></th>
<th><span data-ttu-id="3579a-106">VarType</span><span class="sxs-lookup"><span data-stu-id="3579a-106">VarType</span></span></th>
<th><span data-ttu-id="3579a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3579a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3579a-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="3579a-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="3579a-110">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="3579a-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3579a-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="3579a-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="3579a-113">Valore booleano che specifica se l'evento viene trasmesso a tutti i client. I client possono ricevere questo evento registrando il callback con <strong>IPortableDevice:: Advise</strong>.</span><span class="sxs-lookup"><span data-stu-id="3579a-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3579a-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="3579a-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="3579a-116">Valore booleano che specifica se la gerarchia figlio per l'oggetto è stata modificata. Questo parametro viene utilizzato per notificare al chiamante che alcuni elementi figlio per l'oggetto specificato sono stati aggiunti o rimossi.</span><span class="sxs-lookup"><span data-stu-id="3579a-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="3579a-117">In genere, la modifica della gerarchia viene avviata sul lato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3579a-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="3579a-118">È possibile che i client debbano enumerare di nuovo gli elementi figlio della cartella per mantengono aggiornate le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="3579a-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3579a-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="3579a-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="3579a-121">Valore che identifica un evento.</span><span class="sxs-lookup"><span data-stu-id="3579a-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3579a-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="3579a-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3579a-124">Il cookie viene restituito a un client quando richiede la creazione di un oggetto chiamando il metodo <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent:: CreateObjectWithPropertiesAndData</strong></a> . Questo parametro viene aggiunto come praticità per consentire al chiamante di associare un evento aggiunto a un oggetto alla richiesta inviata per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3579a-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="3579a-125">Il driver consegna il cookie come valore restituito <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> durante l'elaborazione del comando di <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .</span><span class="sxs-lookup"><span data-stu-id="3579a-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3579a-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="3579a-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3579a-128">Valore che identifica in modo univoco l'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="3579a-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="3579a-129">Questa proprietà è simile a <strong>WPD_OBJECT_PARENT_ID</strong>, ma questo ID non cambia tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="3579a-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3579a-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="3579a-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="3579a-132">Valore che specifica lo stato di avanzamento di un'operazione attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3579a-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="3579a-133">Il valore di questa proprietà può variare da 0 a 100, con 100 che indica che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3579a-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3579a-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="3579a-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="3579a-136">Valore che indica lo stato corrente dell'operazione, ad esempio avviato, in esecuzione, arrestato e così via. I valori possibili di questo parametro sono delineati dall'enumerazione <strong>WPD_OPERATION_STATES</strong> definita in portabledevice. h.</span><span class="sxs-lookup"><span data-stu-id="3579a-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="3579a-137">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="3579a-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="3579a-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="3579a-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="3579a-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="3579a-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="3579a-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="3579a-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="3579a-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3579a-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="3579a-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3579a-147">Valore che specifica il dispositivo che ha originato l'evento. Si tratta dell'identificatore del dispositivo o del servizio fornito dal sistema plug-and-Play (PnP) ed è la stessa stringa utilizzata nei metodi <strong>IPortableDevice:: Open</strong>o <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService:: Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3579a-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3579a-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="3579a-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3579a-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3579a-150">Stringa utilizzata da un driver WPD per identificare l'operazione di un metodo del servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3579a-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="3579a-151">Le applicazioni non devono usare questo parametro direttamente.</span><span class="sxs-lookup"><span data-stu-id="3579a-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3579a-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3579a-152">Requirements</span></span>



| <span data-ttu-id="3579a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="3579a-153">Requirement</span></span> | <span data-ttu-id="3579a-154">Valore</span><span class="sxs-lookup"><span data-stu-id="3579a-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3579a-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3579a-155">Header</span></span><br/> | <dl> <span data-ttu-id="3579a-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3579a-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3579a-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3579a-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3579a-158">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="3579a-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




