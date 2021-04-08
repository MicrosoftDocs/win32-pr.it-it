---
title: Panoramica di Download Manager
description: Panoramica di Download Manager
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, Download in tempo reale
- negozi online, Download in tempo reale
- digitare 2 negozi online, Download in tempo reale
- Windows Media Player Online Stores, Download in background
- negozi online, Download in background
- digitare 2 negozi online, Download in background
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- Download in tempo reale
- Download in background
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045259"
---
# <a name="download-manager-overview"></a><span data-ttu-id="466ff-117">Panoramica di Download Manager</span><span class="sxs-lookup"><span data-stu-id="466ff-117">Download Manager Overview</span></span>

<span data-ttu-id="466ff-118">Microsoft Windows Media Player fornisce riquadri attività di archivio online che contengono una finestra del browser ospitata.</span><span class="sxs-lookup"><span data-stu-id="466ff-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="466ff-119">Tramite gli archivi online, gli utenti possono interagire con le pagine Web del negozio online tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="466ff-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="466ff-120">Windows Media Player Download Manager fornisce un modello a oggetti che è possibile utilizzare per gestire le attività associate al download del contenuto nel computer dell'utente da Microsoft Internet Information Services (IIS) tramite Hypertext Transfer Protocol (HTTP).</span><span class="sxs-lookup"><span data-stu-id="466ff-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="466ff-121">Con Download Manager è possibile:</span><span class="sxs-lookup"><span data-stu-id="466ff-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="466ff-122">Gestione simultanea di più download come raccolta.</span><span class="sxs-lookup"><span data-stu-id="466ff-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="466ff-123">Specificare un URL per un file e avviarlo scaricando tramite HTTP.</span><span class="sxs-lookup"><span data-stu-id="466ff-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="466ff-124">Eseguire una query per lo stato di download e lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="466ff-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="466ff-125">Sospendere, riprendere o annullare un download.</span><span class="sxs-lookup"><span data-stu-id="466ff-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="466ff-126">Consente di specificare se un download viene eseguito in background o in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="466ff-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="466ff-127">Il download in background è disponibile solo nel sistema operativo Microsoft Windows XP. Vedere [informazioni sul download in background e in tempo reale](#about-background-and-real-time-downloading).</span><span class="sxs-lookup"><span data-stu-id="466ff-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="466ff-128">Consente di specificare la modalità di visualizzazione del contenuto nella libreria.</span><span class="sxs-lookup"><span data-stu-id="466ff-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="466ff-129">Vedere [informazioni sull'integrazione della libreria](#about-library-integration).</span><span class="sxs-lookup"><span data-stu-id="466ff-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="466ff-130">Download Manager è la soluzione per scaricare il contenuto dal codice di script nelle pagine Web ospitate.</span><span class="sxs-lookup"><span data-stu-id="466ff-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="466ff-131">Per scaricare il contenuto usando il codice C++, usare il Servizio trasferimento intelligente in background di Windows XP (BITS).</span><span class="sxs-lookup"><span data-stu-id="466ff-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="466ff-132">Per ulteriori informazioni, vedere [bits](bits.md).</span><span class="sxs-lookup"><span data-stu-id="466ff-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="466ff-133">Informazioni sul download in tempo reale e in background</span><span class="sxs-lookup"><span data-stu-id="466ff-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="466ff-134">Download Manager offre due tipi di download: background e in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="466ff-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="466ff-135">Il tipo usato dipende dall'utente ed è possibile consentire all'utente di selezionare anche il tipo di download.</span><span class="sxs-lookup"><span data-stu-id="466ff-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="466ff-136">Se si sceglie di consentire all'utente di selezionare il tipo di download, assicurarsi di illustrare le differenze tra i due tipi disponibili.</span><span class="sxs-lookup"><span data-stu-id="466ff-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="466ff-137">Il download in tempo reale si verifica in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="466ff-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="466ff-138">Quando l'utente avvia un download di file, l'intero file viene trasferito al computer dell'utente in un unico flusso continuo.</span><span class="sxs-lookup"><span data-stu-id="466ff-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="466ff-139">L'utente non è in grado di sospendere o interrompere il download.</span><span class="sxs-lookup"><span data-stu-id="466ff-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="466ff-140">Se l'utente sceglie di chiudere Windows Media Player prima del completamento del download, perderà tutti i file incompleti ed è necessario scaricarli dall'inizio per acquisire il contenuto.</span><span class="sxs-lookup"><span data-stu-id="466ff-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="466ff-141">Il vantaggio principale del download in tempo reale è che consente all'utente di acquisire il contenuto più velocemente rispetto al download in background.</span><span class="sxs-lookup"><span data-stu-id="466ff-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="466ff-142">Il download in tempo reale è disponibile per gli utenti di Windows XP, ma è l'unico tipo di download disponibile nelle versioni del sistema operativo Windows precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="466ff-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="466ff-143">Il download in background avviene in modo a fasi.</span><span class="sxs-lookup"><span data-stu-id="466ff-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="466ff-144">Quando l'utente avvia un download in background, le parti del file vengono trasferite nel computer dell'utente quando è disponibile il tempo del processore.</span><span class="sxs-lookup"><span data-stu-id="466ff-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="466ff-145">È possibile sospendere e riprendere un download in background.</span><span class="sxs-lookup"><span data-stu-id="466ff-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="466ff-146">Se l'utente sceglie di chiudere Windows Media Player prima del completamento del download dello sfondo, la condizione dei file incompleti viene salvata e il download può continuare in background, anche dopo il riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="466ff-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="466ff-147">Il download in background può richiedere più tempo del download in tempo reale, perché il processo di download si verifica solo quando il processore non sta eseguendo altre attività.</span><span class="sxs-lookup"><span data-stu-id="466ff-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="466ff-148">Il download in background è disponibile solo quando si utilizza Windows XP.</span><span class="sxs-lookup"><span data-stu-id="466ff-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="466ff-149">Informazioni sull'integrazione della libreria</span><span class="sxs-lookup"><span data-stu-id="466ff-149">About Library Integration</span></span>

<span data-ttu-id="466ff-150">Windows Media Player può organizzare automaticamente il contenuto del negozio online nella libreria.</span><span class="sxs-lookup"><span data-stu-id="466ff-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="466ff-151">Per abilitare questa impostazione, è necessario specificare un valore per l'attributo **WM/contentdistributor** per ogni file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="466ff-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="466ff-152">Quando un file multimediale digitale viene aggiunto alla libreria, che si verifica automaticamente quando si usa gestione download, il file viene elencato automaticamente nel nodo **musica acquistato** o **video acquistati** .</span><span class="sxs-lookup"><span data-stu-id="466ff-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="466ff-153">Se, ad esempio, il valore per **WM/contentdistributor** è "Proseware" e il file multimediale digitale contiene musica, il contenuto verrà visualizzato nella libreria nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="466ff-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="466ff-154">Musica/musica acquistata/proseware</span><span class="sxs-lookup"><span data-stu-id="466ff-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="466ff-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="466ff-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="466ff-156">**Gestione download**</span><span class="sxs-lookup"><span data-stu-id="466ff-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="466ff-157">**DownloadCollection. startDownload**</span><span class="sxs-lookup"><span data-stu-id="466ff-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




