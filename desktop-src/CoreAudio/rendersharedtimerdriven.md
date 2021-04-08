---
description: Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748538"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="164bb-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="164bb-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="164bb-104">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="164bb-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="164bb-105">Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="164bb-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="164bb-106">Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</span><span class="sxs-lookup"><span data-stu-id="164bb-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="164bb-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="164bb-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="164bb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164bb-108">Description</span></span>](#description)
-   [<span data-ttu-id="164bb-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="164bb-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="164bb-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="164bb-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="164bb-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="164bb-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="164bb-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="164bb-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="164bb-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="164bb-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="164bb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164bb-114">Description</span></span>

<span data-ttu-id="164bb-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="164bb-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="164bb-116">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="164bb-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="164bb-117">WASAPI per le operazioni di gestione del flusso.</span><span class="sxs-lookup"><span data-stu-id="164bb-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="164bb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="164bb-118">Requirements</span></span>



| <span data-ttu-id="164bb-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="164bb-119">Product</span></span>                                                        | <span data-ttu-id="164bb-120">Versione</span><span class="sxs-lookup"><span data-stu-id="164bb-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="164bb-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="164bb-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="164bb-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="164bb-122">Windows 7</span></span> |
| <span data-ttu-id="164bb-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="164bb-123">Visual Studio</span></span>                                                  | <span data-ttu-id="164bb-124">2008</span><span class="sxs-lookup"><span data-stu-id="164bb-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="164bb-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="164bb-125">Downloading the Sample</span></span>

<span data-ttu-id="164bb-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="164bb-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="164bb-127">Location</span><span class="sxs-lookup"><span data-stu-id="164bb-127">Location</span></span>    | <span data-ttu-id="164bb-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="164bb-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="164bb-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="164bb-129">Windows SDK</span></span> | <span data-ttu-id="164bb-130">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="164bb-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="164bb-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="164bb-131">Building the Sample</span></span>

<span data-ttu-id="164bb-132">Per compilare l'esempio RenderSharedTimerDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="164bb-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="164bb-133">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="164bb-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="164bb-134">Eseguire il comando `start WASAPIRenderSharedTimerDriven.sln` nella directory RenderSharedTimerDriven per aprire il progetto WASAPIRenderSharedTimerDriven nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="164bb-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="164bb-135">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="164bb-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="164bb-136">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="164bb-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="164bb-137">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIRenderSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="164bb-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="164bb-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="164bb-138">Running the Sample</span></span>

<span data-ttu-id="164bb-139">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPIRenderSharedTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="164bb-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="164bb-140">Per eseguirlo, digitare `WASAPIRenderSharedTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="164bb-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="164bb-141">Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione sul dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="164bb-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="164bb-142">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="164bb-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="164bb-143">Argomento</span><span class="sxs-lookup"><span data-stu-id="164bb-143">Argument</span></span>        | <span data-ttu-id="164bb-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164bb-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="164bb-145">-?</span><span class="sxs-lookup"><span data-stu-id="164bb-145">-?</span></span>              | <span data-ttu-id="164bb-146">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="164bb-146">Shows help.</span></span>                                                |
| <span data-ttu-id="164bb-147">-H</span><span class="sxs-lookup"><span data-stu-id="164bb-147">-h</span></span>              | <span data-ttu-id="164bb-148">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="164bb-148">Shows help.</span></span>                                                |
| <span data-ttu-id="164bb-149">-f</span><span class="sxs-lookup"><span data-stu-id="164bb-149">-f</span></span>              | <span data-ttu-id="164bb-150">Frequenza di onda sinusoidale in Hz.</span><span class="sxs-lookup"><span data-stu-id="164bb-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="164bb-151">-l</span><span class="sxs-lookup"><span data-stu-id="164bb-151">-l</span></span>              | <span data-ttu-id="164bb-152">Latenza di rendering audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="164bb-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="164bb-153">-d</span><span class="sxs-lookup"><span data-stu-id="164bb-153">-d</span></span>              | <span data-ttu-id="164bb-154">Durata in secondi dell'onda sinusoidale.</span><span class="sxs-lookup"><span data-stu-id="164bb-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="164bb-155">-M</span><span class="sxs-lookup"><span data-stu-id="164bb-155">-m</span></span>              | <span data-ttu-id="164bb-156">Disabilita l'uso di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="164bb-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="164bb-157">-Console</span><span class="sxs-lookup"><span data-stu-id="164bb-157">-console</span></span>        | <span data-ttu-id="164bb-158">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="164bb-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="164bb-159">-comunicazioni</span><span class="sxs-lookup"><span data-stu-id="164bb-159">-communications</span></span> | <span data-ttu-id="164bb-160">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="164bb-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="164bb-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="164bb-161">-multimedia</span></span>     | <span data-ttu-id="164bb-162">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="164bb-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="164bb-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="164bb-163">-endpoint</span></span>       | <span data-ttu-id="164bb-164">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="164bb-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="164bb-165">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di rendering.</span><span class="sxs-lookup"><span data-stu-id="164bb-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="164bb-166">Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda sinusoidale a 440 Hz per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="164bb-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="164bb-167">Questi valori possono essere modificati specificando i valori di opzione-f e-d.</span><span class="sxs-lookup"><span data-stu-id="164bb-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="164bb-168">RenderSharedTimerDriven illustra il buffering basato sul timer.</span><span class="sxs-lookup"><span data-stu-id="164bb-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="164bb-169">In questa modalità il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore del parametro-d, in millisecondi).</span><span class="sxs-lookup"><span data-stu-id="164bb-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="164bb-170">Quando il client viene riattivato, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore.</span><span class="sxs-lookup"><span data-stu-id="164bb-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="164bb-171">Prima che ogni elaborazione venga superata nel ciclo di buffering, il client deve rilevare la quantità di dati di cui eseguire il rendering in modo che i dati non sovraccarichino il buffer.</span><span class="sxs-lookup"><span data-stu-id="164bb-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="164bb-172">I dati audio da riprodurre sul dispositivo specificato possono essere elaborati abilitando il buffering basato sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="164bb-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="164bb-173">Questa modalità è illustrata nell'esempio [RenderSharedEventDriven](rendersharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="164bb-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="164bb-174">Per altre informazioni sul rendering di un flusso, vedere [rendering di un flusso](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="164bb-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="164bb-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="164bb-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="164bb-176">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="164bb-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



