---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298870"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="61713-103">IAgentBalloon:: GetForeColor</span><span class="sxs-lookup"><span data-stu-id="61713-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="61713-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61713-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="61713-105">Recupera il valore per il colore di primo piano visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="61713-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="61713-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="61713-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="61713-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span><span class="sxs-lookup"><span data-stu-id="61713-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="61713-108">Indirizzo di una variabile che riceve l'impostazione del colore per il primo piano del fumetto.</span><span class="sxs-lookup"><span data-stu-id="61713-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="61713-109">Il colore di primo piano utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="61713-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="61713-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61713-110">It cannot be changed by an application.</span></span> <span data-ttu-id="61713-111">Tuttavia, l'utente può eseguire l'override del colore di primo piano delle parole palloncine per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="61713-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="61713-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="61713-112">See Also</span></span>

[<span data-ttu-id="61713-113">**IAgentBalloon:: GetBackColor**</span><span class="sxs-lookup"><span data-stu-id="61713-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 




