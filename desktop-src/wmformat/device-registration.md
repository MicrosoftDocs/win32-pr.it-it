---
title: Registrazione del dispositivo
description: Registrazione del dispositivo
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK, registrazione del dispositivo
- Windows Media Format SDK, registrazione dei dispositivi
- ASF (Advanced Systems Format), registrazione del dispositivo
- ASF (formato avanzato dei sistemi), registrazione del dispositivo
- ASF (Advanced Systems Format), registrazione dei dispositivi
- ASF (Advanced Systems Format), registrazione dei dispositivi
- Digital Rights Management (DRM), registrazione del dispositivo
- DRM (Digital Rights Management), registrazione del dispositivo
- Digital Rights Management (DRM), registrazione dei dispositivi
- DRM (Digital Rights Management), registrazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046306"
---
# <a name="device-registration"></a><span data-ttu-id="f4f15-113">Registrazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f4f15-113">Device Registration</span></span>

<span data-ttu-id="f4f15-114">Windows Media Format SDK consente di accedere al database di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4f15-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="f4f15-115">Questo database è protetto nel computer client e viene usato per registrare i dispositivi che supportano Windows Media DRM 10 per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="f4f15-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="f4f15-116">Quando un dispositivo viene aggiunto a una rete a cui è connesso il computer client, il dispositivo tenta di contattare un'applicazione di trasmissione di Windows Media DRM 10 per dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="f4f15-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="f4f15-117">Dopo aver stabilito le comunicazioni, il dispositivo invia un messaggio di richiesta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f4f15-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="f4f15-118">Quando riceve un messaggio di richiesta di registrazione, l'applicazione deve eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4f15-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="f4f15-119">Analizzare il messaggio chiamando il metodo [**IWMDRMMessageParser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) .</span><span class="sxs-lookup"><span data-stu-id="f4f15-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="f4f15-120">Questo metodo recupera il certificato del dispositivo e il numero di serie del dispositivo, entrambi necessari per identificare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4f15-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="f4f15-121">Chiamare il metodo [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , passando il numero di serie del certificato e del dispositivo recuperato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="f4f15-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="f4f15-122">Se il dispositivo viene trovato, è già registrato ed è possibile ignorare il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="f4f15-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="f4f15-123">Chiamare il metodo [**IWMDeviceRegistration:: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) per aggiungere il dispositivo al database di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4f15-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="f4f15-124">Per accedere alle informazioni relative a qualsiasi dispositivo nel database di registrazione, è possibile recuperare l'oggetto dispositivo registrato associato.</span><span class="sxs-lookup"><span data-stu-id="f4f15-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="f4f15-125">Esistono due modi per ottenere un oggetto dispositivo registrato.</span><span class="sxs-lookup"><span data-stu-id="f4f15-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="f4f15-126">Se il certificato e il numero di serie del dispositivo sono disponibili, è possibile chiamare il metodo [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) .</span><span class="sxs-lookup"><span data-stu-id="f4f15-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="f4f15-127">Se il certificato e il numero di serie del dispositivo non sono disponibili, è possibile enumerare tutti i dispositivi nel database chiamando [**IWMDeviceRegistration:: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguito da chiamate ripetute a [**IWMDeviceRegistration:: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) fino a quando una chiamata non restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="f4f15-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="f4f15-128">Prima che l'applicazione possa inviare dati a un dispositivo, è necessario assicurarsi che il dispositivo sia approvato, convalidato e aperto.</span><span class="sxs-lookup"><span data-stu-id="f4f15-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="f4f15-129">L'approvazione del dispositivo deve coinvolgere l'interazione con l'utente.</span><span class="sxs-lookup"><span data-stu-id="f4f15-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="f4f15-130">Quando un dispositivo invia un messaggio di registrazione, l'applicazione può chiedere all'utente di decidere se il dispositivo è quello che dovrebbe ricevere i dati dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f4f15-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="f4f15-131">Aggiornare quindi il database di registrazione del dispositivo chiamando il metodo [**IWMRegisteredDevice:: approv**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , passando **true** o **false** nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="f4f15-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="f4f15-132">La convalida è detta anche rilevamento della prossimità.</span><span class="sxs-lookup"><span data-stu-id="f4f15-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="f4f15-133">Si tratta di un processo mediante il quale gli oggetti DRM interni di Windows Media Format SDK determinano se il dispositivo è sufficientemente "vicino" al computer che esegue l'applicazione per la trasmissione sicura dei supporti.</span><span class="sxs-lookup"><span data-stu-id="f4f15-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="f4f15-134">La prossimità è determinata dal tempo necessario per ottenere una risposta a un messaggio.</span><span class="sxs-lookup"><span data-stu-id="f4f15-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="f4f15-135">Questa funzionalità è destinata a impedire a utenti non autorizzati di accedere alla rete e di ottenere il supporto protetto.</span><span class="sxs-lookup"><span data-stu-id="f4f15-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="f4f15-136">Per ulteriori informazioni, vedere [esecuzione del rilevamento della prossimità](performing-proximity-detection.md).</span><span class="sxs-lookup"><span data-stu-id="f4f15-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="f4f15-137">Per aprire un dispositivo, chiamare [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span><span class="sxs-lookup"><span data-stu-id="f4f15-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="f4f15-138">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f4f15-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f4f15-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4f15-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4f15-140">**IWMRegisteredDevice**</span><span class="sxs-lookup"><span data-stu-id="f4f15-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="f4f15-141">**Uso del protocollo Windows Media DRM 10 per i dispositivi di rete**</span><span class="sxs-lookup"><span data-stu-id="f4f15-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




