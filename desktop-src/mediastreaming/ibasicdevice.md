---
title: Interfaccia IBasicDevice
description: Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API di streaming multimediale dell'interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, descritta
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399915"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="60012-105">Interfaccia IBasicDevice</span><span class="sxs-lookup"><span data-stu-id="60012-105">IBasicDevice interface</span></span>

<span data-ttu-id="60012-106">Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="60012-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="60012-107">Membri</span><span class="sxs-lookup"><span data-stu-id="60012-107">Members</span></span>

<span data-ttu-id="60012-108">L'interfaccia **IBasicDevice** eredita da [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="60012-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="60012-109">**IBasicDevice** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="60012-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="60012-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="60012-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60012-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="60012-111">Methods</span></span>

<span data-ttu-id="60012-112">L'interfaccia **IBasicDevice** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="60012-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="60012-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="60012-113">Method</span></span>                                                                                 | <span data-ttu-id="60012-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60012-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60012-115">**Aggiungi \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="60012-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="60012-116">Registra un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="60012-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="60012-117">**CanWakeDevices**</span><span class="sxs-lookup"><span data-stu-id="60012-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="60012-118">Recupera un valore che indica se il dispositivo può essere riattivato.</span><span class="sxs-lookup"><span data-stu-id="60012-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="60012-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60012-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="60012-120">Restituisce un valore di enumerazione che indica se il dispositivo è attualmente in linea, non in linea o in sospensione ma riattivabile.</span><span class="sxs-lookup"><span data-stu-id="60012-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="60012-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="60012-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="60012-122">Recupera una descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="60012-123">**DiscoveredOnCurrentNetwork**</span><span class="sxs-lookup"><span data-stu-id="60012-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="60012-124">Recupera un valore che indica se il dispositivo si trova nella rete corrente.</span><span class="sxs-lookup"><span data-stu-id="60012-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="60012-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="60012-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="60012-126">Recupera il nome descrittivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="60012-127">**Icone**</span><span class="sxs-lookup"><span data-stu-id="60012-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="60012-128">Restituisce un vettore di interfacce [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="60012-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="60012-129">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="60012-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="60012-130">Restituisce un vettore di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="60012-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="60012-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="60012-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="60012-132">Recupera il nome del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="60012-133">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="60012-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="60012-134">Recupera l'URL del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="60012-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="60012-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="60012-136">Recupera il nome del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="60012-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="60012-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="60012-138">Recupera il numero di modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="60012-139">**ModelUrl**</span><span class="sxs-lookup"><span data-stu-id="60012-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="60012-140">Recupera l'URL del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="60012-141">**PhysicalAddresses**</span><span class="sxs-lookup"><span data-stu-id="60012-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="60012-142">Restituisce un vettore di indirizzi fisici.</span><span class="sxs-lookup"><span data-stu-id="60012-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="60012-143">**PresentationUrl**</span><span class="sxs-lookup"><span data-stu-id="60012-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="60012-144">Recupera l'URL di presentazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="60012-145">**RemoteStreamingUrls**</span><span class="sxs-lookup"><span data-stu-id="60012-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="60012-146">Restituisce un vettore di URL di streaming remoto.</span><span class="sxs-lookup"><span data-stu-id="60012-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="60012-147">**rimuovere \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="60012-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="60012-148">Annulla la registrazione di un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="60012-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="60012-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="60012-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="60012-150">Recupera il numero di serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60012-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="60012-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="60012-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="60012-152">Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="60012-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="60012-153">**UniqueDeviceName**</span><span class="sxs-lookup"><span data-stu-id="60012-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="60012-154">Recupera il nome del dispositivo univoco del dispositivo (UDN).</span><span class="sxs-lookup"><span data-stu-id="60012-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="60012-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60012-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60012-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="60012-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

