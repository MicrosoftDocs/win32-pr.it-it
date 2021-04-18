---
description: La proprietà SWbemRefreshableItem. IsSet è un valore booleano che indica se l'oggetto SWbemRefreshableItem rappresenta un singolo oggetto o un set di oggetti. L'oggetto SWbemRefreshableItem rappresenta un singolo oggetto o un set di oggetti.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Proprietà SWbemRefreshableItem. IsSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320558"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="0cab3-103">Proprietà SWbemRefreshableItem. IsSet</span><span class="sxs-lookup"><span data-stu-id="0cab3-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="0cab3-104">La proprietà **SWbemRefreshableItem. IsSet** è un valore booleano che indica se l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) rappresenta un singolo oggetto o un set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="0cab3-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="0cab3-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0cab3-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0cab3-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0cab3-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cab3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cab3-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0cab3-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0cab3-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0cab3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cab3-109">Remarks</span></span>

<span data-ttu-id="0cab3-110">Se **SWbemRefreshableItem. IsSet** è **true**, l'elemento rappresenta un oggetto [**SWbemObjectSet**](swbemobjectset.md) e la proprietà dell' [**oggetto**](swbemrefreshableitem-object.md) sarà **null**.</span><span class="sxs-lookup"><span data-stu-id="0cab3-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="0cab3-111">Se **false**, l'elemento rappresenta un oggetto [**SWbemObject**](swbemobject.md) e la proprietà dell' **oggetto** è **null**.</span><span class="sxs-lookup"><span data-stu-id="0cab3-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cab3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cab3-112">Requirements</span></span>



| <span data-ttu-id="0cab3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cab3-113">Requirement</span></span> | <span data-ttu-id="0cab3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0cab3-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cab3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cab3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0cab3-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cab3-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cab3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cab3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0cab3-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cab3-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cab3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cab3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cab3-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cab3-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cab3-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0cab3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="0cab3-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0cab3-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0cab3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0cab3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cab3-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cab3-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0cab3-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="0cab3-125">CLSID</span></span><br/>                    | <span data-ttu-id="0cab3-126">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="0cab3-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="0cab3-127">IID</span><span class="sxs-lookup"><span data-stu-id="0cab3-127">IID</span></span><br/>                      | <span data-ttu-id="0cab3-128">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="0cab3-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="0cab3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cab3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cab3-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="0cab3-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="0cab3-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="0cab3-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




