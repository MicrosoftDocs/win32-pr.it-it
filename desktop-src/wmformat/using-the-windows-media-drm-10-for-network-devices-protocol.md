---
title: Uso del protocollo Windows Media DRM 10 per i dispositivi di rete
description: Uso del protocollo Windows Media DRM 10 per i dispositivi di rete
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 per i dispositivi di rete
- Windows Media Format SDK, DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per i dispositivi di rete
- Digital Rights Management (DRM), Windows Media DRM 10 per i dispositivi di rete
- DRM (Digital Rights Management), Windows Media DRM 10 per i dispositivi di rete
- Digital Rights Management (DRM), DRM 10 per i dispositivi di rete
- DRM (Digital Rights Management), DRM 10 per i dispositivi di rete
- Windows Media DRM 10 per dispositivi di rete, protocolli
- DRM 10 per dispositivi di rete, protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329692"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a><span data-ttu-id="43b98-115">Uso del protocollo Windows Media DRM 10 per i dispositivi di rete</span><span class="sxs-lookup"><span data-stu-id="43b98-115">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>

<span data-ttu-id="43b98-116">Windows Media Format SDK fornisce alcune funzionalità per il supporto del protocollo Secure Network Device Protocol, Windows Media DRM 10 per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="43b98-116">The Windows Media Format SDK provides some features to support the secure network device protocol, Windows Media DRM 10 for Network Devices.</span></span> <span data-ttu-id="43b98-117">Questo protocollo definisce i messaggi inviati tra un dispositivo di riproduzione multimediale digitale, ad esempio un lettore video set-top, e il computer che fornisce i dati al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43b98-117">This protocol defines the messages sent between a digital media playback device, such as a set-top video player, and the computer that serves data to the device.</span></span> <span data-ttu-id="43b98-118">I dati multimediali inviati tra il server e il dispositivo vengono crittografati per proteggerli dall'intercettazione.</span><span class="sxs-lookup"><span data-stu-id="43b98-118">The media data sent between server and device is encrypted to protect it from interception.</span></span>

<span data-ttu-id="43b98-119">La comunicazione tra l'applicazione e i dispositivi che supportano Windows Media DRM 10 per i dispositivi di rete può usare tutti i protocolli di rete che preferisci.</span><span class="sxs-lookup"><span data-stu-id="43b98-119">The communication between your application and devices that support Windows Media DRM 10 for Network Devices can use whatever networking protocols you prefer.</span></span> <span data-ttu-id="43b98-120">Windows Media Format SDK non fornisce alcun oggetto che esegua le comunicazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="43b98-120">The Windows Media Format SDK does not provide any objects that perform the network communications for you.</span></span> <span data-ttu-id="43b98-121">Al contrario, gli oggetti di questo SDK elaborano i messaggi di Windows Media DRM 10 per i dispositivi di rete dopo che sono stati ricevuti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43b98-121">Instead, the objects of this SDK process some Windows Media DRM 10 for Network Devices messages after your application has received them.</span></span>

<span data-ttu-id="43b98-122">Le funzionalità che supportano Windows Media DRM 10 per i dispositivi di rete sono la registrazione del dispositivo, il rilevamento della prossimità e la conversione di file protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="43b98-122">The features that support Windows Media DRM 10 for Network Devices are device registration, proximity detection, and converting DRM-protected files.</span></span> <span data-ttu-id="43b98-123">Queste funzionalità sono descritte nelle sezioni riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="43b98-123">These features are described in the following sections.</span></span>



| <span data-ttu-id="43b98-124">Sezione</span><span class="sxs-lookup"><span data-stu-id="43b98-124">Section</span></span>                                                                                                                                                                          | <span data-ttu-id="43b98-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43b98-125">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43b98-126">Registrazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="43b98-126">Device Registration</span></span>](device-registration.md)                                                                                                                                   | <span data-ttu-id="43b98-127">Viene descritto come elaborare i messaggi di richiesta di registrazione dai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="43b98-127">Describes how to process registration request messages from devices.</span></span>                                                                       |
| [<span data-ttu-id="43b98-128">Esecuzione del rilevamento della prossimità</span><span class="sxs-lookup"><span data-stu-id="43b98-128">Performing Proximity Detection</span></span>](performing-proximity-detection.md)                                                                                                             | <span data-ttu-id="43b98-129">Descrive il processo di rilevamento della prossimità.</span><span class="sxs-lookup"><span data-stu-id="43b98-129">Describes the proximity detection process.</span></span>                                                                                                 |
| [<span data-ttu-id="43b98-130">Conversione di un file di DRM-Protected in un flusso Windows Media DRM 10 per dispositivi di rete</span><span class="sxs-lookup"><span data-stu-id="43b98-130">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | <span data-ttu-id="43b98-131">Viene descritto come convertire un file protetto da DRM in un flusso che può essere inviato a un dispositivo che usa Windows Media DRM 10 per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="43b98-131">Describes how to convert a DRM-protected file to a stream that can be sent to a device that uses Windows Media DRM 10 for Network Devices.</span></span> |



 

> [!Note]  
> <span data-ttu-id="43b98-132">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="43b98-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="43b98-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43b98-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43b98-134">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="43b98-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




