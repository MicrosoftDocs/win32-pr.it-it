---
description: Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente. Questo esempio illustra il buffering basato sul timer.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049200"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="2c0cd-104">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="2c0cd-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="2c0cd-105">Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="2c0cd-106">Questo esempio illustra il buffering basato sul timer.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="2c0cd-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2c0cd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c0cd-108">Description</span></span>](#description)
-   [<span data-ttu-id="2c0cd-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c0cd-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2c0cd-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2c0cd-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2c0cd-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="2c0cd-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c0cd-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="2c0cd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c0cd-114">Description</span></span>

<span data-ttu-id="2c0cd-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="2c0cd-116">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="2c0cd-117">[WASAPI](wasapi.md) per le operazioni di gestione del flusso.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0cd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c0cd-118">Requirements</span></span>



| <span data-ttu-id="2c0cd-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2c0cd-119">Product</span></span>                                                        | <span data-ttu-id="2c0cd-120">Versione</span><span class="sxs-lookup"><span data-stu-id="2c0cd-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="2c0cd-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2c0cd-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="2c0cd-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c0cd-122">Windows 7</span></span> |
| <span data-ttu-id="2c0cd-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-123">Visual Studio</span></span>                                                  | <span data-ttu-id="2c0cd-124">2008</span><span class="sxs-lookup"><span data-stu-id="2c0cd-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2c0cd-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-125">Downloading the Sample</span></span>

<span data-ttu-id="2c0cd-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="2c0cd-127">Location</span><span class="sxs-lookup"><span data-stu-id="2c0cd-127">Location</span></span>    | <span data-ttu-id="2c0cd-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="2c0cd-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0cd-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2c0cd-129">Windows SDK</span></span> | <span data-ttu-id="2c0cd-130">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ CaptureSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="2c0cd-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="2c0cd-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-131">Building the Sample</span></span>

<span data-ttu-id="2c0cd-132">Per compilare l'esempio CaptureSharedTimerDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="2c0cd-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="2c0cd-133">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio CaptureSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="2c0cd-134">Eseguire il comando `start WASAPICaptureSharedTimerDriven.sln` nella directory CaptureSharedTimerDriven per aprire il progetto WASAPICaptureSharedTimerDriven nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="2c0cd-135">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="2c0cd-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="2c0cd-136">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="2c0cd-137">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPICaptureSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2c0cd-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c0cd-138">Running the Sample</span></span>

<span data-ttu-id="2c0cd-139">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPICaptureSharedTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="2c0cd-140">Per eseguirlo, digitare `WASAPICaptureSharedTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="2c0cd-141">Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata di acquisizione nel dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="2c0cd-142">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="2c0cd-143">Argomento</span><span class="sxs-lookup"><span data-stu-id="2c0cd-143">Argument</span></span>        | <span data-ttu-id="2c0cd-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c0cd-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="2c0cd-145">-?</span><span class="sxs-lookup"><span data-stu-id="2c0cd-145">-?</span></span>              | <span data-ttu-id="2c0cd-146">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-146">Shows help.</span></span>                                                |
| <span data-ttu-id="2c0cd-147">-H</span><span class="sxs-lookup"><span data-stu-id="2c0cd-147">-h</span></span>              | <span data-ttu-id="2c0cd-148">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-148">Shows help.</span></span>                                                |
| <span data-ttu-id="2c0cd-149">-l</span><span class="sxs-lookup"><span data-stu-id="2c0cd-149">-l</span></span>              | <span data-ttu-id="2c0cd-150">Latenza di acquisizione audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="2c0cd-151">-d</span><span class="sxs-lookup"><span data-stu-id="2c0cd-151">-d</span></span>              | <span data-ttu-id="2c0cd-152">Durata acquisizione audio in secondi.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="2c0cd-153">-M</span><span class="sxs-lookup"><span data-stu-id="2c0cd-153">-m</span></span>              | <span data-ttu-id="2c0cd-154">Disabilita l'uso di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="2c0cd-155">-Console</span><span class="sxs-lookup"><span data-stu-id="2c0cd-155">-console</span></span>        | <span data-ttu-id="2c0cd-156">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="2c0cd-157">-comunicazioni</span><span class="sxs-lookup"><span data-stu-id="2c0cd-157">-communications</span></span> | <span data-ttu-id="2c0cd-158">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="2c0cd-159">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="2c0cd-159">-multimedia</span></span>     | <span data-ttu-id="2c0cd-160">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="2c0cd-161">-endpoint</span><span class="sxs-lookup"><span data-stu-id="2c0cd-161">-endpoint</span></span>       | <span data-ttu-id="2c0cd-162">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="2c0cd-163">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="2c0cd-164">La console, la comunicazione e i dispositivi multimediali predefiniti sono elencati seguiti dai dispositivi e dagli identificatori dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="2c0cd-165">Se non viene specificata alcuna durata, il flusso audio dal dispositivo specificato viene acquisito per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="2c0cd-166">L'applicazione scrive i dati acquisiti in un file con estensione wav denominato in modo univoco.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="2c0cd-167">CaptureSharedTimerDriven illustra il buffering basato sul timer.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="2c0cd-168">In questa modalità il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore del parametro-d, in millisecondi).</span><span class="sxs-lookup"><span data-stu-id="2c0cd-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="2c0cd-169">Quando il client viene riattivato, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="2c0cd-170">Prima che ogni elaborazione venga superata nel ciclo di buffering, il client deve rilevare la quantità di dati di acquisizione disponibili, in modo che i dati non sovraccarichino il buffer di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="2c0cd-171">I dati audio acquisiti dal dispositivo specificato possono essere elaborati abilitando il buffering basato sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="2c0cd-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="2c0cd-172">Questa modalità è illustrata nell'esempio [CaptureSharedEventDriven](capturesharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="2c0cd-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c0cd-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c0cd-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c0cd-174">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="2c0cd-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



