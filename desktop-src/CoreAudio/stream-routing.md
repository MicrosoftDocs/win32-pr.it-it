---
description: Il routing del flusso è la capacità di un'applicazione multimediale di cambiare i flussi tra i dispositivi con interruzioni minime della riproduzione o della sessione di acquisizione.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Routing del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483461"
---
# <a name="stream-routing"></a><span data-ttu-id="2667a-103">Routing del flusso</span><span class="sxs-lookup"><span data-stu-id="2667a-103">Stream Routing</span></span>

<span data-ttu-id="2667a-104">Il *routing del flusso* è la capacità di un'applicazione multimediale di cambiare i flussi tra i dispositivi con interruzioni minime della riproduzione o della sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2667a-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="2667a-105">Un computer può avere più dispositivi di rendering e acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2667a-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="2667a-106">Il sistema elenca questi dispositivi nel pannello di controllo **suoni** .</span><span class="sxs-lookup"><span data-stu-id="2667a-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="2667a-107">Da questo elenco, un utente può impostare un dispositivo come il dispositivo predefinito per ogni ruolo: riproduzione, registrazione o quattro ruoli di comunicazione (rendering della console, acquisizione della console, rendering della comunicazione o acquisizione delle comunicazioni).</span><span class="sxs-lookup"><span data-stu-id="2667a-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="2667a-108">L'elenco dei dispositivi può essere modificato dinamicamente perché alcuni di questi dispositivi possono essere temporaneamente disponibili, ad esempio una cuffia USB.</span><span class="sxs-lookup"><span data-stu-id="2667a-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="2667a-109">Quando sono disponibili più dispositivi, l'utente può modificare il valore predefinito in un dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="2667a-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="2667a-110">L'utente può anche modificare il formato di un dispositivo (frequenza di campionamento, BITS per esempio e così via) nella scheda **Avanzate** per le proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2667a-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="2667a-111">Si consideri uno scenario in cui un utente seleziona gli **altoparlanti** come dispositivo predefinito per il rendering dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="2667a-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="2667a-112">L'utente connette quindi una cuffia USB, seleziona l'auricolare come nuovo dispositivo predefinito e modifica la frequenza di campionamento del dispositivo da 44,1 kHz a 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="2667a-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="2667a-113">L'utente vuole riprodurre il flusso audio nell'auricolare alla nuova frequenza di campionamento con un'interruzione minima della sessione di streaming.</span><span class="sxs-lookup"><span data-stu-id="2667a-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="2667a-114">In questo scenario, è necessario che l'applicazione multimediale gestisca due casi:</span><span class="sxs-lookup"><span data-stu-id="2667a-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="2667a-115">Il flusso deve essere trasferito al nuovo dispositivo predefinito con interruzioni minime per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2667a-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="2667a-116">Il nuovo dispositivo deve riprendere la riproduzione nel nuovo formato (ovvero, l'utente può modificare una frequenza superiore a quella di campionamento).</span><span class="sxs-lookup"><span data-stu-id="2667a-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="2667a-117">In Windows Vista, per supportare questo scenario, l'applicazione multimediale doveva fornire l'implementazione per il routing del flusso.</span><span class="sxs-lookup"><span data-stu-id="2667a-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="2667a-118">L'applicazione è stata responsabile della terminazione dei flussi esistenti e del riavvio dei flussi nel nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2667a-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="2667a-119">Se l'utente ha modificato il dispositivo predefinito o il formato di combinazione modificato, tutte le sessioni associate sono state chiuse e l'applicazione doveva gestire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="2667a-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="2667a-120">In Windows 7, un'applicazione può trasferire facilmente un flusso da un dispositivo predefinito esistente a un nuovo endpoint audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="2667a-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="2667a-121">I set di API audio di alto livello, come Media Foundation, DirectSound e le API WAVE, implementano la funzionalità di routing dei flussi.</span><span class="sxs-lookup"><span data-stu-id="2667a-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="2667a-122">Le applicazioni multimediali che usano questi set di API per riprodurre o acquisire un flusso dal dispositivo predefinito usano l'implementazione predefinita e non dovranno modificare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2667a-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="2667a-123">Tuttavia, se l'applicazione multimediale USA direttamente MMDeviceAPI o WASAPI, l'applicazione deve fornire l'implementazione del routing del flusso.</span><span class="sxs-lookup"><span data-stu-id="2667a-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="2667a-124">MMDeviceAPI e WASAPI sono componenti dell'API audio Core che possono essere usati da un'applicazione per eseguire il rendering o l'acquisizione di un flusso in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2667a-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="2667a-125">Il MMDeviceAPI individua il nuovo dispositivo dell'endpoint audio e WASAPI gestisce il flusso di dati audio tra un'applicazione multimediale e il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="2667a-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="2667a-126">Per implementare la funzionalità di routing del flusso, l'applicazione deve restare in ascolto delle notifiche inviate da MMDeviceAPI e WASAPI nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2667a-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="2667a-127">Il dispositivo predefinito viene modificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2667a-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="2667a-128">Il dispositivo predefinito esistente viene rimosso e viene aggiunto un nuovo dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="2667a-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="2667a-129">Il formato del dispositivo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="2667a-129">The device format is changed.</span></span>

<span data-ttu-id="2667a-130">Gestendo queste notifiche, un'applicazione può eseguire le operazioni di gestione del flusso necessarie durante il trasferimento del flusso al nuovo dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="2667a-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="2667a-131">Inoltre, l'applicazione può eseguire il rendering o acquisire i flussi esistenti usando il nuovo formato specificato dall'utente mentre è attiva una sessione di rendering.</span><span class="sxs-lookup"><span data-stu-id="2667a-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="2667a-132">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="2667a-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="2667a-133">Recupero dell'endpoint del dispositivo per il routing del flusso</span><span class="sxs-lookup"><span data-stu-id="2667a-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="2667a-134">Notifiche rilevanti per il routing dei flussi</span><span class="sxs-lookup"><span data-stu-id="2667a-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="2667a-135">Considerazioni sull'implementazione del routing del flusso</span><span class="sxs-lookup"><span data-stu-id="2667a-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="2667a-136">Negli esempi seguenti, inclusi nel Windows SDK, viene illustrato il modo in cui un'applicazione è in grado di gestire le notifiche di routing del flusso.</span><span class="sxs-lookup"><span data-stu-id="2667a-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="2667a-137">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="2667a-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="2667a-138">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="2667a-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="2667a-139">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="2667a-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="2667a-140">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="2667a-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="2667a-141">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="2667a-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="2667a-142">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="2667a-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="2667a-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2667a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2667a-144">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="2667a-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="2667a-145">Informazioni sull'API MMDevice</span><span class="sxs-lookup"><span data-stu-id="2667a-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="2667a-146">Informazioni su WASAPI</span><span class="sxs-lookup"><span data-stu-id="2667a-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



