---
description: Questa applicazione di esempio, che illustra il buffering basato su timer, usa le API Audio core per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d2814f359668f8724d3deb65a7c2a9eeff5b06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410094"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="3d09c-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="3d09c-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="3d09c-104">Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3d09c-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="3d09c-105">Questo esempio illustra il buffering basato su timer per un client di rendering in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="3d09c-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="3d09c-106">Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</span><span class="sxs-lookup"><span data-stu-id="3d09c-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="3d09c-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d09c-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3d09c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d09c-108">Description</span></span>](#description)
-   [<span data-ttu-id="3d09c-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d09c-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3d09c-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="3d09c-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3d09c-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="3d09c-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3d09c-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="3d09c-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="3d09c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d09c-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="3d09c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d09c-114">Description</span></span>

<span data-ttu-id="3d09c-115">Questo esempio illustra le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d09c-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="3d09c-116">[API MMDevice per](mmdevice-api.md) l'enumerazione e la selezione di dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="3d09c-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="3d09c-117">WASAPI per le operazioni di gestione dei flussi.</span><span class="sxs-lookup"><span data-stu-id="3d09c-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d09c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d09c-118">Requirements</span></span>



| <span data-ttu-id="3d09c-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3d09c-119">Product</span></span>                                                        | <span data-ttu-id="3d09c-120">Versione</span><span class="sxs-lookup"><span data-stu-id="3d09c-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="3d09c-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3d09c-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="3d09c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d09c-122">Windows 7</span></span> |
| <span data-ttu-id="3d09c-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d09c-123">Visual Studio</span></span>                                                  | <span data-ttu-id="3d09c-124">2008</span><span class="sxs-lookup"><span data-stu-id="3d09c-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3d09c-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="3d09c-125">Downloading the Sample</span></span>

<span data-ttu-id="3d09c-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d09c-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="3d09c-127">Percorso</span><span class="sxs-lookup"><span data-stu-id="3d09c-127">Location</span></span>    | <span data-ttu-id="3d09c-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="3d09c-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d09c-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3d09c-129">Windows SDK</span></span> | <span data-ttu-id="3d09c-130">\\Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="3d09c-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="3d09c-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="3d09c-131">Building the Sample</span></span>

<span data-ttu-id="3d09c-132">Per compilare l'esempio RenderSharedTimerDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="3d09c-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="3d09c-133">Aprire la shell CMD per il Windows SDK e passare alla directory di esempio RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="3d09c-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="3d09c-134">Eseguire il `start WASAPIRenderSharedTimerDriven.sln` comando nella directory RenderSharedTimerDriven per aprire il progetto WASAPIRenderSharedTimerDriven nella finestra Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3d09c-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="3d09c-135">Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.**</span><span class="sxs-lookup"><span data-stu-id="3d09c-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="3d09c-136">Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK.</span><span class="sxs-lookup"><span data-stu-id="3d09c-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="3d09c-137">In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPIRenderSharedTimerDriven.vcproj.</span><span class="sxs-lookup"><span data-stu-id="3d09c-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3d09c-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="3d09c-138">Running the Sample</span></span>

<span data-ttu-id="3d09c-139">Se si compila correttamente l'applicazione demo, viene generato un file eseguibile, WASAPIRenderSharedTimerDriven.exe,</span><span class="sxs-lookup"><span data-stu-id="3d09c-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="3d09c-140">Per eseguirlo, digitare `WASAPIRenderSharedTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="3d09c-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="3d09c-141">Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione nel dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d09c-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="3d09c-142">Nella tabella seguente vengono illustrati gli argomenti .</span><span class="sxs-lookup"><span data-stu-id="3d09c-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="3d09c-143">Argomento</span><span class="sxs-lookup"><span data-stu-id="3d09c-143">Argument</span></span>        | <span data-ttu-id="3d09c-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d09c-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="3d09c-145">-?</span><span class="sxs-lookup"><span data-stu-id="3d09c-145">-?</span></span>              | <span data-ttu-id="3d09c-146">Visualizza la Guida.</span><span class="sxs-lookup"><span data-stu-id="3d09c-146">Shows help.</span></span>                                                |
| <span data-ttu-id="3d09c-147">-H</span><span class="sxs-lookup"><span data-stu-id="3d09c-147">-h</span></span>              | <span data-ttu-id="3d09c-148">Visualizza la Guida.</span><span class="sxs-lookup"><span data-stu-id="3d09c-148">Shows help.</span></span>                                                |
| <span data-ttu-id="3d09c-149">-f</span><span class="sxs-lookup"><span data-stu-id="3d09c-149">-f</span></span>              | <span data-ttu-id="3d09c-150">Frequenza delle onde sinsino in Hz.</span><span class="sxs-lookup"><span data-stu-id="3d09c-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="3d09c-151">-l</span><span class="sxs-lookup"><span data-stu-id="3d09c-151">-l</span></span>              | <span data-ttu-id="3d09c-152">Latenza di rendering audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="3d09c-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="3d09c-153">-d</span><span class="sxs-lookup"><span data-stu-id="3d09c-153">-d</span></span>              | <span data-ttu-id="3d09c-154">Durata dell'ondata seno in secondi.</span><span class="sxs-lookup"><span data-stu-id="3d09c-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="3d09c-155">-M</span><span class="sxs-lookup"><span data-stu-id="3d09c-155">-m</span></span>              | <span data-ttu-id="3d09c-156">Disabilita l'uso di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="3d09c-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="3d09c-157">-console</span><span class="sxs-lookup"><span data-stu-id="3d09c-157">-console</span></span>        | <span data-ttu-id="3d09c-158">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d09c-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="3d09c-159">-communications</span><span class="sxs-lookup"><span data-stu-id="3d09c-159">-communications</span></span> | <span data-ttu-id="3d09c-160">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d09c-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="3d09c-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="3d09c-161">-multimedia</span></span>     | <span data-ttu-id="3d09c-162">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d09c-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="3d09c-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="3d09c-163">-endpoint</span></span>       | <span data-ttu-id="3d09c-164">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="3d09c-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="3d09c-165">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e richiede all'utente di selezionare un dispositivo per la sessione di rendering.</span><span class="sxs-lookup"><span data-stu-id="3d09c-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="3d09c-166">Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda seno a 440 Hz per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="3d09c-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="3d09c-167">Questi valori possono essere modificati specificando i valori delle opzioni -f e -d.</span><span class="sxs-lookup"><span data-stu-id="3d09c-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="3d09c-168">RenderSharedTimerDriven illustra il buffer basato su timer.</span><span class="sxs-lookup"><span data-stu-id="3d09c-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="3d09c-169">In questa modalità, il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore dell'opzione -d, in millisecondi).</span><span class="sxs-lookup"><span data-stu-id="3d09c-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="3d09c-170">Quando il client si riattiva, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore.</span><span class="sxs-lookup"><span data-stu-id="3d09c-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="3d09c-171">Prima che ogni elaborazione passi nel ciclo di memorizzazione nel buffer, il client deve individuare la quantità di dati di cui eseguire il rendering in modo che i dati non esercitino il buffer.</span><span class="sxs-lookup"><span data-stu-id="3d09c-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="3d09c-172">I dati audio da riprodurre nel dispositivo specificato possono essere elaborati abilitando il buffer basato su eventi.</span><span class="sxs-lookup"><span data-stu-id="3d09c-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="3d09c-173">Questa modalità è illustrata [nell'esempio RenderSharedEventDriven.](rendersharedeventdriven.md)</span><span class="sxs-lookup"><span data-stu-id="3d09c-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="3d09c-174">Per altre informazioni sul rendering di un flusso, vedere [Rendering di un flusso](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="3d09c-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d09c-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d09c-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d09c-176">Esempi di SDK che usano le API audio di base</span><span class="sxs-lookup"><span data-stu-id="3d09c-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



