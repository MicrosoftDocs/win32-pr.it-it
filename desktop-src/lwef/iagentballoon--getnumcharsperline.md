---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045300"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="1199e-103">IAgentBalloon::GetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="1199e-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="1199e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1199e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="1199e-105">Recupera il valore per il numero medio di caratteri per riga visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="1199e-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="1199e-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1199e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1199e-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="1199e-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="1199e-108">Indirizzo di una variabile che riceve il numero di caratteri per riga.</span><span class="sxs-lookup"><span data-stu-id="1199e-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="1199e-109">Il server Microsoft Agent scorre automaticamente le righe visualizzate per l'output parlato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="1199e-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="1199e-110">Il numero medio di caratteri per riga per la parola Balloon di un carattere è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1199e-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1199e-111">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1199e-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1199e-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1199e-112">See Also</span></span>

[<span data-ttu-id="1199e-113">**IAgentBalloon::GetNumLines**</span><span class="sxs-lookup"><span data-stu-id="1199e-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




