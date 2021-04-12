---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330348"
---
# <a name="iagentpropertysheetgetvisible"></a><span data-ttu-id="3921d-103">IAgentPropertySheet:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="3921d-103">IAgentPropertySheet::GetVisible</span></span>

<span data-ttu-id="3921d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3921d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

<span data-ttu-id="3921d-105">Determina se la finestra delle proprietà di Microsoft Agent è visibile o nascosta.</span><span class="sxs-lookup"><span data-stu-id="3921d-105">Determines whether the Microsoft Agent property sheet is visible or hidden.</span></span>

-   <span data-ttu-id="3921d-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3921d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3921d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="3921d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="3921d-108">Indirizzo di una variabile che riceve **true** se la finestra delle proprietà è visibile e **false** se nascosta.</span><span class="sxs-lookup"><span data-stu-id="3921d-108">Address of a variable that receives **True** if the property sheet is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="3921d-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3921d-109">See Also</span></span>

[<span data-ttu-id="3921d-110">**IAgentPropertySheet:: sevisible**</span><span class="sxs-lookup"><span data-stu-id="3921d-110">**IAgentPropertySheet::SetVisible**</span></span>](iagentpropertysheet--setvisible.md)


 

 




