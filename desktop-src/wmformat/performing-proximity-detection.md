---
title: Esecuzione del rilevamento della prossimità
description: Esecuzione del rilevamento della prossimità
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media Format SDK, esecuzione del rilevamento della prossimità
- Windows Media Format SDK, rilevamento della prossimità
- Advanced Systems Format (ASF), esecuzione del rilevamento della prossimità
- ASF (Advanced Systems Format), esecuzione del rilevamento della prossimità
- Advanced Systems Format (ASF), rilevamento prossimità
- ASF (formato avanzato dei sistemi), rilevamento della prossimità
- Digital Rights Management (DRM), esecuzione del rilevamento della prossimità
- DRM (Digital Rights Management), esecuzione del rilevamento della prossimità
- Digital Rights Management (DRM), rilevamento prossimità
- DRM (Digital Rights Management), rilevamento della prossimità
- rilevamento della prossimità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398534"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="32bf0-114">Esecuzione del rilevamento della prossimità</span><span class="sxs-lookup"><span data-stu-id="32bf0-114">Performing Proximity Detection</span></span>

<span data-ttu-id="32bf0-115">Prima di poter trasmettere i dati crittografati a un dispositivo registrato nel protocollo Windows Media DRM 10 per i dispositivi di rete, è necessario eseguire un processo denominato rilevamento della prossimità (chiamato anche convalida).</span><span class="sxs-lookup"><span data-stu-id="32bf0-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="32bf0-116">Questo processo comporta l'invio di messaggi al dispositivo e la ricezione delle risposte.</span><span class="sxs-lookup"><span data-stu-id="32bf0-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="32bf0-117">Il tempo necessario per ricevere una risposta viene usato per determinare se il dispositivo è sufficientemente vicino al computer della rete per ricevere dati protetti.</span><span class="sxs-lookup"><span data-stu-id="32bf0-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="32bf0-118">Verificare che il dispositivo sia fisicamente vicino al computer client nella rete consente di impedire lo spoofing e altri accessi non autorizzati.</span><span class="sxs-lookup"><span data-stu-id="32bf0-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="32bf0-119">Quando il rilevamento della prossimità viene completato correttamente, il dispositivo viene definito valido.</span><span class="sxs-lookup"><span data-stu-id="32bf0-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="32bf0-120">È possibile verificare se un dispositivo è valido chiamando il metodo [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) .</span><span class="sxs-lookup"><span data-stu-id="32bf0-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="32bf0-121">I dispositivi devono essere convalidati ogni 48 ore.</span><span class="sxs-lookup"><span data-stu-id="32bf0-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="32bf0-122">Un dispositivo che è stato convalidato più di 48 ore prima dell'esecuzione del programma deve essere riconvalidato eseguendo di nuovo il processo di rilevamento della prossimità.</span><span class="sxs-lookup"><span data-stu-id="32bf0-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="32bf0-123">Per eseguire il rilevamento della prossimità, è necessario stabilire le comunicazioni con il dispositivo e quindi chiamare il metodo [**IWMProximityDetection:: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) .</span><span class="sxs-lookup"><span data-stu-id="32bf0-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="32bf0-124">Il processo di rilevamento viene completato in modo asincrono dai componenti DRM interni di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="32bf0-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="32bf0-125">L'applicazione deve includere un'implementazione dell'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) per elaborare i messaggi di rilevamento prossimità.</span><span class="sxs-lookup"><span data-stu-id="32bf0-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="32bf0-126">Il processo di rilevamento della prossimità invia due messaggi: un messaggio di risultato e un messaggio di completamento.</span><span class="sxs-lookup"><span data-stu-id="32bf0-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="32bf0-127">Al \_ \_ termine del processo di rilevamento, viene inviato il messaggio di risultato WMT di prossimità.</span><span class="sxs-lookup"><span data-stu-id="32bf0-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="32bf0-128">Il parametro *HR* del metodo di callback [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica se il dispositivo è stato trovato abbastanza vicino al computer client.</span><span class="sxs-lookup"><span data-stu-id="32bf0-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="32bf0-129">Se il parametro *HR* del messaggio di risultato indica esito positivo, il parametro *PValue* contiene un **valore DWORD** che specifica la latenza misurata al dispositivo in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="32bf0-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="32bf0-130">Il messaggio di completamento, \_ prossimità WMT \_ completata, viene inviato quando il rilevamento viene finalizzato.</span><span class="sxs-lookup"><span data-stu-id="32bf0-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="32bf0-131">È consigliabile rilasciare l'interfaccia [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) solo dopo la ricezione di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="32bf0-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="32bf0-132">Quando il rilevamento della prossimità per un dispositivo ha esito positivo, il database di registrazione del dispositivo viene aggiornato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="32bf0-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="32bf0-133">Le chiamate successive a [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) restituiscono **true** fino a quando non sono trascorse 48 ore e il dispositivo deve essere riconvalidato.</span><span class="sxs-lookup"><span data-stu-id="32bf0-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="32bf0-134">**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="32bf0-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32bf0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32bf0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32bf0-136">**Uso del protocollo Windows Media DRM 10 per i dispositivi di rete**</span><span class="sxs-lookup"><span data-stu-id="32bf0-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




