---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332756"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="f7db9-103">IAgentCharacter:: GetSize</span><span class="sxs-lookup"><span data-stu-id="f7db9-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="f7db9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f7db9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="f7db9-105">Recupera la dimensione del frame di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="f7db9-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="f7db9-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f7db9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f7db9-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="f7db9-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="f7db9-108">Indirizzo di una variabile che riceve la larghezza del fotogramma di animazione dei caratteri in pixel rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="f7db9-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="f7db9-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="f7db9-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="f7db9-110">Indirizzo di una variabile che riceve l'altezza del frame di animazione dei caratteri in pixel rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="f7db9-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="f7db9-111">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.</span><span class="sxs-lookup"><span data-stu-id="f7db9-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7db9-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f7db9-112">See Also</span></span>

[<span data-ttu-id="f7db9-113">**IAgentCharacter:: sesize**</span><span class="sxs-lookup"><span data-stu-id="f7db9-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 




