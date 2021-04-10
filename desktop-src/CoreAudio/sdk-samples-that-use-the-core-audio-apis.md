---
description: Esempi di SDK che usano le API audio principali
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Esempi di SDK che usano le API audio principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966178"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="af080-103">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="af080-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="af080-104">Il Windows SDK include gli esempi di codice seguenti che illustrano l'uso delle API audio di base.</span><span class="sxs-lookup"><span data-stu-id="af080-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="af080-105">Gli esempi seguenti si trovano nella directory% MSSdk% \\ Samples \\ Multimedia \\ audio, dove% MSSdk% è la directory radice dell'installazione del Windows SDK nel computer.</span><span class="sxs-lookup"><span data-stu-id="af080-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af080-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="af080-106">Sample</span></span></th>
<th><span data-ttu-id="af080-107">Deascription</span><span class="sxs-lookup"><span data-stu-id="af080-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af080-108"><a href="aecmicarray.md">AECMicArray</a></span><span class="sxs-lookup"><span data-stu-id="af080-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="af080-109">Questo esempio usa le API MMDevice, WASAPI, DeviceTopology e EndpointVolume per acquisire un flusso vocale di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="af080-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="af080-110">L'esempio TImpossibile supporta l'elaborazione Echo Echo Cancel (AEC) e la matrice di microfoni usando l'AEC DMO chiamato anche il DSP di acquisizione vocale fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af080-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af080-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="af080-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="af080-112">Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input, specificato dall'utente e lo scrive in un nome univoco. File WAV nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="af080-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="af080-113">In questo esempio viene illustrata la memorizzazione nel buffer basata sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="af080-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af080-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="af080-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="af080-115">Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input, specificato dall'utente e lo scrive in un nome univoco. File WAV nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="af080-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="af080-116">Questo esempio illustra il buffering basato sul timer.</span><span class="sxs-lookup"><span data-stu-id="af080-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af080-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span><span class="sxs-lookup"><span data-stu-id="af080-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="af080-118">Questa applicazione di esempio illustra l'apertura e la chiusura di flussi di comunicazione e la generazione di eventi ducking che un'applicazione può ottenere per implementare l'attenuazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="af080-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="af080-119">Questa applicazione implementa un client di chat che usa le API audio principali per leggere i dati audio da un dispositivo di comunicazione e riprodurli sul dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="af080-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af080-120"><a href="endpointvolume.md">EndpointVolume</a></span><span class="sxs-lookup"><span data-stu-id="af080-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="af080-121">Questa applicazione di esempio usa le API audio principali per modificare il volume del dispositivo, specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af080-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af080-122"><a href="osd.md">OSD</a></span><span class="sxs-lookup"><span data-stu-id="af080-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="af080-123">Questo esempio usa le API MMDevice e EndpointVolume per implementare una visualizzazione sullo schermo che mostra le modifiche del volume al flusso di output che riproduce il dispositivo dell'endpoint di rendering audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="af080-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="af080-124">La visualizzazione sullo schermo viene visualizzata quando l'utente regola il livello del volume nel programma di controllo del volume di Windows, Sndvol.exe e scompare dopo che il livello del volume rimane invariato per un breve periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="af080-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af080-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="af080-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="af080-126">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af080-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="af080-127">In questo esempio viene illustrato il buffer basato sugli eventi per un client di rendering in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="af080-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="af080-128">Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="af080-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af080-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="af080-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="af080-130">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af080-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="af080-131">Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="af080-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="af080-132">Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="af080-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af080-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="af080-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="af080-134">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af080-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="af080-135">Questo esempio illustra il buffering basato sugli eventi per un client di rendering in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="af080-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="af080-136">Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</span><span class="sxs-lookup"><span data-stu-id="af080-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af080-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="af080-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="af080-138">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af080-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="af080-139">Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="af080-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="af080-140">Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</span><span class="sxs-lookup"><span data-stu-id="af080-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af080-141">WinAudio</span><span class="sxs-lookup"><span data-stu-id="af080-141">WinAudio</span></span></td>
<td><span data-ttu-id="af080-142">Questo esempio usa l'API MMDevice e WASAPI per riprodurre e acquisire flussi audio.</span><span class="sxs-lookup"><span data-stu-id="af080-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="af080-143">L'interfaccia utente di questa applicazione di esempio consente agli utenti di selezionare dispositivi endpoint audio, modificare il livello del volume della sessione audio locale e riprodurre i file WAV e l'input del microfono.</span><span class="sxs-lookup"><span data-stu-id="af080-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="af080-144">Questo esempio è stato deprecato in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af080-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="af080-145">È possibile scaricare il Windows SDK dal sito Web dell' [area download Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .</span><span class="sxs-lookup"><span data-stu-id="af080-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af080-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af080-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af080-147">Informazioni sulle API audio di Windows Core</span><span class="sxs-lookup"><span data-stu-id="af080-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




