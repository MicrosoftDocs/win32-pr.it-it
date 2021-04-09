---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044530"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="99a26-103">IAgentCharacterEx::GetOriginalSize</span><span class="sxs-lookup"><span data-stu-id="99a26-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="99a26-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99a26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="99a26-105">Recupera le dimensioni originali del frame di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="99a26-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="99a26-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="99a26-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="99a26-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="99a26-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="99a26-108">Indirizzo di una variabile che riceve la larghezza originale del frame di animazione dei caratteri in pixel.</span><span class="sxs-lookup"><span data-stu-id="99a26-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="99a26-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="99a26-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="99a26-110">Indirizzo di una variabile che riceve l'altezza originale del frame di animazione dei caratteri in pixel.</span><span class="sxs-lookup"><span data-stu-id="99a26-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="99a26-111">Questa chiamata restituisce le dimensioni originali del frame di caratteri, come compilata nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="99a26-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="99a26-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="99a26-112">See Also</span></span>

[<span data-ttu-id="99a26-113">**IAgentCharacter:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="99a26-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




