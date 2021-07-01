---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120746"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="c3a85-103">IAgentPropertySheet::SetPage</span><span class="sxs-lookup"><span data-stu-id="c3a85-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="c3a85-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3a85-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="c3a85-105">Imposta la pagina corrente della finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c3a85-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="c3a85-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="c3a85-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c3a85-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="c3a85-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="c3a85-108">Oggetto BSTR che imposta la pagina corrente della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c3a85-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="c3a85-109">Il parametro può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3a85-109">The parameter can be one of the following.</span></span>



|                 | <span data-ttu-id="c3a85-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3a85-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="c3a85-111">**"Voce"**</span><span class="sxs-lookup"><span data-stu-id="c3a85-111">**"Speech"**</span></span>    | <span data-ttu-id="c3a85-112">Pagina Input vocale.</span><span class="sxs-lookup"><span data-stu-id="c3a85-112">The Speech Input page.</span></span> |
| <span data-ttu-id="c3a85-113">**"Output"**</span><span class="sxs-lookup"><span data-stu-id="c3a85-113">**"Output"**</span></span>    | <span data-ttu-id="c3a85-114">Pagina Output.</span><span class="sxs-lookup"><span data-stu-id="c3a85-114">The Output page.</span></span>       |
| <span data-ttu-id="c3a85-115">**"Copyright"**</span><span class="sxs-lookup"><span data-stu-id="c3a85-115">**"Copyright"**</span></span> | <span data-ttu-id="c3a85-116">Pagina Copyright.</span><span class="sxs-lookup"><span data-stu-id="c3a85-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c3a85-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c3a85-117">See Also</span></span>

[<span data-ttu-id="c3a85-118">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="c3a85-118">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




