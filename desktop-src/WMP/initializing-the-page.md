---
title: Inizializzazione della pagina
description: Inizializzazione della pagina
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, inizializzazione di pagine
- archivi online, inizializzazione di pagine
- digitare 2 archivi online, inizializzazione di pagine
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- inizializzazione di pagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221732"
---
# <a name="initializing-the-page"></a><span data-ttu-id="5f735-113">Inizializzazione della pagina</span><span class="sxs-lookup"><span data-stu-id="5f735-113">Initializing the Page</span></span>

<span data-ttu-id="5f735-114">Quando viene caricata la pagina Web, viene eseguita la funzione **init** .</span><span class="sxs-lookup"><span data-stu-id="5f735-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="5f735-115">Questo codice recupera prima tutti i dati archiviati in una sessione precedente.</span><span class="sxs-lookup"><span data-stu-id="5f735-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="5f735-116">Per informazioni dettagliate, vedere [gestione delle informazioni sulla sessione](maintaining-session-information.md).</span><span class="sxs-lookup"><span data-stu-id="5f735-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="5f735-117">Quindi crea l'oggetto **downloadmanager** e lo archivia nella variabile globale denominata g \_ oManager.</span><span class="sxs-lookup"><span data-stu-id="5f735-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="5f735-118">Successivamente, la funzione connette l'evento **OnColorChange** alla funzione denominata **OnAppColor** e quindi chiama direttamente la funzione per inizializzare il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="5f735-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="5f735-119">Vedere [corrispondenza dei colori di Windows Media Player](matching-the-windows-media-player-colors.md).</span><span class="sxs-lookup"><span data-stu-id="5f735-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="5f735-120">Infine, la funzione avvia un timer con un intervallo di un secondo e inizializza le caselle di riepilogo che visualizzano le raccolte di download in sospeso e gli elementi di download.</span><span class="sxs-lookup"><span data-stu-id="5f735-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="5f735-121">Questo è importante perché è possibile che siano state apportate sessioni in corso l'ultima volta che l'archivio online è stato chiuso e che queste informazioni devono essere visualizzate nuovamente.</span><span class="sxs-lookup"><span data-stu-id="5f735-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f735-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f735-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f735-123">**Uso di Download Manager**</span><span class="sxs-lookup"><span data-stu-id="5f735-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




