---
description: Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: RenderSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877946"
---
# <a name="rendersharedeventdriven"></a><span data-ttu-id="2f748-103">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="2f748-103">RenderSharedEventDriven</span></span>

<span data-ttu-id="2f748-104">Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2f748-104">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="2f748-105">Questo esempio illustra il buffering basato sugli eventi per un client di rendering in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="2f748-105">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="2f748-106">Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</span><span class="sxs-lookup"><span data-stu-id="2f748-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="2f748-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f748-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2f748-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f748-108">Description</span></span>](#description)
-   [<span data-ttu-id="2f748-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f748-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2f748-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2f748-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2f748-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2f748-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2f748-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2f748-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="2f748-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f748-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="2f748-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f748-114">Description</span></span>

<span data-ttu-id="2f748-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f748-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="2f748-116">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="2f748-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="2f748-117">WASAPI per le operazioni di gestione del flusso.</span><span class="sxs-lookup"><span data-stu-id="2f748-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f748-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f748-118">Requirements</span></span>



| <span data-ttu-id="2f748-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2f748-119">Product</span></span>                                                        | <span data-ttu-id="2f748-120">Versione</span><span class="sxs-lookup"><span data-stu-id="2f748-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="2f748-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2f748-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="2f748-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f748-122">Windows 7</span></span> |
| <span data-ttu-id="2f748-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2f748-123">Visual Studio</span></span>                                                  | <span data-ttu-id="2f748-124">2008</span><span class="sxs-lookup"><span data-stu-id="2f748-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2f748-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2f748-125">Downloading the Sample</span></span>

<span data-ttu-id="2f748-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f748-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="2f748-127">Location</span><span class="sxs-lookup"><span data-stu-id="2f748-127">Location</span></span>    | <span data-ttu-id="2f748-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="2f748-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f748-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2f748-129">Windows SDK</span></span> | <span data-ttu-id="2f748-130">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ RenderSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="2f748-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="2f748-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2f748-131">Building the Sample</span></span>

<span data-ttu-id="2f748-132">Per compilare l'esempio RenderSharedEventDriven, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="2f748-132">To build the RenderSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="2f748-133">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio RenderSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="2f748-133">Open the CMD shell for the Windows SDK and change to the RenderSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="2f748-134">Eseguire il comando `start WASAPIRenderSharedEventDriven.sln` nella directory RenderSharedEventDriven per aprire il progetto WASAPIRenderSharedEventDriven nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2f748-134">Run the command `start WASAPIRenderSharedEventDriven.sln` in the RenderSharedEventDriven directory to open the WASAPIRenderSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="2f748-135">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="2f748-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="2f748-136">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="2f748-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="2f748-137">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIRenderSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="2f748-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2f748-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2f748-138">Running the Sample</span></span>

<span data-ttu-id="2f748-139">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPIRenderSharedEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="2f748-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="2f748-140">Per eseguirlo, digitare `WASAPIRenderSharedEventDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="2f748-140">To run it, type `WASAPIRenderSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="2f748-141">Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione sul dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f748-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="2f748-142">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="2f748-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="2f748-143">Argomento</span><span class="sxs-lookup"><span data-stu-id="2f748-143">Argument</span></span>        | <span data-ttu-id="2f748-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f748-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="2f748-145">-?</span><span class="sxs-lookup"><span data-stu-id="2f748-145">-?</span></span>              | <span data-ttu-id="2f748-146">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="2f748-146">Shows help.</span></span>                                                |
| <span data-ttu-id="2f748-147">-H</span><span class="sxs-lookup"><span data-stu-id="2f748-147">-h</span></span>              | <span data-ttu-id="2f748-148">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="2f748-148">Shows help.</span></span>                                                |
| <span data-ttu-id="2f748-149">-f</span><span class="sxs-lookup"><span data-stu-id="2f748-149">-f</span></span>              | <span data-ttu-id="2f748-150">Frequenza di onda sinusoidale in Hz.</span><span class="sxs-lookup"><span data-stu-id="2f748-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="2f748-151">-l</span><span class="sxs-lookup"><span data-stu-id="2f748-151">-l</span></span>              | <span data-ttu-id="2f748-152">Latenza di rendering audio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="2f748-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="2f748-153">-d</span><span class="sxs-lookup"><span data-stu-id="2f748-153">-d</span></span>              | <span data-ttu-id="2f748-154">Durata in secondi dell'onda sinusoidale.</span><span class="sxs-lookup"><span data-stu-id="2f748-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="2f748-155">-M</span><span class="sxs-lookup"><span data-stu-id="2f748-155">-m</span></span>              | <span data-ttu-id="2f748-156">Disabilita l'uso di MMCSS.</span><span class="sxs-lookup"><span data-stu-id="2f748-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="2f748-157">-Console</span><span class="sxs-lookup"><span data-stu-id="2f748-157">-console</span></span>        | <span data-ttu-id="2f748-158">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f748-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="2f748-159">-comunicazioni</span><span class="sxs-lookup"><span data-stu-id="2f748-159">-communications</span></span> | <span data-ttu-id="2f748-160">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f748-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="2f748-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="2f748-161">-multimedia</span></span>     | <span data-ttu-id="2f748-162">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f748-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="2f748-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="2f748-163">-endpoint</span></span>       | <span data-ttu-id="2f748-164">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="2f748-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="2f748-165">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di rendering.</span><span class="sxs-lookup"><span data-stu-id="2f748-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="2f748-166">Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda sinusoidale a 440 Hz per 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="2f748-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="2f748-167">Questi valori possono essere modificati specificando i valori di opzione-f e-d.</span><span class="sxs-lookup"><span data-stu-id="2f748-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="2f748-168">RenderSharedEventDriven illustra la memorizzazione nel buffer basata sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="2f748-168">RenderSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="2f748-169">Nell'esempio viene illustrato come eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f748-169">The sample shows how to:</span></span>

-   <span data-ttu-id="2f748-170">Creare un'istanza di un client audio, configurarlo per l'esecuzione in modalità esclusiva e abilitare la memorizzazione nel buffer basata sugli eventi impostando il flag **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** nella chiamata a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="2f748-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="2f748-171">Associare il client agli esempi pronti per il rendering fornendo un handle di evento al sistema chiamando il metodo [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="2f748-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="2f748-172">Creare un thread di rendering per eseguire gli esempi dal motore audio.</span><span class="sxs-lookup"><span data-stu-id="2f748-172">Create a render thread to proces samples from the audio engine.</span></span>
-   <span data-ttu-id="2f748-173">Controllare il formato di combinazione dell'endpoint del dispositivo per determinare se è possibile eseguire il rendering degli esempi.</span><span class="sxs-lookup"><span data-stu-id="2f748-173">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="2f748-174">Se il dispositivo non supporta il formato di combinazione, i dati vengono convertiti nel PCM.</span><span class="sxs-lookup"><span data-stu-id="2f748-174">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="2f748-175">Gestire il cambio di flusso.</span><span class="sxs-lookup"><span data-stu-id="2f748-175">Handle stream switching.</span></span>

<span data-ttu-id="2f748-176">Dopo l'inizio della sessione di rendering e l'avvio del flusso, il motore audio segnala all'handle di evento fornito di notificare al client ogni volta che un buffer è pronto per l'elaborazione da parte del client.</span><span class="sxs-lookup"><span data-stu-id="2f748-176">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="2f748-177">I dati audio possono anche essere elaborati in un ciclo basato su timer.</span><span class="sxs-lookup"><span data-stu-id="2f748-177">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="2f748-178">Questa modalità è illustrata nell'esempio [RenderSharedTimerDriven](rendersharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="2f748-178">This mode is demonstrated in the [RenderSharedTimerDriven](rendersharedtimerdriven.md) sample.</span></span>

<span data-ttu-id="2f748-179">Per altre informazioni sul rendering di un flusso, vedere [rendering di un flusso](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="2f748-179">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f748-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f748-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f748-181">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="2f748-181">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



