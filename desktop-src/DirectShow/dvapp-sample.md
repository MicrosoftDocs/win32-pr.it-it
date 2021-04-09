---
description: Esempio DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Esempio DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124827"
---
# <a name="dvapp-sample"></a><span data-ttu-id="cffa0-103">Esempio DVApp</span><span class="sxs-lookup"><span data-stu-id="cffa0-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="cffa0-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cffa0-104">Description</span></span>

<span data-ttu-id="cffa0-105">Applicazione di acquisizione video digitale (DV).</span><span class="sxs-lookup"><span data-stu-id="cffa0-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="cffa0-106">Questo esempio illustra come creare vari tipi di grafici di filtro per il controllo di videocamere DV.</span><span class="sxs-lookup"><span data-stu-id="cffa0-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="cffa0-107">Viene inoltre illustrato come eseguire il controllo di acquisizione, anteprima, trasmissione e dispositivo con una videocamera DV.</span><span class="sxs-lookup"><span data-stu-id="cffa0-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="cffa0-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="cffa0-108">Usage</span></span>

<span data-ttu-id="cffa0-109">L'applicazione DVApp supporta le modalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="cffa0-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="cffa0-110">Anteprima: esegue il rendering di DV dalla videocamera a una finestra del video.</span><span class="sxs-lookup"><span data-stu-id="cffa0-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="cffa0-111">Da DV a file di tipo-1: acquisisce i dati DV dalla videocamera in un file DV di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="cffa0-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="cffa0-112">Digitare-1 file in DV: trasmette i dati da un file DV di tipo 1 alla videocamera.</span><span class="sxs-lookup"><span data-stu-id="cffa0-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="cffa0-113">Da DV a file di tipo 2: acquisisce i dati DV dalla videocamera a un file DV di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="cffa0-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="cffa0-114">Digitare-2 file in DV: trasmette i dati da un file DV di tipo 2 alla videocamera.</span><span class="sxs-lookup"><span data-stu-id="cffa0-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="cffa0-115">Anche le modalità di acquisizione e trasmissione eseguono l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="cffa0-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="cffa0-116">Ognuna di queste modalità non include anche un'opzione di **Anteprima** , che disabilita l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="cffa0-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="cffa0-117">L'acquisizione senza anteprima è più efficiente e può ridurre il numero di frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="cffa0-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="cffa0-118">L'applicazione viene avviata in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="cffa0-118">The application starts in preview mode.</span></span> <span data-ttu-id="cffa0-119">Per selezionare un'altra modalità, scegliere una modalità dal menu **modalità grafico** .</span><span class="sxs-lookup"><span data-stu-id="cffa0-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="cffa0-120">Per ogni modalità, DVApp compila un grafico di filtro che supporta la funzionalità di tale modalità.</span><span class="sxs-lookup"><span data-stu-id="cffa0-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="cffa0-121">Per salvare il grafico come file GraphEdit (. GRF), selezionare **Salva grafico in file** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="cffa0-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="cffa0-122">Uscire da DVApp prima di aprire il file in GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="cffa0-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="cffa0-123">Per acquisire in un file:</span><span class="sxs-lookup"><span data-stu-id="cffa0-123">To capture to a file:</span></span>

1.  <span data-ttu-id="cffa0-124">Scegliere **Imposta file di output** dal menu **file** e immettere un nome file.</span><span class="sxs-lookup"><span data-stu-id="cffa0-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="cffa0-125">Dal menu **modalità grafico** selezionare un *DV in modalità file* (digitare 1 o digitare 2, con o senza anteprima).</span><span class="sxs-lookup"><span data-stu-id="cffa0-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="cffa0-126">Fare clic su **record**.</span><span class="sxs-lookup"><span data-stu-id="cffa0-126">Click **Record**.</span></span>
4.  <span data-ttu-id="cffa0-127">Se la videocamera è in modalità VTR, fare clic su **Riproduci**.</span><span class="sxs-lookup"><span data-stu-id="cffa0-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="cffa0-128">Per arrestare l'acquisizione, fare clic su **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="cffa0-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="cffa0-129">Per trasmettere da un file alla videocamera:</span><span class="sxs-lookup"><span data-stu-id="cffa0-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="cffa0-130">Scegliere **Imposta file di input** dal menu **file** e selezionare un file DV.</span><span class="sxs-lookup"><span data-stu-id="cffa0-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="cffa0-131">Il file deve corrispondere alla modalità selezionata (tipo 1 o tipo 2).</span><span class="sxs-lookup"><span data-stu-id="cffa0-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="cffa0-132">Dal menu **modalità grafico** selezionare un *file in modalità DV* (digitare 1 o digitare 2, con o senza anteprima).</span><span class="sxs-lookup"><span data-stu-id="cffa0-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="cffa0-133">Fare clic su **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="cffa0-133">Click **Play**.</span></span>
4.  <span data-ttu-id="cffa0-134">Per registrare i dati su nastro, fare clic su **registra**.</span><span class="sxs-lookup"><span data-stu-id="cffa0-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="cffa0-135">Per arrestare la trasmissione, fare clic su **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="cffa0-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="cffa0-136">Se la videocamera è in modalità VTR, l'utente può controllare il meccanismo di trasporto tramite i pulsanti di tipo VCR dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cffa0-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="cffa0-137">Per cercare il nastro, immettere il timecode di destinazione e fare clic sul pulsante Seek (Cerca).</span><span class="sxs-lookup"><span data-stu-id="cffa0-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="cffa0-138">Per limitare la quantità di dati che l'applicazione acquisisce, scegliere **dimensioni acquisizione** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="cffa0-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="cffa0-139">Per controllare il formato del nastro (NTSC o PAL), scegliere **Controlla nastro** dal menu **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="cffa0-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="cffa0-140">Per modificare le dimensioni della finestra di anteprima, scegliere **modifica dimensioni decodifica** dal menu **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="cffa0-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="cffa0-141">Note sulla programmazione</span><span class="sxs-lookup"><span data-stu-id="cffa0-141">Programming Notes</span></span>

