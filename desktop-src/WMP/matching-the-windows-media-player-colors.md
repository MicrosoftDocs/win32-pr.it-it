---
title: Corrispondenza dei colori di Windows Media Player
description: Corrispondenza dei colori di Windows Media Player
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player Online Stores, corrispondenti colori di Windows Media Player
- negozi online, corrispondenti colori di Windows Media Player
- digitare 1 negozi online, corrispondenti colori di Windows Media Player
- digitare 2 archivi online, corrispondenti colori di Windows Media Player
- Windows Media Player Online Stores, Windows Media Player color matching
- archivi online, corrispondenza colori Windows Media Player
- digitare 1 archivi online, corrispondenza colori Windows Media Player
- digitare 2 archivi online, corrispondenza colori Windows Media Player
- Windows Media Player Online Stores, corrispondenza colori per Windows Media Player
- negozi online, corrispondenza dei colori per Windows Media Player
- digitare 1 negozi online, corrispondenza dei colori per Windows Media Player
- digitare 2 negozi online, corrispondenza dei colori per Windows Media Player
- corrispondenza dei colori per Windows Media Player
- colori corrispondenti di Windows Media Player
- Windows Media Player, colori corrispondenti
- Windows Media Player, corrispondenza colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298715"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="19b8f-119">Corrispondenza dei colori di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="19b8f-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="19b8f-120">La creazione di una pagina Web di archivio online corrisponde alla combinazione di colori di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="19b8f-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="19b8f-121">È sufficiente gestire l'evento **External. OnColorChange** .</span><span class="sxs-lookup"><span data-stu-id="19b8f-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="19b8f-122">Per specificare una funzione per gestire l'evento, usare codice simile al seguente quando viene caricata la pagina Web:</span><span class="sxs-lookup"><span data-stu-id="19b8f-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="19b8f-123">Ogni volta che l'utente modifica la combinazione di colori di Windows Media Player, il lettore chiamerà la funzione.</span><span class="sxs-lookup"><span data-stu-id="19b8f-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="19b8f-124">Nell'esempio seguente viene illustrata una funzione semplice che imposta lo sfondo della pagina Web in modo che corrisponda alla proprietà **External. appColorLight** :</span><span class="sxs-lookup"><span data-stu-id="19b8f-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="19b8f-125">Sono disponibili anche altre proprietà di colore per l'uso.</span><span class="sxs-lookup"><span data-stu-id="19b8f-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="19b8f-126">Vedere [oggetto esterno per gli archivi online di tipo 2](external-object-for-type-2-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="19b8f-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b8f-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19b8f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b8f-128">**External. appColorLight**</span><span class="sxs-lookup"><span data-stu-id="19b8f-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="19b8f-129">**Evento External. OnColorChange**</span><span class="sxs-lookup"><span data-stu-id="19b8f-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="19b8f-130">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="19b8f-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




