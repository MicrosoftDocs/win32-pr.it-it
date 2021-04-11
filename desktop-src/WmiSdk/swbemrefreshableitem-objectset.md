---
description: La proprietà SWbemRefreshableItem. ObjectSet rappresenta il set di oggetti da aggiornare.
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: Proprietà SWbemRefreshableItem. ObjectSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351386"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="d65a1-103">Proprietà SWbemRefreshableItem. ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d65a1-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="d65a1-104">La proprietà **SWbemRefreshableItem. ObjectSet** rappresenta il set di oggetti da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d65a1-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="d65a1-105">La proprietà **ObjectSet** è un enumeratore o un elemento della raccolta contenuto in un oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="d65a1-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="d65a1-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d65a1-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d65a1-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d65a1-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d65a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d65a1-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="d65a1-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d65a1-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d65a1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d65a1-110">Remarks</span></span>

<span data-ttu-id="d65a1-111">Questa proprietà è **null** a meno che [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) sia **true**.</span><span class="sxs-lookup"><span data-stu-id="d65a1-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d65a1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d65a1-112">Requirements</span></span>



| <span data-ttu-id="d65a1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d65a1-113">Requirement</span></span> | <span data-ttu-id="d65a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a1-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d65a1-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d65a1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d65a1-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d65a1-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d65a1-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d65a1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d65a1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d65a1-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d65a1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d65a1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d65a1-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d65a1-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d65a1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d65a1-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d65a1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d65a1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d65a1-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d65a1-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="d65a1-125">CLSID</span></span><br/>                    | <span data-ttu-id="d65a1-126">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="d65a1-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="d65a1-127">IID</span><span class="sxs-lookup"><span data-stu-id="d65a1-127">IID</span></span><br/>                      | <span data-ttu-id="d65a1-128">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="d65a1-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="d65a1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d65a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d65a1-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="d65a1-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="d65a1-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="d65a1-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




