---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119866"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="07a4f-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="07a4f-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="07a4f-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07a4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="07a4f-105">Recupera la pagina corrente della finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="07a4f-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="07a4f-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="07a4f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="07a4f-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="07a4f-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="07a4f-108">Indirizzo di una variabile che riceve la pagina corrente della finestra delle proprietà (ultima pagina visualizzata se la finestra non è aperta).</span><span class="sxs-lookup"><span data-stu-id="07a4f-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="07a4f-109">Il parametro può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="07a4f-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="07a4f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a4f-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="07a4f-111">**"Voce"**</span><span class="sxs-lookup"><span data-stu-id="07a4f-111">**"Speech"**</span></span>    | <span data-ttu-id="07a4f-112">Pagina Input vocale.</span><span class="sxs-lookup"><span data-stu-id="07a4f-112">The Speech Input page.</span></span> |
| <span data-ttu-id="07a4f-113">**"Output"**</span><span class="sxs-lookup"><span data-stu-id="07a4f-113">**"Output"**</span></span>    | <span data-ttu-id="07a4f-114">Pagina Output.</span><span class="sxs-lookup"><span data-stu-id="07a4f-114">The Output page.</span></span>       |
| <span data-ttu-id="07a4f-115">**"Copyright"**</span><span class="sxs-lookup"><span data-stu-id="07a4f-115">**"Copyright"**</span></span> | <span data-ttu-id="07a4f-116">Pagina Copyright.</span><span class="sxs-lookup"><span data-stu-id="07a4f-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="07a4f-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="07a4f-117">See Also</span></span>

[<span data-ttu-id="07a4f-118">**IAgentPropertySheet::SetPage**</span><span class="sxs-lookup"><span data-stu-id="07a4f-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




