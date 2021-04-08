---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856874"
---
# <a name="iagentballoongetvisible"></a><span data-ttu-id="94dde-103">IAgentBalloon:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="94dde-103">IAgentBalloon::GetVisible</span></span>

<span data-ttu-id="94dde-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94dde-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

<span data-ttu-id="94dde-105">Determina se la parola Balloon è visibile o nascosta.</span><span class="sxs-lookup"><span data-stu-id="94dde-105">Determines whether the word balloon is visible or hidden.</span></span>

-   <span data-ttu-id="94dde-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="94dde-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="94dde-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="94dde-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="94dde-108">Indirizzo di una variabile che riceve **true** se la parola Balloon è visibile e **false** se nascosta.</span><span class="sxs-lookup"><span data-stu-id="94dde-108">Address of a variable that receives **True** if the word balloon is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="94dde-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="94dde-109">See Also</span></span>

[<span data-ttu-id="94dde-110">**IAgentBalloon:: sevisible**</span><span class="sxs-lookup"><span data-stu-id="94dde-110">**IAgentBalloon::SetVisible**</span></span>](iagentballoon--setvisible.md)


 

 




