---
description: Restituisce il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305417"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="9814f-103">\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="9814f-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="9814f-104">Restituisce il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="9814f-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="9814f-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="9814f-105">Requirement</span></span> | <span data-ttu-id="9814f-106">Valore</span><span class="sxs-lookup"><span data-stu-id="9814f-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9814f-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="9814f-107">Query GUID</span></span>  | <span data-ttu-id="9814f-108">**\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="9814f-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="9814f-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="9814f-109">Input data</span></span>  | [<span data-ttu-id="9814f-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9814f-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="9814f-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="9814f-111">Return data</span></span> | [<span data-ttu-id="9814f-112">**\_Output QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9814f-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="9814f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9814f-113">Remarks</span></span>

<span data-ttu-id="9814f-114">L'unico tipo di canale che supporta questa query è il **\_ \_ software del driver D3DAUTHENTICATEDCHANNEL**.</span><span class="sxs-lookup"><span data-stu-id="9814f-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9814f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9814f-115">Requirements</span></span>



| <span data-ttu-id="9814f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9814f-116">Requirement</span></span> | <span data-ttu-id="9814f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9814f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9814f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9814f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9814f-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9814f-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9814f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9814f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9814f-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9814f-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9814f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9814f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9814f-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9814f-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9814f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9814f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9814f-125">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="9814f-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="9814f-126">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="9814f-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="9814f-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="9814f-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




