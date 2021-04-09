---
description: Informazioni sulle API audio di Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Informazioni sulle API audio di Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878338"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="6db95-103">Informazioni sulle API audio di Windows Core</span><span class="sxs-lookup"><span data-stu-id="6db95-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="6db95-104">In questa documentazione vengono fornite informazioni sulle API audio principali per la famiglia di sistemi operativi Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6db95-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="6db95-105">Le API di base audio sono state introdotte in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6db95-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="6db95-106">Si tratta di un nuovo set di componenti audio in modalità utente che offre applicazioni client con funzionalità audio migliorate.</span><span class="sxs-lookup"><span data-stu-id="6db95-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="6db95-107">Di seguito sono riportate alcune funzionalità:</span><span class="sxs-lookup"><span data-stu-id="6db95-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="6db95-108">Streaming audio a bassa latenza e con resilienza.</span><span class="sxs-lookup"><span data-stu-id="6db95-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="6db95-109">Maggiore affidabilità (molte funzioni audio sono state spostate dalla modalità kernel alla modalità utente).</span><span class="sxs-lookup"><span data-stu-id="6db95-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="6db95-110">Maggiore sicurezza (l'elaborazione del contenuto audio protetto avviene in un processo sicuro con privilegi inferiori).</span><span class="sxs-lookup"><span data-stu-id="6db95-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="6db95-111">Assegnazione di particolari ruoli a livello di sistema (console, Multimedia e comunicazioni) a singoli dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="6db95-112">Astrazione del software dei dispositivi dell'endpoint audio (ad esempio, altoparlanti, cuffie e microfoni) manipolati direttamente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6db95-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="6db95-113">Le API di base audio sono state migliorate in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6db95-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="6db95-114">Per ulteriori informazioni sui miglioramenti e sulle nuove funzionalità aggiunte, vedere [What ' s New for Core Audio API in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span><span class="sxs-lookup"><span data-stu-id="6db95-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="6db95-115">Questa documentazione descrive le API audio principali.</span><span class="sxs-lookup"><span data-stu-id="6db95-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="6db95-116">Queste API vengono utilizzate come base per le API di livello superiore seguenti:</span><span class="sxs-lookup"><span data-stu-id="6db95-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="6db95-117">DirectSound</span><span class="sxs-lookup"><span data-stu-id="6db95-117">DirectSound</span></span>
-   <span data-ttu-id="6db95-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="6db95-118">DirectMusic</span></span>
-   <span data-ttu-id="6db95-119">Funzioni **waveXxx** e **mixerXxx** multimediali di Windows</span><span class="sxs-lookup"><span data-stu-id="6db95-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="6db95-120">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6db95-120">Media Foundation</span></span>

<span data-ttu-id="6db95-121">Queste API di livello superiore usano le API audio principali per condividere l'accesso ai dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="6db95-122">Media Foundation è una novità di Windows Vista, mentre le funzioni DirectSound, DirectMusic e **waveXxx** e **mixerXxx** sono supportate in Windows 98, Windows Millennium Edition e in Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6db95-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="6db95-123">La maggior parte delle applicazioni audio comunica con le API di livello superiore anziché comunicare direttamente con le API di base di audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="6db95-124">Di seguito sono riportati alcuni esempi di applicazioni che usano le API di livello superiore:</span><span class="sxs-lookup"><span data-stu-id="6db95-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="6db95-125">Lettori multimediali</span><span class="sxs-lookup"><span data-stu-id="6db95-125">Media players</span></span>
-   <span data-ttu-id="6db95-126">Lettori DVD</span><span class="sxs-lookup"><span data-stu-id="6db95-126">DVD players</span></span>
-   <span data-ttu-id="6db95-127">Giochi</span><span class="sxs-lookup"><span data-stu-id="6db95-127">Games</span></span>
-   <span data-ttu-id="6db95-128">Applicazioni aziendali, ad esempio Microsoft Office PowerPoint, che riproducono file audio</span><span class="sxs-lookup"><span data-stu-id="6db95-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="6db95-129">In genere, queste applicazioni comunicano con le API DirectSound o Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6db95-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="6db95-130">La comunicazione diretta con le API audio di base potrebbe non essere adatta per molte applicazioni audio per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="6db95-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="6db95-131">Ad esempio, le API audio principali richiedono flussi audio per usare i formati di dati nativi di un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="6db95-132">Tuttavia, gli sviluppatori di software di terze parti che sviluppano i tipi di prodotti seguenti potrebbero richiedere le funzionalità speciali delle API audio principali:</span><span class="sxs-lookup"><span data-stu-id="6db95-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="6db95-133">Applicazioni audio professionali ("Audio Pro")</span><span class="sxs-lookup"><span data-stu-id="6db95-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="6db95-134">Applicazioni di comunicazione in tempo reale (RTC)</span><span class="sxs-lookup"><span data-stu-id="6db95-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="6db95-135">API audio di terze parti</span><span class="sxs-lookup"><span data-stu-id="6db95-135">Third-party audio APIs</span></span>

<span data-ttu-id="6db95-136">Per ottenere una latenza minima, è possibile che un'applicazione "Audio Pro" o un'applicazione RTC debba accedere direttamente alle funzionalità di basso livello delle API audio principali, ottenendo l'accesso esclusivo all'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="6db95-137">Un'API audio di terze parti potrebbe richiedere l'accesso diretto alle API audio principali per implementare un set di funzionalità che potrebbero non essere supportate interamente da un'unica API audio di alto livello fornita con Windows.</span><span class="sxs-lookup"><span data-stu-id="6db95-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="6db95-138">Un'applicazione che usa un'API audio legacy per riprodurre o registrare audio potrebbe richiedere funzionalità aggiuntive non supportate dall'API audio legacy, ma supportate dalle API audio di base.</span><span class="sxs-lookup"><span data-stu-id="6db95-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="6db95-139">In molti casi, l'applicazione può accedere a queste funzionalità direttamente tramite le API audio principali, che possono essere usate in combinazione con l'API audio legacy.</span><span class="sxs-lookup"><span data-stu-id="6db95-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="6db95-140">Le API audio principali sono:</span><span class="sxs-lookup"><span data-stu-id="6db95-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="6db95-141">[API del dispositivo multimediale (MMDevice)](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="6db95-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="6db95-142">I client usano questa API per enumerare i dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6db95-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="6db95-143">[API di sessione audio Windows (WASAPI)](wasapi.md).</span><span class="sxs-lookup"><span data-stu-id="6db95-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="6db95-144">I client usano questa API per creare e gestire flussi audio da e verso dispositivi endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="6db95-145">[API DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="6db95-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="6db95-146">I client usano questa API per accedere direttamente alle funzionalità topologiche (ad esempio, i controlli volume e i multiplexer) che si trovano lungo i percorsi dati all'interno dei dispositivi hardware nelle schede audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="6db95-147">[API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="6db95-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="6db95-148">I client usano questa API per accedere direttamente ai controlli volume sui dispositivi dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="6db95-149">Questa API viene usata principalmente dalle applicazioni che gestiscono flussi audio in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="6db95-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="6db95-150">Queste API supportano la nozione intuitiva di un dispositivo endpoint, descritto in dispositivi dell' [endpoint audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="6db95-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="6db95-151">Microsoft non prevede di creare le API audio principali descritte di seguito disponibili per l'utilizzo con le versioni precedenti di Windows, tra cui Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="6db95-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="6db95-152">Questa panoramica include gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="6db95-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="6db95-153">**Argomento**</span><span class="sxs-lookup"><span data-stu-id="6db95-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="6db95-154">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6db95-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6db95-155">Novità relative alle API audio di base in Windows 7</span><span class="sxs-lookup"><span data-stu-id="6db95-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="6db95-156">Riepiloga le nuove funzionalità e i miglioramenti apportati alle API audio principali</span><span class="sxs-lookup"><span data-stu-id="6db95-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="6db95-157">File di intestazione e componenti di sistema</span><span class="sxs-lookup"><span data-stu-id="6db95-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="6db95-158">Descrive i file di intestazione e i componenti di sistema per le API audio di base.</span><span class="sxs-lookup"><span data-stu-id="6db95-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="6db95-159">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="6db95-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="6db95-160">Elenca gli esempi nell'Windows SDK che usano le API di base di audio.</span><span class="sxs-lookup"><span data-stu-id="6db95-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="6db95-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6db95-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db95-162">API audio Core</span><span class="sxs-lookup"><span data-stu-id="6db95-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



