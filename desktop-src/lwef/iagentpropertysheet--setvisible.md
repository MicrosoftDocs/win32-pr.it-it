---
title: IAgentPropertySheet visibile
description: IAgentPropertySheet visibile
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298325"
---
# <a name="iagentpropertysheetsetvisible"></a><span data-ttu-id="fc4a2-103">IAgentPropertySheet:: sevisible</span><span class="sxs-lookup"><span data-stu-id="fc4a2-103">IAgentPropertySheet::SetVisible</span></span>

<span data-ttu-id="fc4a2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc4a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

<span data-ttu-id="fc4a2-105">Imposta la proprietà [**Visible**](visible-property.md) per la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fc4a2-105">Sets the [**Visible**](visible-property.md) property for the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="fc4a2-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fc4a2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fc4a2-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="fc4a2-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="fc4a2-108">Impostazione della proprietà Visible.</span><span class="sxs-lookup"><span data-stu-id="fc4a2-108">Visible property setting.</span></span> <span data-ttu-id="fc4a2-109">Il valore **true** Visualizza la finestra delle proprietà. il valore **false** lo nasconde.</span><span class="sxs-lookup"><span data-stu-id="fc4a2-109">A value of **True** displays the property sheet; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fc4a2-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fc4a2-110">See Also</span></span>

[<span data-ttu-id="fc4a2-111">**IAgentPropertySheet:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="fc4a2-111">**IAgentPropertySheet::GetVisible**</span></span>](iagentpropertysheet--getvisible.md)


 

 




