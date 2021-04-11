---
description: Un'applicazione può rifiutare esplicitamente l'esperienza di ducking predefinita gestita dal sistema e sostituirla con un'implementazione personalizzata.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fornire un comportamento di ducking personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127426"
---
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="04230-103">Fornire un comportamento di ducking personalizzato</span><span class="sxs-lookup"><span data-stu-id="04230-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="04230-104">Un'applicazione può rifiutare esplicitamente l' [esperienza di ducking predefinita](stream-attenuation.md) gestita dal sistema e sostituirla con un'implementazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="04230-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="04230-105">Un'applicazione può offrire un'esperienza di ducking personalizzata.</span><span class="sxs-lookup"><span data-stu-id="04230-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="04230-106">Ad esempio, Windows Media Player fornisce una propria esperienza di ducking sospendendo il flusso multimediale corrente durante una sessione di comunicazione e riprendendo la riproduzione quando la sessione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="04230-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="04230-107">Con Windows SDK esempi è inclusa un'applicazione multimediale di esempio che implementa ducking; Per ulteriori informazioni, vedere [DuckingMediaPlayer](duckingmediaplayer.md).</span><span class="sxs-lookup"><span data-stu-id="04230-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="04230-108">Per simulare l'esperienza di apertura e chiusura dei flussi di comunicazione e la generazione di eventi ducking, vedere [DuckingCaptureSample](duckingcapturesample.md), che è anche incluso in Windows SDK esempi.</span><span class="sxs-lookup"><span data-stu-id="04230-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="04230-109">Un'applicazione multimediale che riproduce i suoni da attenuare deve essere in grado di riconoscere i flussi di comunicazione, quando vengono aperti e chiusi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="04230-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="04230-110">È possibile fornire l'implementazione personalizzata usando MediaFoundation, DirectShow o DirectSound, che usano le API di base di audio.</span><span class="sxs-lookup"><span data-stu-id="04230-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="04230-111">Un client WASAPI diretto può anche eseguire l'override della gestione predefinita se sa quando inizia e termina la sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="04230-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="04230-112">**Per offrire un'esperienza di ducking personalizzata, un client WASAPI deve eseguire le attività seguenti:**</span><span class="sxs-lookup"><span data-stu-id="04230-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="04230-113">Registrarsi per ricevere eventi ducking da *ducking Manager*, un componente del sistema audio che gestisce le notifiche relative alle modifiche del flusso di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="04230-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="04230-114">Per altre informazioni, [ottenere eventi ducking](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="04230-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="04230-115">Se il client viene registrato per ricevere notifiche di ducking, il Manager di ducking Disabilita il comportamento predefinito fornito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="04230-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="04230-116">Se il comportamento predefinito è disabilitato esplicitamente (vedere [disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)) e il client non fornisce un comportamento di sostituzione, l'applicazione non ha alcun comportamento di ducking.</span><span class="sxs-lookup"><span data-stu-id="04230-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="04230-117">Ascolta le notifiche degli eventi Duck inviate da ducking Manager ed Esegui il comportamento di ducking desiderato.</span><span class="sxs-lookup"><span data-stu-id="04230-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="04230-118">Per altre informazioni sull'implementazione di un comportamento di ducking, vedere [considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="04230-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04230-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04230-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04230-120">Uso di un dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="04230-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="04230-121">Esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="04230-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="04230-122">Disabilitazione dell'esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="04230-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="04230-123">Considerazioni sull'implementazione per le notifiche di ducking</span><span class="sxs-lookup"><span data-stu-id="04230-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="04230-124">Recupero di eventi ducking</span><span class="sxs-lookup"><span data-stu-id="04230-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



