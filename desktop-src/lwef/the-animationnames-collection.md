---
title: Raccolta AnimationNames
description: Raccolta AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856169"
---
# <a name="the-animationnames-collection"></a><span data-ttu-id="836bd-103">Raccolta AnimationNames</span><span class="sxs-lookup"><span data-stu-id="836bd-103">The AnimationNames Collection</span></span>

<span data-ttu-id="836bd-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="836bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="836bd-105">La raccolta [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) è una raccolta speciale che contiene l'elenco dei nomi di animazione compilati per un carattere.</span><span class="sxs-lookup"><span data-stu-id="836bd-105">The [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) collection is a special collection that contains the list of animation names compiled for a character.</span></span> <span data-ttu-id="836bd-106">È possibile utilizzare la raccolta per enumerare i nomi delle animazioni per un carattere.</span><span class="sxs-lookup"><span data-stu-id="836bd-106">You can use the collection to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="836bd-107">Ad esempio, in Visual Basic o VBScript (2,0 o versione successiva) è possibile accedere a questi nomi usando il **per ciascuno... Istruzioni successive** :</span><span class="sxs-lookup"><span data-stu-id="836bd-107">For example, in Visual Basic or VBScript (2.0 or later) you can access these names using the **For Each...Next** statements:</span></span>


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



<span data-ttu-id="836bd-108">Gli elementi della raccolta non hanno proprietà, quindi non è possibile accedere direttamente a singoli elementi.</span><span class="sxs-lookup"><span data-stu-id="836bd-108">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span>

<span data-ttu-id="836bd-109">Per. I caratteri ACF, la raccolta restituisce tutte le animazioni definite per il carattere, non solo quelle che sono state recuperate con il metodo [**Get**](get-method.md) .</span><span class="sxs-lookup"><span data-stu-id="836bd-109">For .ACF characters, the collection returns all the animations that have been defined for the character, not just the ones that have been retrieved with the [**Get**](get-method.md) method.</span></span>

 

 




