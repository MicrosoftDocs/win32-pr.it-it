---
title: Avvio dei download
description: Avvio dei download
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, avvio di download
- negozi online, avvio di download
- digitare 2 archivi online, avvio di download
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- avvio del download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396750"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="b860b-113">Avvio dei download</span><span class="sxs-lookup"><span data-stu-id="b860b-113">Starting the Downloads</span></span>

<span data-ttu-id="b860b-114">Il download viene avviato quando l'utente fa clic su **download**.</span><span class="sxs-lookup"><span data-stu-id="b860b-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="b860b-115">Questo pulsante è denominato btnDownload nel codice e la funzione del gestore eventi per l'evento **OnClick** è denominata "ondownload".</span><span class="sxs-lookup"><span data-stu-id="b860b-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="b860b-116">Con "ondownload" viene innanzitutto creato un nuovo oggetto **scaricabile** vuoto che viene assegnato a una variabile locale.</span><span class="sxs-lookup"><span data-stu-id="b860b-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="b860b-117">Successivamente, la funzione avvia ognuno dei cinque elementi scaricati e archivia l'oggetto **DownloadItem** restituito in una matrice.</span><span class="sxs-lookup"><span data-stu-id="b860b-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="b860b-118">Il codice aggiorna quindi gli elementi dell'interfaccia utente con le informazioni sulla raccolta di download e sui relativi elementi di download.</span><span class="sxs-lookup"><span data-stu-id="b860b-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b860b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b860b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b860b-120">**Uso di Download Manager**</span><span class="sxs-lookup"><span data-stu-id="b860b-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




