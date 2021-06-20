---
description: Questa applicazione di esempio, che illustra il buffering basato su eventi, usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75553496219d0a4ddaf6685089de802e034f94cb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405134"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="9bf81-103">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="9bf81-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="9bf81-104">Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9bf81-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="9bf81-105">In questo esempio viene illustrata la memorizzazione nel buffer basata su eventi per un client di rendering in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="9bf81-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="9bf81-106">Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="9bf81-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="9bf81-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bf81-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9bf81-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bf81-108">Description</span></span>](#description)
-   [<span data-ttu-id="9bf81-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bf81-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9bf81-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9bf81-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9bf81-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9bf81-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9bf81-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9bf81-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="9bf81-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bf81-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="9bf81-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bf81-114">Description</span></span>

<span data-ttu-id="9bf81-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bf81-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="9bf81-116">[API MMDevice per](mmdevice-api.md) l'enumerazione e la selezione di dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="9bf81-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="9bf81-117">WASAPI per le operazioni di gestione dei flussi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf81-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bf81-118">Requirements</span></span>



| <span data-ttu-id="9bf81-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9bf81-119">Product</span></span>                                                        | <span data-ttu-id="9bf81-120">Versione</span><span class="sxs-lookup"><span data-stu-id="9bf81-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="9bf81-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9bf81-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="9bf81-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9bf81-122">Windows 7</span></span> |
| <span data-ttu-id="9bf81-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9bf81-123">Visual Studio</span></span>                                                  | <span data-ttu-id="9bf81-124">2008</span><span class="sxs-lookup"><span data-stu-id="9bf81-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9bf81-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9bf81-125">Downloading the Sample</span></span>

<span data-ttu-id="9bf81-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bf81-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="9bf81-127">Percorso</span><span class="sxs-lookup"><span data-stu-id="9bf81-127">Location</span></span>    | <span data-ttu-id="9bf81-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="9bf81-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf81-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9bf81-129">Windows SDK</span></span> | <span data-ttu-id="9bf81-130">\\Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderExclusiveEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="9bf81-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="9bf81-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9bf81-131">Building the Sample</span></span>

<span data-ttu-id="9bf81-132">Per compilare l'esempio RenderExclusiveEventDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="9bf81-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="9bf81-133">Aprire la shell CMD per il Windows SDK e passare alla directory di esempio RenderExclusiveEventDriven.</span><span class="sxs-lookup"><span data-stu-id="9bf81-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="9bf81-134">Eseguire il comando nella directory RenderExclusiveEventDriven per aprire il progetto `start WASAPIRenderExclusiveEventDriven.sln` WASAPIRenderExclusiveEventDriven Visual Studio finestra.</span><span class="sxs-lookup"><span data-stu-id="9bf81-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="9bf81-135">Nella finestra selezionare la configurazione della soluzione **Debug** o **Release,** selezionare il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.**</span><span class="sxs-lookup"><span data-stu-id="9bf81-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="9bf81-136">Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione sdk.</span><span class="sxs-lookup"><span data-stu-id="9bf81-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="9bf81-137">In tal caso, l'esempio non verrà compilato a meno che non si sia impostata in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPIRenderExclusiveEventDriven.vcproj.</span><span class="sxs-lookup"><span data-stu-id="9bf81-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9bf81-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9bf81-138">Running the Sample</span></span>

<span data-ttu-id="9bf81-139">Se l'applicazione demo viene compilata correttamente, viene generato WASAPIRenderExclusiveEventDriven.exe file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="9bf81-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="9bf81-140">Per eseguirlo, digitare `WASAPIRenderExclusiveEventDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="9bf81-141">L'esempio seguente illustra come eseguire l'esempio specificando la durata della riproduzione nel dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bf81-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="9bf81-142">Nella tabella seguente vengono illustrati gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="9bf81-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="9bf81-143">Argomento</span><span class="sxs-lookup"><span data-stu-id="9bf81-143">Argument</span></span>        | <span data-ttu-id="9bf81-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bf81-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="9bf81-145">-?</span><span class="sxs-lookup"><span data-stu-id="9bf81-145">-?</span></span>              | <span data-ttu-id="9bf81-146">Visualizza la Guida.</span><span class="sxs-lookup"><span data-stu-id="9bf81-146">Shows help.</span></span>                                                |
| <span data-ttu-id="9bf81-147">-H</span><span class="sxs-lookup"><span data-stu-id="9bf81-147">-h</span></span>              | <span data-ttu-id="9bf81-148">Visualizza la Guida.</span><span class="sxs-lookup"><span data-stu-id="9bf81-148">Shows help.</span></span>                                                |
| <span data-ttu-id="9bf81-149">-f</span><span class="sxs-lookup"><span data-stu-id="9bf81-149">-f</span></span>              | <span data-ttu-id="9bf81-150">Frequenza delle onde sinsino in Hz.</span><span class="sxs-lookup"><span data-stu-id="9bf81-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="9bf81-151">-l</span><span class="sxs-lookup"><span data-stu-id="9bf81-151">-l</span></span>              | <span data-ttu-id="9bf81-152">Latenza di rendering audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="9bf81-153">-d</span><span class="sxs-lookup"><span data-stu-id="9bf81-153">-d</span></span>              | <span data-ttu-id="9bf81-154">Durata dell'onda sinsidale in secondi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="9bf81-155">-M</span><span class="sxs-lookup"><span data-stu-id="9bf81-155">-m</span></span>              | <span data-ttu-id="9bf81-156">Disabilita l'utilizzo di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="9bf81-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="9bf81-157">-console</span><span class="sxs-lookup"><span data-stu-id="9bf81-157">-console</span></span>        | <span data-ttu-id="9bf81-158">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bf81-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="9bf81-159">-communications</span><span class="sxs-lookup"><span data-stu-id="9bf81-159">-communications</span></span> | <span data-ttu-id="9bf81-160">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bf81-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="9bf81-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="9bf81-161">-multimedia</span></span>     | <span data-ttu-id="9bf81-162">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bf81-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="9bf81-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="9bf81-163">-endpoint</span></span>       | <span data-ttu-id="9bf81-164">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="9bf81-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="9bf81-165">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di rendering.</span><span class="sxs-lookup"><span data-stu-id="9bf81-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="9bf81-166">Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda sinsidale a 440 Hz per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="9bf81-167">Questi valori possono essere modificati specificando i valori delle opzioni -f e -d.</span><span class="sxs-lookup"><span data-stu-id="9bf81-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="9bf81-168">L'esempio RenderExclusiveEventDriven illustra il buffering basato su eventi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="9bf81-169">L'esempio illustra come:</span><span class="sxs-lookup"><span data-stu-id="9bf81-169">The sample shows how to:</span></span>

-   <span data-ttu-id="9bf81-170">Creare un'istanza di un client audio, configurarlo per l'esecuzione in modalità esclusiva e abilitare il buffering basato su eventi impostando il flag **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** nella chiamata a [**IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)</span><span class="sxs-lookup"><span data-stu-id="9bf81-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="9bf81-171">Associare il client agli esempi pronti per il rendering fornendo un handle di evento al sistema chiamando il [**metodo IAudioClient::SetEventHandle.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)</span><span class="sxs-lookup"><span data-stu-id="9bf81-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="9bf81-172">Creare un thread di rendering per elaborare esempi dal motore audio.</span><span class="sxs-lookup"><span data-stu-id="9bf81-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="9bf81-173">Allineare correttamente i buffer su un limite di 128 byte prima di inviarli al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9bf81-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="9bf81-174">Questa operazione viene eseguita regolando la periodicità del motore.</span><span class="sxs-lookup"><span data-stu-id="9bf81-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="9bf81-175">Controllare il formato di combinazione dell'endpoint del dispositivo per determinare se è possibile eseguire il rendering degli esempi.</span><span class="sxs-lookup"><span data-stu-id="9bf81-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="9bf81-176">Se il dispositivo non supporta il formato di combinazione, i dati vengono convertiti in PCM.</span><span class="sxs-lookup"><span data-stu-id="9bf81-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="9bf81-177">Gestire il cambio di flusso.</span><span class="sxs-lookup"><span data-stu-id="9bf81-177">Handle stream switching.</span></span>

<span data-ttu-id="9bf81-178">Dopo l'avvio della sessione di rendering e l'avvio del flusso, il motore audio segnala l'handle di evento fornito per notificare al client ogni volta che un buffer diventa pronto per l'elaborazione da parte del client.</span><span class="sxs-lookup"><span data-stu-id="9bf81-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="9bf81-179">I dati audio possono essere elaborati anche in un ciclo basato su timer.</span><span class="sxs-lookup"><span data-stu-id="9bf81-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="9bf81-180">Questa modalità è illustrata [nell'esempio RenderExclusiveTimerDriven.](renderexclusivetimerdriven.md)</span><span class="sxs-lookup"><span data-stu-id="9bf81-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="9bf81-181">Per altre informazioni sul rendering di un flusso, vedere [Rendering di un flusso.](rendering-a-stream.md)</span><span class="sxs-lookup"><span data-stu-id="9bf81-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bf81-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bf81-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf81-183">Esempi di SDK che usano le API audio di base</span><span class="sxs-lookup"><span data-stu-id="9bf81-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



