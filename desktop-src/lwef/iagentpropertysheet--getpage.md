---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396126"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="7e6dd-103">IAgentPropertySheet:: GetPage</span><span class="sxs-lookup"><span data-stu-id="7e6dd-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="7e6dd-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7e6dd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="7e6dd-105">Recupera la pagina corrente della finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="7e6dd-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7e6dd-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="7e6dd-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="7e6dd-108">Indirizzo di una variabile che riceve la pagina corrente della finestra delle proprietà (ultima pagina visualizzata se la finestra non è aperta).</span><span class="sxs-lookup"><span data-stu-id="7e6dd-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="7e6dd-109">Il parametro può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e6dd-109">The parameter can be one of the following:</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="7e6dd-110">**Discorso**</span><span class="sxs-lookup"><span data-stu-id="7e6dd-110">**"Speech"**</span></span>    | <span data-ttu-id="7e6dd-111">Pagina di input vocale.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-111">The Speech Input page.</span></span> |
| <span data-ttu-id="7e6dd-112">**Output**</span><span class="sxs-lookup"><span data-stu-id="7e6dd-112">**"Output"**</span></span>    | <span data-ttu-id="7e6dd-113">Pagina di output.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-113">The Output page.</span></span>       |
| <span data-ttu-id="7e6dd-114">**Copyright**</span><span class="sxs-lookup"><span data-stu-id="7e6dd-114">**"Copyright"**</span></span> | <span data-ttu-id="7e6dd-115">Pagina di copyright.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7e6dd-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7e6dd-116">See Also</span></span>

[<span data-ttu-id="7e6dd-117">**IAgentPropertySheet:: sepage**</span><span class="sxs-lookup"><span data-stu-id="7e6dd-117">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




