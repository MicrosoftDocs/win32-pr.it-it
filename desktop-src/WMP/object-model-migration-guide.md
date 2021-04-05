---
title: Guida alla migrazione del modello a oggetti
description: Guida alla migrazione del modello a oggetti
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Windows Media Player, modello a oggetti
- Windows Media Player, Guida alla migrazione
- Modello a oggetti di Windows Media Player, Guida alla migrazione
- modello a oggetti, Guida alla migrazione
- Controllo ActiveX di Windows Media Player, Guida alla migrazione
- Controllo ActiveX, Guida alla migrazione
- Controllo ActiveX Windows Media Player Mobile, Guida alla migrazione
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione di Windows Media Player Mobile
- Guida alla migrazione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045142"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="af736-113">Guida alla migrazione del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="af736-113">Object Model Migration Guide</span></span>

<span data-ttu-id="af736-114">In Windows Media Player 7 è stato introdotto un nuovo modello a oggetti che offre un nuovo set completo di funzionalità che è possibile utilizzare per migliorare le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="af736-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="af736-115">Le versioni successive hanno esteso il modello a oggetti della versione 7 con proprietà, metodi ed eventi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="af736-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="af736-116">Tuttavia, il nuovo modello a oggetti è sostanzialmente diverso dal modello a oggetti di Windows Media Player 6,4, pertanto è necessario comprendere come aggiornare il codice esistente se si desidera supportare Windows Media Player 7 e versioni successive nei progetti.</span><span class="sxs-lookup"><span data-stu-id="af736-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="af736-117">Per un esempio in cui viene illustrato come rilevare la versione di Windows Media Player e il browser corrente dell'utente, vedere l'esempio denominato "rilevamento" installato con questo SDK.</span><span class="sxs-lookup"><span data-stu-id="af736-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="af736-118">Per ulteriori informazioni sugli esempi, vedere [esempi](samples.md).</span><span class="sxs-lookup"><span data-stu-id="af736-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="af736-119">Questa guida si riferisce al nuovo modello a oggetti come modello a oggetti di Windows Media Player 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="af736-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="af736-120">Per informazioni dettagliate sulle funzionalità disponibili in ogni versione di Windows Media Player, vedere [riferimento del modello a oggetti per lo scripting](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="af736-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="af736-121">Questi problemi del modello a oggetti sono trattati negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="af736-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="af736-122">Differenze tra i modelli a oggetti</span><span class="sxs-lookup"><span data-stu-id="af736-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="af736-123">Uso del modello a oggetti di Windows Media Player 7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="af736-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="af736-124">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="af736-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="af736-125">Playlist</span><span class="sxs-lookup"><span data-stu-id="af736-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="af736-126">Didascalie chiuse</span><span class="sxs-lookup"><span data-stu-id="af736-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="af736-127">DVD</span><span class="sxs-lookup"><span data-stu-id="af736-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="af736-128">Confronto dettagliato del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="af736-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="af736-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af736-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af736-130">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="af736-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




