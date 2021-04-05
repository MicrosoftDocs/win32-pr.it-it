---
title: Pagina IAgentPropertySheet
description: Pagina IAgentPropertySheet
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711353"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="b3bf4-103">IAgentPropertySheet:: sepage</span><span class="sxs-lookup"><span data-stu-id="b3bf4-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="b3bf4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3bf4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="b3bf4-105">Imposta la pagina corrente della finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="b3bf4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b3bf4-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="b3bf4-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="b3bf4-108">BSTR che imposta la pagina corrente della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="b3bf4-109">Il parametro può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="b3bf4-110">**Discorso**</span><span class="sxs-lookup"><span data-stu-id="b3bf4-110">**"Speech"**</span></span>    | <span data-ttu-id="b3bf4-111">Pagina di input vocale.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-111">The Speech Input page.</span></span> |
| <span data-ttu-id="b3bf4-112">**Output**</span><span class="sxs-lookup"><span data-stu-id="b3bf4-112">**"Output"**</span></span>    | <span data-ttu-id="b3bf4-113">Pagina di output.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-113">The Output page.</span></span>       |
| <span data-ttu-id="b3bf4-114">**Copyright**</span><span class="sxs-lookup"><span data-stu-id="b3bf4-114">**"Copyright"**</span></span> | <span data-ttu-id="b3bf4-115">Pagina di copyright.</span><span class="sxs-lookup"><span data-stu-id="b3bf4-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b3bf4-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b3bf4-116">See Also</span></span>

[<span data-ttu-id="b3bf4-117">**IAgentPropertySheet:: GetPage**</span><span class="sxs-lookup"><span data-stu-id="b3bf4-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




