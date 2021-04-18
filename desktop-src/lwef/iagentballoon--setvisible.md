---
title: IAgentBalloon visibile
description: IAgentBalloon visibile
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838c34397bc089ea49579b5f6a8c7d5834c8a580
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298265"
---
# <a name="iagentballoonsetvisible"></a><span data-ttu-id="57a38-103">IAgentBalloon:: sevisible</span><span class="sxs-lookup"><span data-stu-id="57a38-103">IAgentBalloon::SetVisible</span></span>

<span data-ttu-id="57a38-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57a38-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

<span data-ttu-id="57a38-105">Imposta la proprietà [**Visible**](visible-property.md) per la parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="57a38-105">Sets the [**Visible**](visible-property.md) property for the word balloon.</span></span>

-   <span data-ttu-id="57a38-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="57a38-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="57a38-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="57a38-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="57a38-108">Impostazione della proprietà Visible.</span><span class="sxs-lookup"><span data-stu-id="57a38-108">Visible property setting.</span></span> <span data-ttu-id="57a38-109">Il valore **true** Visualizza la parola Balloon; il valore **false** lo nasconde.</span><span class="sxs-lookup"><span data-stu-id="57a38-109">A value of **True** displays the word balloon; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="57a38-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="57a38-110">See Also</span></span>

[<span data-ttu-id="57a38-111">**IAgentBalloon:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="57a38-111">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




