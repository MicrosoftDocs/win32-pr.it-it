---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396798"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="1d0e7-103">IAgentBalloon::GetNumLines</span><span class="sxs-lookup"><span data-stu-id="1d0e7-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="1d0e7-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d0e7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="1d0e7-105">Recupera il valore del numero di righe visualizzate in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="1d0e7-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="1d0e7-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1d0e7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1d0e7-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span><span class="sxs-lookup"><span data-stu-id="1d0e7-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="1d0e7-108">Indirizzo di una variabile che riceve il numero di righe visualizzate.</span><span class="sxs-lookup"><span data-stu-id="1d0e7-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="1d0e7-109">Il server Microsoft Agent scorre automaticamente le righe visualizzate per l'output parlato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="1d0e7-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="1d0e7-110">Il numero di righe per un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1d0e7-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1d0e7-111">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d0e7-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d0e7-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1d0e7-112">See Also</span></span>

[<span data-ttu-id="1d0e7-113">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="1d0e7-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




