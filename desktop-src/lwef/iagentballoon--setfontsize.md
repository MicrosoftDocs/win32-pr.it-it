---
title: IAgentBalloon sefontsize
description: IAgentBalloon sefontsize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332247"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="787b4-103">IAgentBalloon:: sefontsize</span><span class="sxs-lookup"><span data-stu-id="787b4-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="787b4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="787b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="787b4-105">Imposta la dimensione del tipo di carattere visualizzato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="787b4-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="787b4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="787b4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="787b4-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="787b4-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="787b4-108">Dimensione del carattere.</span><span class="sxs-lookup"><span data-stu-id="787b4-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="787b4-109">Le dimensioni predefinite del carattere utilizzate nella parola Balloon di un carattere sono definite nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="787b4-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="787b4-110">È possibile modificarlo con **IAgentBalloon:: sefontsize**.</span><span class="sxs-lookup"><span data-stu-id="787b4-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="787b4-111">Tuttavia, l'utente può eseguire l'override dell'impostazione della dimensione del carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="787b4-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="787b4-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="787b4-112">See Also</span></span>

[<span data-ttu-id="787b4-113">**IAgentBalloon:: GetFontSize**</span><span class="sxs-lookup"><span data-stu-id="787b4-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




