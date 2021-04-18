---
title: Oggetto registrazione dispositivo
description: Oggetto registrazione dispositivo
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK, oggetti registrazione dispositivo
- ASF (Advanced Systems Format), oggetti di registrazione del dispositivo
- ASF (Advanced Systems Format), oggetti di registrazione del dispositivo
- oggetti, oggetti di registrazione del dispositivo
- oggetti di registrazione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299409"
---
# <a name="device-registration-object"></a><span data-ttu-id="8ca4d-108">Oggetto registrazione dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ca4d-108">Device Registration Object</span></span>

<span data-ttu-id="8ca4d-109">L'oggetto registrazione dispositivo gestisce il database di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="8ca4d-110">In questo database vengono archiviate le informazioni sui dispositivi di rete, ad esempio i lettori video di set-top, che sono connessi al computer client.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="8ca4d-111">Lo scopo principale del database di registrazione del dispositivo è quello di gestire i dispositivi che usano il protocollo Windows Media DRM 10 per i dispositivi di rete per la ricezione di flussi di dati protetti.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="8ca4d-112">Se l'applicazione supporta Windows Media DRM 10 per i dispositivi di rete, è necessario utilizzare le interfacce di questo oggetto per registrare i dispositivi di rete e per convalidare tali dispositivi.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="8ca4d-113">È anche possibile usare il database di registrazione del dispositivo per archiviare le informazioni sui dispositivi di rete che non usano Windows Media DRM 10 per i dispositivi di rete, anche se non tutte le informazioni presenti nel database verranno applicate a tali dispositivi.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="8ca4d-114">L'oggetto registrazione del dispositivo viene creato dalla funzione [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , che imposta un puntatore a un'interfaccia **IWMDeviceRegistration** .</span><span class="sxs-lookup"><span data-stu-id="8ca4d-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="8ca4d-115">Gli altri metodi dell'oggetto registrazione del dispositivo possono essere ottenuti chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="8ca4d-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="8ca4d-116">Le interfacce seguenti sono supportate dall'oggetto registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="8ca4d-117">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8ca4d-117">Interface</span></span>                                              | <span data-ttu-id="8ca4d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca4d-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="8ca4d-119">**IWMDeviceRegistration**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="8ca4d-120">Gestisce il database di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="8ca4d-121">**IWMDRMMessageParser**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="8ca4d-122">Analizza i messaggi inviati dai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="8ca4d-123">**IWMProximityDetection**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="8ca4d-124">Gestisce la convalida del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="8ca4d-125">L'interfaccia di callback seguente deve essere implementata dall'applicazione per usare i metodi dell'interfaccia **IWMProximityDetection** .</span><span class="sxs-lookup"><span data-stu-id="8ca4d-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="8ca4d-126">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8ca4d-126">Interface</span></span>                                      | <span data-ttu-id="8ca4d-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca4d-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="8ca4d-128">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="8ca4d-129">Riceve i messaggi di stato dai processi eseguiti in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="8ca4d-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8ca4d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ca4d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ca4d-131">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




