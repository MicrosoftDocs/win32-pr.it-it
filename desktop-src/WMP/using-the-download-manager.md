---
title: Uso di Download Manager
description: Uso di Download Manager
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396886"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="c0378-109">Uso di Download Manager</span><span class="sxs-lookup"><span data-stu-id="c0378-109">Using the Download Manager</span></span>

<span data-ttu-id="c0378-110">Windows Media Player SDK include una pagina Web di esempio che illustra l'utilizzo di gestione download per scaricare i file nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0378-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="c0378-111">È possibile individuare l'esempio nella cartella denominata Web in cui è stato installato l'SDK.</span><span class="sxs-lookup"><span data-stu-id="c0378-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="c0378-112">Il nome del file è sample. ASP.</span><span class="sxs-lookup"><span data-stu-id="c0378-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="c0378-113">Nell'esempio sono disponibili le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="c0378-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="c0378-114">Crea l'oggetto **downloadmanager** .</span><span class="sxs-lookup"><span data-stu-id="c0378-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="c0378-115">Crea un oggetto **DownloadCollection** .</span><span class="sxs-lookup"><span data-stu-id="c0378-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="c0378-116">Inizia a scaricare cinque file quando l'utente fa clic su **download**.</span><span class="sxs-lookup"><span data-stu-id="c0378-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="c0378-117">Nell'esempio vengono forniti i percorsi di file predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c0378-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="c0378-118">È necessario sostituire questi percorsi predefiniti con i percorsi dei file nel proprio server.</span><span class="sxs-lookup"><span data-stu-id="c0378-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="c0378-119">È possibile modificare i percorsi modificando i valori assegnati alla matrice globale denominata g \_ sFiles.</span><span class="sxs-lookup"><span data-stu-id="c0378-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="c0378-120">Mostra informazioni sullo stato di un download quando l'utente lo seleziona.</span><span class="sxs-lookup"><span data-stu-id="c0378-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="c0378-121">Fornisce i controlli per sospendere, riprendere, annullare e rimuovere un elemento di download.</span><span class="sxs-lookup"><span data-stu-id="c0378-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="c0378-122">Mantiene le informazioni sulle raccolte di download tra le sessioni usando i cookie.</span><span class="sxs-lookup"><span data-stu-id="c0378-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="c0378-123">Questo è importante perché l'utente può chiudere il lettore in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="c0378-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="c0378-124">Inoltre, se l'utente passa i riquadri attività nel lettore, termina la sessione di archiviazione online.</span><span class="sxs-lookup"><span data-stu-id="c0378-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="c0378-125">Usa il download in tempo reale per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c0378-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="c0378-126">È possibile modificare il comportamento per il download in background modificando il valore della variabile denominata g \_ sDLType.</span><span class="sxs-lookup"><span data-stu-id="c0378-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="c0378-127">Il download in background è disponibile per l'utilizzo con il sistema operativo Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c0378-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="c0378-128">Sincronizza il colore di sfondo con il colore del lettore.</span><span class="sxs-lookup"><span data-stu-id="c0378-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="c0378-129">Questa funzionalità può essere usata per modificare l'aspetto del negozio online quando l'utente sceglie di modificare il colore del lettore.</span><span class="sxs-lookup"><span data-stu-id="c0378-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="c0378-130">Le sezioni seguenti forniscono altre informazioni:</span><span class="sxs-lookup"><span data-stu-id="c0378-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="c0378-131">Inizializzazione della pagina</span><span class="sxs-lookup"><span data-stu-id="c0378-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="c0378-132">Avvio dei download</span><span class="sxs-lookup"><span data-stu-id="c0378-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="c0378-133">Recupero delle informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="c0378-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="c0378-134">Gestione delle informazioni sulla sessione</span><span class="sxs-lookup"><span data-stu-id="c0378-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="c0378-135">Debug della pagina</span><span class="sxs-lookup"><span data-stu-id="c0378-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="c0378-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0378-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0378-137">**Guida per programmatori per i negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="c0378-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




