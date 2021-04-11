---
description: Questo esempio usa le API audio principali per acquisire un flusso vocale di alta qualità. L'esempio supporta l'elaborazione dell'annullamento acustico Echo (AEC) e dell'array di microfoni usando l'AEC DMO, detto anche DSP di acquisizione vocale, fornito da Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127678"
---
# <a name="aecmicarray"></a><span data-ttu-id="165b3-104">AECMicArray</span><span class="sxs-lookup"><span data-stu-id="165b3-104">AECMicArray</span></span>

<span data-ttu-id="165b3-105">Questo esempio usa le API audio principali per acquisire un flusso vocale di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="165b3-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="165b3-106">L'esempio supporta l'elaborazione dell'annullamento acustico Echo (AEC) e dell'array di microfoni usando l'AEC DMO, detto anche DSP di acquisizione vocale, fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="165b3-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="165b3-107">Questo argomento contiene le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="165b3-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="165b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="165b3-108">Description</span></span>](#description)
-   [<span data-ttu-id="165b3-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="165b3-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="165b3-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="165b3-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="165b3-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="165b3-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="165b3-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="165b3-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="165b3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="165b3-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="165b3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="165b3-114">Description</span></span>

<span data-ttu-id="165b3-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="165b3-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="165b3-116">[MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="165b3-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="165b3-117">[WASAPI](wasapi.md) per le operazioni di gestione del flusso, ad esempio l'avvio e l'arresto del flusso, il cambio di flusso.</span><span class="sxs-lookup"><span data-stu-id="165b3-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="165b3-118">[DeviceTopology](devicetopology-api.md) per l'enumerazione di schede audio.</span><span class="sxs-lookup"><span data-stu-id="165b3-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="165b3-119">[EndpointVolume](endpointvolume-api.md) controllano i livelli di volume delle [sessioni audio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="165b3-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="165b3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="165b3-120">Requirements</span></span>



| <span data-ttu-id="165b3-121">Prodotto</span><span class="sxs-lookup"><span data-stu-id="165b3-121">Product</span></span>                                                        | <span data-ttu-id="165b3-122">Versione</span><span class="sxs-lookup"><span data-stu-id="165b3-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="165b3-123">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="165b3-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="165b3-124">Windows Vista o versioni successive</span><span class="sxs-lookup"><span data-stu-id="165b3-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="165b3-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="165b3-125">Visual Studio</span></span>                                                  | <span data-ttu-id="165b3-126">2005 (edizioni non Express)</span><span class="sxs-lookup"><span data-stu-id="165b3-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="165b3-127">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="165b3-127">Downloading the Sample</span></span>

<span data-ttu-id="165b3-128">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="165b3-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="165b3-129">Location</span><span class="sxs-lookup"><span data-stu-id="165b3-129">Location</span></span>    | <span data-ttu-id="165b3-130">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="165b3-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="165b3-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="165b3-131">Windows SDK</span></span> | <span data-ttu-id="165b3-132">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ AECMicArray \\ ...</span><span class="sxs-lookup"><span data-stu-id="165b3-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="165b3-133">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="165b3-133">Building the Sample</span></span>

<span data-ttu-id="165b3-134">Per compilare l'esempio AecSDKDemo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="165b3-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="165b3-135">Aprire una finestra di comando di SDK.</span><span class="sxs-lookup"><span data-stu-id="165b3-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="165b3-136">Digitare **CD% MSSDK% \\ Setup**.</span><span class="sxs-lookup"><span data-stu-id="165b3-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="165b3-137">Eseguire VCIntegrate.exe.</span><span class="sxs-lookup"><span data-stu-id="165b3-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="165b3-138">Da questo punto in poi, le finestre di comando avranno le impostazioni di ambiente appropriate per creare un'applicazione che sfrutta i vantaggi dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="165b3-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="165b3-139">Compilare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="165b3-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="165b3-140">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="165b3-140">Running the Sample</span></span>

<span data-ttu-id="165b3-141">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile AecSDKDemo.exe.</span><span class="sxs-lookup"><span data-stu-id="165b3-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="165b3-142">Per eseguirlo, digitare `AecSDKDemo` una finestra di comando seguita da argomenti obbligatori o facoltativi, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="165b3-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="165b3-143">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="165b3-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="165b3-144">Argomento</span><span class="sxs-lookup"><span data-stu-id="165b3-144">Argument</span></span>  | <span data-ttu-id="165b3-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="165b3-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="165b3-146">-out</span><span class="sxs-lookup"><span data-stu-id="165b3-146">-out</span></span>      | <span data-ttu-id="165b3-147">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="165b3-147">Required.</span></span> <span data-ttu-id="165b3-148">Specifica il nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="165b3-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="165b3-149">-mod</span><span class="sxs-lookup"><span data-stu-id="165b3-149">-mod</span></span>      | <span data-ttu-id="165b3-150">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="165b3-150">Required.</span></span> <span data-ttu-id="165b3-151">Specifica la modalità del sistema di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="165b3-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="165b3-152">Per informazioni dettagliate, vedere la sezione "configurazione della funzionalità di acquisizione voce DMO" nel file Leggimi di esempio.</span><span class="sxs-lookup"><span data-stu-id="165b3-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="165b3-153">-feat</span><span class="sxs-lookup"><span data-stu-id="165b3-153">-feat</span></span>     | <span data-ttu-id="165b3-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-154">Optional.</span></span> <span data-ttu-id="165b3-155">Attiva la modalità della funzionalità attivata (1) o disattivata (0).</span><span class="sxs-lookup"><span data-stu-id="165b3-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="165b3-156">-NS</span><span class="sxs-lookup"><span data-stu-id="165b3-156">-ns</span></span>       | <span data-ttu-id="165b3-157">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-157">Optional.</span></span> <span data-ttu-id="165b3-158">Attiva l'eliminazione del rumore (1) o disattivato (0).</span><span class="sxs-lookup"><span data-stu-id="165b3-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="165b3-159">Per specificare questa opzione, è necessario che la modalità funzionalità sia attiva.</span><span class="sxs-lookup"><span data-stu-id="165b3-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="165b3-160">-AGC</span><span class="sxs-lookup"><span data-stu-id="165b3-160">-agc</span></span>      | <span data-ttu-id="165b3-161">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-161">Optional.</span></span> <span data-ttu-id="165b3-162">Attiva il CAG digitale (1) o disattivato (0).</span><span class="sxs-lookup"><span data-stu-id="165b3-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="165b3-163">Per specificare questa opzione, è necessario che la modalità funzionalità sia attiva.</span><span class="sxs-lookup"><span data-stu-id="165b3-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="165b3-164">-cntrclip</span><span class="sxs-lookup"><span data-stu-id="165b3-164">-cntrclip</span></span> | <span data-ttu-id="165b3-165">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-165">Optional.</span></span> <span data-ttu-id="165b3-166">Attiva il ritaglio al centro (1) o disattivato (0).</span><span class="sxs-lookup"><span data-stu-id="165b3-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="165b3-167">Per specificare questa opzione, è necessario che la modalità funzionalità sia attiva.</span><span class="sxs-lookup"><span data-stu-id="165b3-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="165b3-168">-spkdev</span><span class="sxs-lookup"><span data-stu-id="165b3-168">-spkdev</span></span>   | <span data-ttu-id="165b3-169">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-169">Optional.</span></span> <span data-ttu-id="165b3-170">Specifica l'indice del dispositivo speaker.</span><span class="sxs-lookup"><span data-stu-id="165b3-170">Specifies speaker device index.</span></span> <span data-ttu-id="165b3-171">Se non specificato, all'utente verrà richiesto di effettuare la selezione.</span><span class="sxs-lookup"><span data-stu-id="165b3-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="165b3-172">-micdev</span><span class="sxs-lookup"><span data-stu-id="165b3-172">-micdev</span></span>   | <span data-ttu-id="165b3-173">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-173">Optional.</span></span> <span data-ttu-id="165b3-174">Specifica l'indice del dispositivo microfonico.</span><span class="sxs-lookup"><span data-stu-id="165b3-174">Specifies microphone device index.</span></span> <span data-ttu-id="165b3-175">Se non specificato, all'utente verrà richiesto di effettuare la selezione.</span><span class="sxs-lookup"><span data-stu-id="165b3-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="165b3-176">-durata</span><span class="sxs-lookup"><span data-stu-id="165b3-176">-duration</span></span> | <span data-ttu-id="165b3-177">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="165b3-177">Optional.</span></span> <span data-ttu-id="165b3-178">Specifica la durata dell'esecuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="165b3-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="165b3-179">Questa applicazione di esempio non riproduce alcun segnale.</span><span class="sxs-lookup"><span data-stu-id="165b3-179">This sample application does not play any signals.</span></span> <span data-ttu-id="165b3-180">Per eseguire la demo correttamente per le modalità abilitate per AEC (modalità 0 e 4), gli utenti devono riprodurre alcuni segnali audio tramite lo stesso dispositivo speaker specificato per DMO (ovvero il dispositivo specificato dall'opzione "-spkdev"), che simula la voce finale in uno scenario di chat bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="165b3-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="165b3-181">Gli utenti possono usare qualsiasi lettore per riprodurre segnali audio.</span><span class="sxs-lookup"><span data-stu-id="165b3-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="165b3-182">Se non è presente alcun flusso di rendering attivo sul dispositivo altoparlante selezionato, l'operazione DMO non verrà elaborata.</span><span class="sxs-lookup"><span data-stu-id="165b3-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="165b3-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="165b3-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="165b3-184">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="165b3-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



