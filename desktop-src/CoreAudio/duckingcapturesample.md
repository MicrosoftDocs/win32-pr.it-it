---
description: Questa applicazione di esempio illustra l'apertura e la chiusura di flussi di comunicazione e la generazione di eventi ducking che un'applicazione può ottenere per implementare l'attenuazione del flusso.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878334"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="b74d3-103">DuckingCaptureSample</span><span class="sxs-lookup"><span data-stu-id="b74d3-103">DuckingCaptureSample</span></span>

<span data-ttu-id="b74d3-104">Questa applicazione di esempio illustra l'apertura e la chiusura di flussi di comunicazione e la generazione di eventi ducking che un'applicazione può ottenere per implementare l'attenuazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="b74d3-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="b74d3-105">Questa applicazione implementa un client di chat che usa le API audio principali per leggere i dati audio da un dispositivo di comunicazione e riprodurli sul dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="b74d3-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="b74d3-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b74d3-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b74d3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b74d3-107">Description</span></span>](#description)
-   [<span data-ttu-id="b74d3-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b74d3-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b74d3-109">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b74d3-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b74d3-110">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b74d3-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b74d3-111">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b74d3-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b74d3-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b74d3-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b74d3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b74d3-113">Description</span></span>

<span data-ttu-id="b74d3-114">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="b74d3-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="b74d3-115">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="b74d3-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="b74d3-116">[WASAPI](wasapi.md) per l'accesso al dispositivo di acquisizione e rendering delle comunicazioni, alle operazioni di gestione del flusso e alla gestione degli eventi ducking.</span><span class="sxs-lookup"><span data-stu-id="b74d3-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="b74d3-117">[API Wave](/previous-versions//ms713499(v=vs.85)) per accedere al dispositivo di comunicazione e acquisire l'input audio.</span><span class="sxs-lookup"><span data-stu-id="b74d3-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74d3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b74d3-118">Requirements</span></span>



| <span data-ttu-id="b74d3-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b74d3-119">Product</span></span>                                                        | <span data-ttu-id="b74d3-120">Versione</span><span class="sxs-lookup"><span data-stu-id="b74d3-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b74d3-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b74d3-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b74d3-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b74d3-122">Windows 7</span></span> |
| <span data-ttu-id="b74d3-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="b74d3-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b74d3-124">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b74d3-124">Downloading the Sample</span></span>

<span data-ttu-id="b74d3-125">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b74d3-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="b74d3-126">Location</span><span class="sxs-lookup"><span data-stu-id="b74d3-126">Location</span></span>    | <span data-ttu-id="b74d3-127">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="b74d3-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b74d3-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b74d3-128">Windows SDK</span></span> | <span data-ttu-id="b74d3-129">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ DuckingCaptureSample \\ ...</span><span class="sxs-lookup"><span data-stu-id="b74d3-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="b74d3-130">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b74d3-130">Building the Sample</span></span>

<span data-ttu-id="b74d3-131">Per compilare l'esempio DuckingCaptureSample, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="b74d3-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="b74d3-132">Aprire DuckingCaptureSample. sln in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b74d3-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="b74d3-133">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="b74d3-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="b74d3-134">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="b74d3-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="b74d3-135">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, DuckingCaptureSample. vcproj.</span><span class="sxs-lookup"><span data-stu-id="b74d3-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b74d3-136">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b74d3-136">Running the Sample</span></span>

<span data-ttu-id="b74d3-137">Se l'applicazione viene compilata correttamente, viene generato un file eseguibile, DuckingCaptureSample.exe.</span><span class="sxs-lookup"><span data-stu-id="b74d3-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="b74d3-138">Per eseguirlo, selezionare **Avvia debug** o **Avvia senza eseguire debug** dal menu **debug** oppure digitare `DuckingCaptureSample` una finestra di comando.</span><span class="sxs-lookup"><span data-stu-id="b74d3-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="b74d3-139">DuckingCaptureSample fornisce all'utente due implementazioni per acquisire l'audio dal dispositivo console predefinito: WASAPI e le API Wave.</span><span class="sxs-lookup"><span data-stu-id="b74d3-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="b74d3-140">Per avviare una sessione di acquisizione, selezionare una modalità e fare clic su **Avvia** nell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b74d3-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="b74d3-141">Per terminare la sessione, fare clic su **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="b74d3-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="b74d3-142">A seconda del dispositivo specificato dall'utente (input o output), l'applicazione usa l'API MMDevice per ottenere un riferimento al dispositivo di comunicazione predefinito di rendering o acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b74d3-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="b74d3-143">Dopo l'avvio di una sessione di chat da parte dell'utente, l'applicazione esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="b74d3-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="b74d3-144">Crea e Inizializza un client audio in modalità guidata dagli eventi.</span><span class="sxs-lookup"><span data-stu-id="b74d3-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="b74d3-145">Associa il client all'handle di evento che segnala che gli esempi sono pronti per l'acquisizione o il rendering.</span><span class="sxs-lookup"><span data-stu-id="b74d3-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="b74d3-146">Imposta un client di acquisizione e un client di rendering per il trasporto.</span><span class="sxs-lookup"><span data-stu-id="b74d3-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="b74d3-147">Crea il thread di chat e avvia il motore audio.</span><span class="sxs-lookup"><span data-stu-id="b74d3-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="b74d3-148">Per l'acquisizione di dati audio, a ogni passaggio di elaborazione, l'esempio usa il client di acquisizione per ottenere la quantità totale di dati acquisiti disponibili nel buffer, leggere i dati dal dispositivo di input predefinito e rilasciare il pacchetto e rendere disponibile il buffer per la lettura del set successivo di dati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="b74d3-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="b74d3-149">Per il rendering, l'applicazione determina la quantità di dati accodati per la riproduzione nel buffer dell'endpoint di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b74d3-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="b74d3-150">Scrive di conseguenza nel buffer e rilascia il buffer in preparazione al successivo passaggio di elaborazione fino a quando tutti i dati non sono stati scritti.</span><span class="sxs-lookup"><span data-stu-id="b74d3-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="b74d3-151">Per il rendering, i frame invisibili vengono preregistrati per impedire che il motore audio si inconvenienti all'avvio.</span><span class="sxs-lookup"><span data-stu-id="b74d3-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="b74d3-152">DuckingCaptureSample Mostra anche come nascondere il flusso di rendering dal mixer del volume.</span><span class="sxs-lookup"><span data-stu-id="b74d3-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="b74d3-153">Per altre informazioni sulla funzionalità di attenuazione dei flussi, vedere [uso di un dispositivo di comunicazione](using-the-communication-device.md).</span><span class="sxs-lookup"><span data-stu-id="b74d3-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b74d3-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b74d3-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b74d3-155">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="b74d3-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
