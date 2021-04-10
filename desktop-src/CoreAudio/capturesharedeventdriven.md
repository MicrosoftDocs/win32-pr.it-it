---
description: Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata sugli eventi.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126906"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="59a3c-104">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="59a3c-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="59a3c-105">Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="59a3c-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="59a3c-106">In questo esempio viene illustrata la memorizzazione nel buffer basata sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="59a3c-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="59a3c-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="59a3c-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="59a3c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a3c-108">Description</span></span>](#description)
-   [<span data-ttu-id="59a3c-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59a3c-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="59a3c-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="59a3c-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="59a3c-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="59a3c-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="59a3c-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="59a3c-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="59a3c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59a3c-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="59a3c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a3c-114">Description</span></span>

<span data-ttu-id="59a3c-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="59a3c-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="59a3c-116">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="59a3c-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="59a3c-117">[WASAPI](wasapi.md) per le operazioni di gestione del flusso, ad esempio l'avvio e l'arresto del flusso e il cambio di flusso.</span><span class="sxs-lookup"><span data-stu-id="59a3c-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a3c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59a3c-118">Requirements</span></span>



| <span data-ttu-id="59a3c-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="59a3c-119">Product</span></span>                                                        | <span data-ttu-id="59a3c-120">Versione</span><span class="sxs-lookup"><span data-stu-id="59a3c-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="59a3c-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="59a3c-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="59a3c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59a3c-122">Windows 7</span></span> |
| <span data-ttu-id="59a3c-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="59a3c-123">Visual Studio</span></span>                                                  | <span data-ttu-id="59a3c-124">2008</span><span class="sxs-lookup"><span data-stu-id="59a3c-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="59a3c-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="59a3c-125">Downloading the Sample</span></span>

<span data-ttu-id="59a3c-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="59a3c-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="59a3c-127">Location</span><span class="sxs-lookup"><span data-stu-id="59a3c-127">Location</span></span>    | <span data-ttu-id="59a3c-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="59a3c-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a3c-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="59a3c-129">Windows SDK</span></span> | <span data-ttu-id="59a3c-130">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ CaptureSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="59a3c-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="59a3c-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="59a3c-131">Building the Sample</span></span>

<span data-ttu-id="59a3c-132">Per compilare l'esempio CaptureSharedEventDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="59a3c-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="59a3c-133">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio CaptureSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="59a3c-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="59a3c-134">Eseguire il comando `start WASAPICaptureSharedEventDriven.sln` nella directory CaptureSharedEventDriven per aprire il progetto WASAPICaptureSharedEventDriven nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="59a3c-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="59a3c-135">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="59a3c-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="59a3c-136">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="59a3c-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="59a3c-137">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPICaptureSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="59a3c-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="59a3c-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="59a3c-138">Running the Sample</span></span>

<span data-ttu-id="59a3c-139">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPICaptureSharedEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="59a3c-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="59a3c-140">Per eseguirlo, digitare `WASAPICaptureSharedEventDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="59a3c-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="59a3c-141">Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata di acquisizione nel dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="59a3c-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="59a3c-142">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="59a3c-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="59a3c-143">Argomento</span><span class="sxs-lookup"><span data-stu-id="59a3c-143">Argument</span></span>        | <span data-ttu-id="59a3c-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a3c-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="59a3c-145">-?</span><span class="sxs-lookup"><span data-stu-id="59a3c-145">-?</span></span>              | <span data-ttu-id="59a3c-146">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="59a3c-146">Shows help.</span></span>                                                |
| <span data-ttu-id="59a3c-147">-H</span><span class="sxs-lookup"><span data-stu-id="59a3c-147">-h</span></span>              | <span data-ttu-id="59a3c-148">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="59a3c-148">Shows help.</span></span>                                                |
| <span data-ttu-id="59a3c-149">-l</span><span class="sxs-lookup"><span data-stu-id="59a3c-149">-l</span></span>              | <span data-ttu-id="59a3c-150">Latenza di acquisizione audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="59a3c-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="59a3c-151">-d</span><span class="sxs-lookup"><span data-stu-id="59a3c-151">-d</span></span>              | <span data-ttu-id="59a3c-152">Durata acquisizione audio in secondi.</span><span class="sxs-lookup"><span data-stu-id="59a3c-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="59a3c-153">-M</span><span class="sxs-lookup"><span data-stu-id="59a3c-153">-m</span></span>              | <span data-ttu-id="59a3c-154">Disabilita l'uso di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="59a3c-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="59a3c-155">-Console</span><span class="sxs-lookup"><span data-stu-id="59a3c-155">-console</span></span>        | <span data-ttu-id="59a3c-156">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="59a3c-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="59a3c-157">-comunicazioni</span><span class="sxs-lookup"><span data-stu-id="59a3c-157">-communications</span></span> | <span data-ttu-id="59a3c-158">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="59a3c-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="59a3c-159">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="59a3c-159">-multimedia</span></span>     | <span data-ttu-id="59a3c-160">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="59a3c-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="59a3c-161">-endpoint</span><span class="sxs-lookup"><span data-stu-id="59a3c-161">-endpoint</span></span>       | <span data-ttu-id="59a3c-162">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="59a3c-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="59a3c-163">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="59a3c-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="59a3c-164">La console, la comunicazione e i dispositivi multimediali predefiniti sono elencati seguiti dai dispositivi e dagli identificatori dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="59a3c-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="59a3c-165">Se non viene specificata alcuna durata, il flusso audio dal dispositivo specificato viene acquisito per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="59a3c-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="59a3c-166">L'applicazione scrive i dati acquisiti in un file con estensione wav denominato in modo univoco.</span><span class="sxs-lookup"><span data-stu-id="59a3c-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="59a3c-167">CaptureSharedEventDriven illustra la memorizzazione nel buffer basata sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="59a3c-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="59a3c-168">Il client audio di cui è stata creata un'istanza per questo esempio è configurato per l'esecuzione in modalità condivisa e l'elaborazione del client del buffer audio viene eseguita mediante l'impostazione del flag **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** nella chiamata a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="59a3c-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="59a3c-169">Nell'esempio viene illustrato come il client deve fornire un handle di evento al sistema chiamando il metodo [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="59a3c-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="59a3c-170">Dopo l'inizio della sessione di acquisizione e l'avvio del flusso, il motore audio segnala all'handle di evento fornito di notificare al client ogni volta che un buffer è pronto per l'elaborazione da parte del client.</span><span class="sxs-lookup"><span data-stu-id="59a3c-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="59a3c-171">I dati audio possono anche essere elaborati in un ciclo basato su timer.</span><span class="sxs-lookup"><span data-stu-id="59a3c-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="59a3c-172">Questa modalità è dimostrato nell'esempio [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="59a3c-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a3c-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59a3c-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59a3c-174">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="59a3c-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



