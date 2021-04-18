---
description: In questa applicazione di esempio viene illustrata l'attenuazione dei flussi implementando un lettore multimediale che mostra il comportamento di attenuazione predefinito fornito dal sistema, rifiuta gli eventi ducking e implementa la gestione personalizzata quando vengono ricevuti gli eventi ducking.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320517"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="70917-103">DuckingMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="70917-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="70917-104">In questa applicazione di esempio viene illustrata l'attenuazione dei flussi implementando un lettore multimediale che mostra il comportamento di attenuazione predefinito fornito dal sistema, rifiuta gli eventi ducking e implementa la gestione personalizzata quando vengono ricevuti gli eventi ducking.</span><span class="sxs-lookup"><span data-stu-id="70917-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="70917-105">Questo esempio deve essere usato in ID insieme ad con [DuckingCaptureSample](duckingcapturesample.md).</span><span class="sxs-lookup"><span data-stu-id="70917-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="70917-106">Per altre informazioni sull'attenuazione dei flussi o sull'abbassamento di livello, vedere [esperienza ducking predefinita](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="70917-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="70917-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="70917-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="70917-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70917-108">Description</span></span>](#description)
-   [<span data-ttu-id="70917-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70917-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="70917-110">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70917-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="70917-111">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70917-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="70917-112">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70917-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="70917-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70917-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="70917-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70917-114">Description</span></span>

<span data-ttu-id="70917-115">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="70917-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="70917-116">DirectShow per riprodurre un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="70917-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="70917-117">[WASAPI](wasapi.md) per la gestione del flusso e la gestione degli eventi ducking.</span><span class="sxs-lookup"><span data-stu-id="70917-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="70917-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70917-118">Requirements</span></span>



| <span data-ttu-id="70917-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="70917-119">Product</span></span>                                                        | <span data-ttu-id="70917-120">Versione</span><span class="sxs-lookup"><span data-stu-id="70917-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="70917-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="70917-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="70917-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70917-122">Windows 7</span></span> |
| <span data-ttu-id="70917-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="70917-123">Visual Studio</span></span>                                                  | <span data-ttu-id="70917-124">2008</span><span class="sxs-lookup"><span data-stu-id="70917-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="70917-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70917-125">Downloading the Sample</span></span>

<span data-ttu-id="70917-126">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="70917-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="70917-127">Location</span><span class="sxs-lookup"><span data-stu-id="70917-127">Location</span></span>    | <span data-ttu-id="70917-128">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="70917-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70917-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="70917-129">Windows SDK</span></span> | <span data-ttu-id="70917-130">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ DuckingMediaPlayer \\ ...</span><span class="sxs-lookup"><span data-stu-id="70917-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="70917-131">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70917-131">Building the Sample</span></span>

<span data-ttu-id="70917-132">Per compilare l'esempio DuckingMediaPlayer, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="70917-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="70917-133">Aprire DuckingMediaPlayer. sln in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="70917-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="70917-134">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="70917-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="70917-135">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="70917-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="70917-136">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, DuckingMediaPlayer. vcproj.</span><span class="sxs-lookup"><span data-stu-id="70917-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="70917-137">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70917-137">Running the Sample</span></span>

<span data-ttu-id="70917-138">Se l'applicazione viene compilata correttamente, viene generato un file eseguibile, DuckingMediaPlayer.exe.</span><span class="sxs-lookup"><span data-stu-id="70917-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="70917-139">Per eseguirlo, selezionare **Avvia debug** o **Avvia senza eseguire debug** dal menu **debug** oppure digitare `DuckingMediaPlayer` una finestra di comando.</span><span class="sxs-lookup"><span data-stu-id="70917-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="70917-140">Per visualizzare una dimostrazione di ducking, è necessario eseguire contemporaneamente DuckingMediaPlayer e DuckingCaptureSample.</span><span class="sxs-lookup"><span data-stu-id="70917-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="70917-141">DuckingCaptureSample apre un flusso di comunicazione e segnala al sistema di generare un evento ducking.</span><span class="sxs-lookup"><span data-stu-id="70917-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="70917-142">Il DuckingMediaPlayer riceve una notifica al sistema quando si verifica un evento ducking e il lettore multimediale esegue l'azione richiesta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="70917-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="70917-143">Per disabilitare il comportamento di ducking:</span><span class="sxs-lookup"><span data-stu-id="70917-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="70917-144">Nella finestra DuckingCaptureSample selezionare **USA dispositivo di input predefinito** e fare clic su **Avvia** per avviare una sessione di acquisizione dal dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="70917-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="70917-145">In DuckingMediaPlayer selezionare un file multimediale da riprodurre e specificare l'opzione ducking come **rifiuto esplicito**.</span><span class="sxs-lookup"><span data-stu-id="70917-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="70917-146">Si noti che il file multimediale viene riprodotto senza interruzioni.</span><span class="sxs-lookup"><span data-stu-id="70917-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="70917-147">Gli eventi generati dal sistema quando il flusso di comunicazione aperto vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="70917-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="70917-148">Per illustrare il comportamento predefinito di ducking fornito dal sistema, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="70917-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="70917-149">Selezionare l'opzione **suoni** dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="70917-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="70917-150">Nella scheda **comunicazioni** selezionare **Riduci il volume di altri suoni del 80%**.</span><span class="sxs-lookup"><span data-stu-id="70917-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="70917-151">Nella finestra DuckingCaptureSample selezionare **USA dispositivo di input predefinito** e fare clic su **Avvia** per avviare una sessione di acquisizione dal dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="70917-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="70917-152">In DuckingMediaPlayer selezionare un file multimediale da riprodurre senza scegliere le opzioni di ducking.</span><span class="sxs-lookup"><span data-stu-id="70917-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="70917-153">Nella finestra DuckingCaptureSample fare clic su **Interrompi** per arrestare il flusso di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="70917-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="70917-154">Si noti che quando DuckingCaptureSample apre il flusso di comunicazione, il file multimediale riprodotto da DuckingMediaPlayer viene riprodotto senza interruzioni, ma il livello del volume è ridotto.</span><span class="sxs-lookup"><span data-stu-id="70917-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="70917-155">Quando la sessione di comunicazione viene arrestata, il volume viene reimpostato sull'impostazione originale.</span><span class="sxs-lookup"><span data-stu-id="70917-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="70917-156">Questo comportamento di attenuazione del flusso è il comportamento predefinito di ducking implementato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="70917-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="70917-157">Per visualizzare un comportamento di ducking personalizzato implementato da Media Player:</span><span class="sxs-lookup"><span data-stu-id="70917-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="70917-158">Nella finestra DuckingCaptureSample selezionare **USA dispositivo di input predefinito** e fare clic su **Avvia** per avviare una sessione di acquisizione dal dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="70917-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="70917-159">In DuckingMediaPlayer selezionare un file multimediale da riprodurre e specificare l'opzione ducking come **pausa in Duck**.</span><span class="sxs-lookup"><span data-stu-id="70917-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="70917-160">Nella finestra DuckingCaptureSample fare clic su **Interrompi** per arrestare il flusso di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="70917-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="70917-161">Si noti che quando DuckingCaptureSample apre il flusso di comunicazione, il file multimediale riprodotto da DuckingMediaPlayer viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="70917-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="70917-162">La riproduzione riprende quando la sessione di comunicazione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="70917-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="70917-163">Questo comportamento di attenuazione del flusso è il comportamento di ducking implementato da Media Player.</span><span class="sxs-lookup"><span data-stu-id="70917-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="70917-164">DuckingMediaPlayer illustra anche come integrare il controllo del volume per ogni applicazione con il mixer del volume.</span><span class="sxs-lookup"><span data-stu-id="70917-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="70917-165">Per ulteriori informazioni sulla funzionalità di attenuazione dei flussi, vedere l' [esperienza di ducking predefinita](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="70917-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70917-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70917-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70917-167">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="70917-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



