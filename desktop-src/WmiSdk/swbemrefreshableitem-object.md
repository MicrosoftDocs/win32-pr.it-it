---
description: La proprietà SWbemRefreshableItem. Object rappresenta una singola istanza di SWbemObject che viene aggiornata. L'elemento è contenuto in un oggetto SWbemRefresher. Istanza di SWbemObject che viene aggiornata. L'elemento è contenuto in un oggetto SWbemRefresher.
ms.assetid: 91a693c0-cde4-4cf6-b85a-662cfd0333e9
ms.tgt_platform: multiple
title: Proprietà SWbemRefreshableItem. Object (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Object
- ISWbemRefreshableItem.Object
- ISWbemRefreshableItem.get_Object
- ISWbemRefreshableItem.put_Object
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b8456422088e9914562b87b2b114629bd80003c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968896"
---
# <a name="swbemrefreshableitemobject-property"></a><span data-ttu-id="56ab2-105">Proprietà SWbemRefreshableItem. Object</span><span class="sxs-lookup"><span data-stu-id="56ab2-105">SWbemRefreshableItem.Object property</span></span>

<span data-ttu-id="56ab2-106">La proprietà **SWbemRefreshableItem. Object** rappresenta una singola istanza di [**SWbemObject**](swbemobject.md) che viene aggiornata.</span><span class="sxs-lookup"><span data-stu-id="56ab2-106">The **SWbemRefreshableItem.Object** property represents a single [**SWbemObject**](swbemobject.md) instance that is refreshed.</span></span> <span data-ttu-id="56ab2-107">L'elemento è contenuto in un oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="56ab2-107">The item is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="56ab2-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="56ab2-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="56ab2-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="56ab2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ab2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56ab2-110">Syntax</span></span>


```VB
SWbemRefreshableItem.Object As Object
```



## <a name="property-value"></a><span data-ttu-id="56ab2-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="56ab2-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="56ab2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="56ab2-112">Remarks</span></span>

<span data-ttu-id="56ab2-113">Questa proprietà è **null** a meno che [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) sia **false**.</span><span class="sxs-lookup"><span data-stu-id="56ab2-113">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ab2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56ab2-114">Requirements</span></span>



| <span data-ttu-id="56ab2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ab2-115">Requirement</span></span> | <span data-ttu-id="56ab2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="56ab2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56ab2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56ab2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56ab2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56ab2-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56ab2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56ab2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56ab2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56ab2-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56ab2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56ab2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ab2-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ab2-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56ab2-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="56ab2-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="56ab2-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56ab2-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56ab2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="56ab2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ab2-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ab2-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="56ab2-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="56ab2-127">CLSID</span></span><br/>                    | <span data-ttu-id="56ab2-128">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="56ab2-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="56ab2-129">IID</span><span class="sxs-lookup"><span data-stu-id="56ab2-129">IID</span></span><br/>                      | <span data-ttu-id="56ab2-130">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="56ab2-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="56ab2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56ab2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ab2-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="56ab2-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="56ab2-133">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="56ab2-133">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




