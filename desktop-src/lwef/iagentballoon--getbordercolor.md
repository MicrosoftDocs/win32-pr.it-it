---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712046"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="05e7b-103">IAgentBalloon::GetBorderColor</span><span class="sxs-lookup"><span data-stu-id="05e7b-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="05e7b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05e7b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="05e7b-105">Recupera il valore per il colore del bordo visualizzato per un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="05e7b-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="05e7b-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="05e7b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="05e7b-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span><span class="sxs-lookup"><span data-stu-id="05e7b-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="05e7b-108">Indirizzo di una variabile che riceve l'impostazione del colore per il bordo del fumetto.</span><span class="sxs-lookup"><span data-stu-id="05e7b-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="05e7b-109">Il colore del bordo per un fumetto di parole in caratteri è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="05e7b-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="05e7b-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05e7b-110">It cannot be changed by an application.</span></span> <span data-ttu-id="05e7b-111">Tuttavia, l'utente può modificare il colore del bordo della parola Balloons per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="05e7b-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="05e7b-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="05e7b-112">See Also</span></span>

<span data-ttu-id="05e7b-113">[**IAgentBalloon:: getBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="05e7b-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 




