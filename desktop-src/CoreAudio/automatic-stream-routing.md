---
description: Questo articolo descrive come aggiornare un'implementazione di WASAPI per sfruttare i vantaggi del routing automatico dei flussi.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Routing automatico del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966339"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="894ea-103">Routing automatico del flusso</span><span class="sxs-lookup"><span data-stu-id="894ea-103">Automatic Stream Routing</span></span>

<span data-ttu-id="894ea-104">Questo articolo descrive come aggiornare un'implementazione di WASAPI per sfruttare i vantaggi del routing automatico dei flussi.</span><span class="sxs-lookup"><span data-stu-id="894ea-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="894ea-105">A partire da Windows 7, ogni volta che viene modificato il dispositivo audio predefinito, il flusso di riproduzione audio di un'app viene trasferito senza interruzioni dal dispositivo audio predefinito precedente al nuovo dispositivo audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="894ea-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="894ea-106">Questo trasferimento viene eseguito automaticamente senza codice dell'applicazione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="894ea-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="894ea-107">Tuttavia, prima di Windows 10, versione 1607, le app che usavano l'API di sessione audio di Windows di basso livello (WASAPI) non potevano partecipare a questa funzionalità di routing automatico dei flussi.</span><span class="sxs-lookup"><span data-stu-id="894ea-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="894ea-108">Le app che usano WASAPI sono necessarie per implementare il proprio modulo di routing del flusso aggiungendo codice aggiuntivo per rilevare l'arrivo e la rimozione di dispositivi audio e passare il flusso a tali dispositivi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="894ea-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="894ea-109">Le applicazioni che usano WASAPI che non implementano il proprio meccanismo di routing del flusso all'arrivo o alla rimozione del dispositivo rischiano di offrire un'esperienza utente inferiore a quella ideale.</span><span class="sxs-lookup"><span data-stu-id="894ea-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="894ea-110">A partire da Windows 10, versione 1607, le app che usano WASAPI possono sfruttare il routing automatico dei flussi.</span><span class="sxs-lookup"><span data-stu-id="894ea-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="894ea-111">Se l'applicazione usa WASAPI, è consigliabile aggiornare l'applicazione per sfruttare questa nuova funzionalità attenendosi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="894ea-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="894ea-112">Windows 10, versione 1607, definisce due nuovi GUID che possono essere usati per attivare un'interfaccia di rendering o acquisizione audio con routing automatico dei flussi [, \_ \_ rendering audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids) e [ \_ \_ acquisizione audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span><span class="sxs-lookup"><span data-stu-id="894ea-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="894ea-113">Ottenere una rappresentazione di stringa di questi GUID chiamando [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span><span class="sxs-lookup"><span data-stu-id="894ea-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="894ea-114">Nell'esempio seguente viene illustrata questa chiamata per il GUID di rendering audio.</span><span class="sxs-lookup"><span data-stu-id="894ea-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="894ea-115">Attivare l'endpoint audio passando la stringa dell'identificatore alla funzione WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) .</span><span class="sxs-lookup"><span data-stu-id="894ea-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="894ea-116">Nell'esempio seguente l'identificatore di rendering audio ottenuto nel passaggio 1 viene passato:</span><span class="sxs-lookup"><span data-stu-id="894ea-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="894ea-117">Liberare la memoria allocata per contenere l'identificatore dell'endpoint:</span><span class="sxs-lookup"><span data-stu-id="894ea-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="894ea-118">Dopo aver modificato l'app per attivare l'interfaccia audio nel modo descritto in precedenza, parteciperà alla funzionalità di routing automatico dei flussi.</span><span class="sxs-lookup"><span data-stu-id="894ea-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="894ea-119">Per illustrare il routing automatico dei flussi, usare un portatile o un tablet dotato di altoparlanti interni per riprodurre l'audio.</span><span class="sxs-lookup"><span data-stu-id="894ea-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="894ea-120">È necessario ascoltare la riproduzione audio degli altoparlanti interni del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="894ea-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="894ea-121">Durante la riproduzione dell'audio, connettere una coppia di cuffie.</span><span class="sxs-lookup"><span data-stu-id="894ea-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="894ea-122">A questo punto si dovrebbe ascoltare la riproduzione audio attraverso le cuffie.</span><span class="sxs-lookup"><span data-stu-id="894ea-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="894ea-123">Quindi, scollegare le cuffie e audio deve essere indirizzato automaticamente ai relatori interni.</span><span class="sxs-lookup"><span data-stu-id="894ea-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="894ea-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="894ea-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="894ea-125">Routing del flusso</span><span class="sxs-lookup"><span data-stu-id="894ea-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="894ea-126">**MediaDevice.GetDefaultAudioRenderId**</span><span class="sxs-lookup"><span data-stu-id="894ea-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="894ea-127">**MediaDevice.GetDefaultAudioCaptureId**</span><span class="sxs-lookup"><span data-stu-id="894ea-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="894ea-128">**ActivateAudioInterfaceAsync**</span><span class="sxs-lookup"><span data-stu-id="894ea-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
