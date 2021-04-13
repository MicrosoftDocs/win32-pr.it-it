---
title: Informazioni sul monitoraggio delle cartelle
description: Informazioni sul monitoraggio delle cartelle
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, monitoraggio cartelle
- Modello a oggetti di Windows Media Player, monitoraggio delle cartelle
- modello a oggetti, monitoraggio delle cartelle
- Controllo ActiveX Windows Media Player, monitoraggio cartelle
- Controllo ActiveX, monitoraggio cartelle
- Controllo ActiveX Windows Media Player Mobile, monitoraggio cartelle
- Windows Media Player Mobile, monitoraggio cartelle
- monitoraggio cartelle
- cartelle di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398537"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="1208c-112">Informazioni sul monitoraggio delle cartelle</span><span class="sxs-lookup"><span data-stu-id="1208c-112">About Folder Monitoring</span></span>

<span data-ttu-id="1208c-113">Windows Media Player può monitorare le cartelle che contengono file multimediali digitali e aggiornare la libreria quando i file vengono aggiunti o rimossi.</span><span class="sxs-lookup"><span data-stu-id="1208c-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="1208c-114">Questa funzionalità di monitoraggio della cartella viene fornita dall'interfaccia [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .</span><span class="sxs-lookup"><span data-stu-id="1208c-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="1208c-115">Per utilizzare i servizi di monitoraggio delle cartelle, è necessario creare l'oggetto Player in uno stato remoto.</span><span class="sxs-lookup"><span data-stu-id="1208c-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="1208c-116">Per ulteriori informazioni sulla comunicazione remota, vedere la pagina relativa [ai servizi remoti di Windows Media Player](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="1208c-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="1208c-117">Dopo aver creato un'istanza remota del lettore, ottenere un puntatore all'interfaccia **IWMPFolderMonitorServices** chiamando **QueryInterface** sull'interfaccia [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .</span><span class="sxs-lookup"><span data-stu-id="1208c-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="1208c-118">Windows Media Player mantiene un elenco di cartelle monitorate.</span><span class="sxs-lookup"><span data-stu-id="1208c-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="1208c-119">Per ottenere un elenco delle cartelle monitorate, usare i metodi [IWMPFolderMonitorServices:: Get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) e [IWMPFolderMonitorServices:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) .</span><span class="sxs-lookup"><span data-stu-id="1208c-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="1208c-120">Per aggiungere cartelle all'elenco o rimuoverle dall'elenco, usare rispettivamente i metodi [IWMPFolderMonitorServices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) e [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) .</span><span class="sxs-lookup"><span data-stu-id="1208c-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="1208c-121">**Avvio di un'analisi**</span><span class="sxs-lookup"><span data-stu-id="1208c-121">**Starting a Scan**</span></span>

<span data-ttu-id="1208c-122">Il monitoraggio delle cartelle è in genere un processo in background che non deve essere chiamato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1208c-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="1208c-123">Se si desidera eseguire l'analisi attiva di una cartella, chiamare [IWMPFolderMonitorServices:: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span><span class="sxs-lookup"><span data-stu-id="1208c-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="1208c-124">È possibile arrestare un'analisi in corso con il metodo [IWMPFolderMonitorServices:: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .</span><span class="sxs-lookup"><span data-stu-id="1208c-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="1208c-125">**Recupero dello stato di monitoraggio della cartella**</span><span class="sxs-lookup"><span data-stu-id="1208c-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="1208c-126">**IWMPFolderMonitorServices** fornisce funzionalità per il recupero dello stato del processo di monitoraggio della cartella.</span><span class="sxs-lookup"><span data-stu-id="1208c-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="1208c-127">L'analisi delle cartelle viene eseguita in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="1208c-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="1208c-128">Nel primo passaggio, il lettore analizza le cartelle denominate nell'elenco cartelle monitorate una alla volta e compila un elenco di file da aggiungere alla libreria.</span><span class="sxs-lookup"><span data-stu-id="1208c-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="1208c-129">Nel secondo passaggio, viene eseguito l'elenco dei file e i file vengono aggiunti alla libreria e vengono rimossi anche tutti gli elementi multimediali dalla libreria i cui file fisici corrispondenti sono stati eliminati dal file system.</span><span class="sxs-lookup"><span data-stu-id="1208c-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="1208c-130">L'evento [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) viene usato per notificare al programma ogni volta che il giocatore passa a un nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="1208c-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="1208c-131">È anche possibile recuperare lo stato corrente chiamando [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span><span class="sxs-lookup"><span data-stu-id="1208c-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="1208c-132">Quando viene avviato il primo passaggio, il valore dello stato corrente è wmpfssScanning.</span><span class="sxs-lookup"><span data-stu-id="1208c-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="1208c-133">Durante il secondo passaggio, lo stato passa a wmpfssUpdating.</span><span class="sxs-lookup"><span data-stu-id="1208c-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="1208c-134">Al termine del processo, lo stato passa a wmpfssStopped.</span><span class="sxs-lookup"><span data-stu-id="1208c-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="1208c-135">Mentre il lettore esegue l'analisi delle cartelle monitorate al primo passaggio, chiamare [get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) per verificare il numero di file analizzati.</span><span class="sxs-lookup"><span data-stu-id="1208c-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="1208c-136">Il metodo [get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) indica la cartella attualmente sottoposta a scansione.</span><span class="sxs-lookup"><span data-stu-id="1208c-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="1208c-137">Una volta avviato il secondo passaggio, chiamare [get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) per verificare il numero di file aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="1208c-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="1208c-138">Il metodo [get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) indica lo stato del secondo passaggio, come percentuale da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="1208c-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1208c-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1208c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1208c-140">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="1208c-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="1208c-141">**Interfaccia IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="1208c-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




