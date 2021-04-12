---
description: Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità esclusiva.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483484"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="73abd-104">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="73abd-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="73abd-105">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="73abd-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="73abd-106">Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="73abd-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="73abd-107">Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="73abd-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="73abd-108">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="73abd-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="73abd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73abd-109">Description</span></span>](#description)
-   [<span data-ttu-id="73abd-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73abd-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="73abd-111">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="73abd-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="73abd-112">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="73abd-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="73abd-113">Visualizzare i file di esempio</span><span class="sxs-lookup"><span data-stu-id="73abd-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="73abd-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73abd-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="73abd-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73abd-115">Description</span></span>

<span data-ttu-id="73abd-116">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="73abd-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="73abd-117">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="73abd-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="73abd-118">WASAPI per le operazioni di gestione del flusso.</span><span class="sxs-lookup"><span data-stu-id="73abd-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="73abd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73abd-119">Requirements</span></span>



| <span data-ttu-id="73abd-120">Prodotto</span><span class="sxs-lookup"><span data-stu-id="73abd-120">Product</span></span>                                                        | <span data-ttu-id="73abd-121">Versione</span><span class="sxs-lookup"><span data-stu-id="73abd-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="73abd-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="73abd-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="73abd-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73abd-123">Windows 7</span></span> |
| <span data-ttu-id="73abd-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73abd-124">Visual Studio</span></span>                                                  | <span data-ttu-id="73abd-125">2008</span><span class="sxs-lookup"><span data-stu-id="73abd-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="73abd-126">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="73abd-126">Downloading the Sample</span></span>

<span data-ttu-id="73abd-127">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="73abd-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="73abd-128">Location</span><span class="sxs-lookup"><span data-stu-id="73abd-128">Location</span></span>    | <span data-ttu-id="73abd-129">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="73abd-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73abd-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="73abd-130">Windows SDK</span></span> | <span data-ttu-id="73abd-131">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ RenderExclusiveTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="73abd-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="73abd-132">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="73abd-132">Building the Sample</span></span>

<span data-ttu-id="73abd-133">Per compilare l'esempio RenderExclusiveTimerDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="73abd-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="73abd-134">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="73abd-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="73abd-135">Eseguire il comando `start WASAPIRenderExclusiveTimerDriven.sln` nella directory RenderExclusiveTimerDriven per aprire il progetto WASAPIRenderExclusiveTimerDriven nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73abd-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="73abd-136">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="73abd-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="73abd-137">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="73abd-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="73abd-138">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIRenderExclusiveTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="73abd-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="73abd-139">Visualizzare i file di esempio</span><span class="sxs-lookup"><span data-stu-id="73abd-139">View the Sample Files</span></span>

<span data-ttu-id="73abd-140">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPIRenderExclusiveTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="73abd-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="73abd-141">Per eseguirlo, digitare `WASAPIRenderExclusiveTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="73abd-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="73abd-142">Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione sul dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="73abd-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="73abd-143">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="73abd-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="73abd-144">Argomento</span><span class="sxs-lookup"><span data-stu-id="73abd-144">Argument</span></span>        | <span data-ttu-id="73abd-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73abd-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="73abd-146">-?</span><span class="sxs-lookup"><span data-stu-id="73abd-146">-?</span></span>              | <span data-ttu-id="73abd-147">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="73abd-147">Shows help.</span></span>                                                |
| <span data-ttu-id="73abd-148">-H</span><span class="sxs-lookup"><span data-stu-id="73abd-148">-h</span></span>              | <span data-ttu-id="73abd-149">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="73abd-149">Shows help.</span></span>                                                |
| <span data-ttu-id="73abd-150">-f</span><span class="sxs-lookup"><span data-stu-id="73abd-150">-f</span></span>              | <span data-ttu-id="73abd-151">Frequenza di onda sinusoidale in Hz.</span><span class="sxs-lookup"><span data-stu-id="73abd-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="73abd-152">-l</span><span class="sxs-lookup"><span data-stu-id="73abd-152">-l</span></span>              | <span data-ttu-id="73abd-153">Latenza di rendering audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="73abd-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="73abd-154">-d</span><span class="sxs-lookup"><span data-stu-id="73abd-154">-d</span></span>              | <span data-ttu-id="73abd-155">Durata in secondi dell'onda sinusoidale.</span><span class="sxs-lookup"><span data-stu-id="73abd-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="73abd-156">-M</span><span class="sxs-lookup"><span data-stu-id="73abd-156">-m</span></span>              | <span data-ttu-id="73abd-157">Disabilita l'uso di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="73abd-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="73abd-158">-Console</span><span class="sxs-lookup"><span data-stu-id="73abd-158">-console</span></span>        | <span data-ttu-id="73abd-159">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="73abd-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="73abd-160">-comunicazioni</span><span class="sxs-lookup"><span data-stu-id="73abd-160">-communications</span></span> | <span data-ttu-id="73abd-161">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="73abd-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="73abd-162">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="73abd-162">-multimedia</span></span>     | <span data-ttu-id="73abd-163">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="73abd-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="73abd-164">-endpoint</span><span class="sxs-lookup"><span data-stu-id="73abd-164">-endpoint</span></span>       | <span data-ttu-id="73abd-165">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="73abd-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="73abd-166">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di rendering.</span><span class="sxs-lookup"><span data-stu-id="73abd-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="73abd-167">Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda sinusoidale a 440 Hz per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="73abd-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="73abd-168">Questi valori possono essere modificati specificando i valori di opzione-f e-d.</span><span class="sxs-lookup"><span data-stu-id="73abd-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="73abd-169">RenderExclusiveTimerDriven illustra il buffering basato sul timer.</span><span class="sxs-lookup"><span data-stu-id="73abd-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="73abd-170">In questa modalità il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore del parametro-d, in millisecondi).</span><span class="sxs-lookup"><span data-stu-id="73abd-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="73abd-171">Quando il client viene riattivato, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore.</span><span class="sxs-lookup"><span data-stu-id="73abd-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="73abd-172">Prima che ogni elaborazione venga superata nel ciclo di buffering, il client deve rilevare la quantità di dati di cui eseguire il rendering in modo che i dati non sovraccarichino il buffer.</span><span class="sxs-lookup"><span data-stu-id="73abd-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="73abd-173">I dati audio da riprodurre sul dispositivo specificato possono essere elaborati abilitando il buffering basato sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="73abd-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="73abd-174">Questa modalità è illustrata nell'esempio RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="73abd-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="73abd-175">Per altre informazioni sul rendering di un flusso, vedere [rendering di un flusso](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="73abd-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73abd-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73abd-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73abd-177">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="73abd-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