<span data-ttu-id="cffa0-142">Lo scopo principale di questa applicazione è mostrare come compilare diversi grafici di acquisizione e trasmissione DV.</span><span class="sxs-lookup"><span data-stu-id="cffa0-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="cffa0-143">Arrivo e rimozione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="cffa0-143">Device Arrival and Removal</span></span>

<span data-ttu-id="cffa0-144">L'applicazione gestisce l'arrivo e la rimozione dei dispositivi, usando due tecniche diverse.</span><span class="sxs-lookup"><span data-stu-id="cffa0-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="cffa0-145">Per l'arrivo del dispositivo, il ciclo di messaggi dell'applicazione risponde ai \_ messaggi WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="cffa0-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="cffa0-146">Per la rimozione dei dispositivi, l'applicazione risponde agli eventi di [**\_ \_ perdita del dispositivo EC**](ec-device-lost.md) dal gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="cffa0-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="cffa0-147">Entrambi gli approcci funzionano, sebbene l' \_ \_ evento di perdita del dispositivo EC dipenda dall'esistenza del dispositivo nel grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="cffa0-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="cffa0-148">L'applicazione gestisce solo un dispositivo alla volta.</span><span class="sxs-lookup"><span data-stu-id="cffa0-148">The application only handles one device at a time.</span></span> <span data-ttu-id="cffa0-149">Se il dispositivo corrente viene rimosso, l'applicazione cerca un altro dispositivo DV nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cffa0-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="cffa0-150">In alcuni camcorder DV, l'utente deve spegnere il dispositivo quando lo passa tra la modalità videocamera e la modalità VTR, che attiva un messaggio perso dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cffa0-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="cffa0-151">L'applicazione risponde abilitando o disabilitando i comandi di menu appropriati.</span><span class="sxs-lookup"><span data-stu-id="cffa0-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="cffa0-152">Tuttavia, se l'utente passa rapidamente tra le modalità, la videocamera potrebbe non generare un messaggio perso dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cffa0-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="cffa0-153">È possibile forzare l'aggiornamento dei menu scegliendo **modalità di aggiornamento** dal menu **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="cffa0-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="cffa0-154">Alcuni camcorder DV possono attivare o disattivare le modalità senza arrestare, ma inviare un messaggio perso dal dispositivo solo quando passano alla modalità VTR.</span><span class="sxs-lookup"><span data-stu-id="cffa0-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="cffa0-155">Controllo dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="cffa0-155">Device Control</span></span>

<span data-ttu-id="cffa0-156">La funzionalità del pulsante **Riproduci** e **registra** dipende dalla modalità corrente:</span><span class="sxs-lookup"><span data-stu-id="cffa0-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="cffa0-157">Anteprima: il grafico del filtro viene eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cffa0-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="cffa0-158">Il pulsante **Riproduci** avvia il trasporto.</span><span class="sxs-lookup"><span data-stu-id="cffa0-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="cffa0-159">Acquisisci nel file: il pulsante **registra** esegue il grafico e il pulsante **Riproduci** avvia il trasporto.</span><span class="sxs-lookup"><span data-stu-id="cffa0-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="cffa0-160">Trasmissione al dispositivo: il pulsante **Riproduci** esegue il grafico e il pulsante **registra** avvia il trasporto.</span><span class="sxs-lookup"><span data-stu-id="cffa0-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="cffa0-161">L'applicazione di esempio non esegue un'acquisizione accurata del frame.</span><span class="sxs-lookup"><span data-stu-id="cffa0-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="cffa0-162">In vari punti, l'applicazione chiama la funzione di **sospensione** per attendere la risposta del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cffa0-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="cffa0-163">I camcorder DV più recenti inviano una notifica quando lo stato del dispositivo cambia.</span><span class="sxs-lookup"><span data-stu-id="cffa0-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="cffa0-164">I dispositivi meno recenti potrebbero non supportare la notifica; ai fini di un esempio, la chiamata a **Sleep** è una soluzione più semplice.</span><span class="sxs-lookup"><span data-stu-id="cffa0-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="cffa0-165">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cffa0-165">Downloading the Sample</span></span>

<span data-ttu-id="cffa0-166">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cffa0-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="cffa0-167">Questo esempio viene installato nel percorso seguente: *\[ SDK \] radice* \\ esempi \\ Multimedia \\ DirectShow \\ Capture \\ DVApp.</span><span class="sxs-lookup"><span data-stu-id="cffa0-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cffa0-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cffa0-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cffa0-169">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="cffa0-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="cffa0-170">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cffa0-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="cffa0-171">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="cffa0-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



