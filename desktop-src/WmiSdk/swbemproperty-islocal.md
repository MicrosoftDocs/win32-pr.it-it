---
description: La proprietà setlocale dell'oggetto SWbemProperty è un valore booleano che può essere utilizzato per determinare se questa proprietà è locale. Il valore FALSE indica che questa proprietà è stata ereditata da un'altra classe. Questa proprietà è di sola lettura.
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: Proprietà SWbemProperty. setlocale (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882301"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="a0312-105">Proprietà SWbemProperty. setlocale</span><span class="sxs-lookup"><span data-stu-id="a0312-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="a0312-106">La proprietà **setlocale** dell'oggetto [**SWbemProperty**](swbemproperty.md) è un valore booleano che può essere utilizzato per determinare se questa proprietà è locale.</span><span class="sxs-lookup"><span data-stu-id="a0312-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="a0312-107">Il valore **false** indica che questa proprietà è stata ereditata da un'altra classe.</span><span class="sxs-lookup"><span data-stu-id="a0312-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="a0312-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a0312-108">This property is read-only.</span></span>

<span data-ttu-id="a0312-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a0312-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a0312-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a0312-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0312-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0312-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a0312-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a0312-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a0312-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0312-113">Requirements</span></span>



| <span data-ttu-id="a0312-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0312-114">Requirement</span></span> | <span data-ttu-id="a0312-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a0312-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0312-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0312-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0312-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0312-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0312-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0312-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0312-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0312-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0312-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0312-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0312-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0312-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0312-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a0312-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0312-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0312-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0312-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a0312-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0312-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0312-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0312-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="a0312-126">CLSID</span></span><br/>                    | <span data-ttu-id="a0312-127">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="a0312-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="a0312-128">IID</span><span class="sxs-lookup"><span data-stu-id="a0312-128">IID</span></span><br/>                      | <span data-ttu-id="a0312-129">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="a0312-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




