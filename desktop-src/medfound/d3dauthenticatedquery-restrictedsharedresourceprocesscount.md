---
description: Restituisce il numero di processi a cui è consentito aprire risorse condivise con accesso limitato.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305418"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a><span data-ttu-id="beb3a-103">\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="beb3a-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span></span>

<span data-ttu-id="beb3a-104">Restituisce il numero di processi a cui è consentito aprire risorse condivise con accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="beb3a-104">Returns the number of processes that are allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="beb3a-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb3a-105">Requirement</span></span> | <span data-ttu-id="beb3a-106">Valore</span><span class="sxs-lookup"><span data-stu-id="beb3a-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb3a-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="beb3a-107">Query GUID</span></span>  | <span data-ttu-id="beb3a-108">**\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="beb3a-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span></span>                                                                                                |
| <span data-ttu-id="beb3a-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="beb3a-109">Input data</span></span>  | [<span data-ttu-id="beb3a-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="beb3a-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                           |
| <span data-ttu-id="beb3a-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="beb3a-111">Return data</span></span> | [<span data-ttu-id="beb3a-112">**\_Output QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="beb3a-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="beb3a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="beb3a-113">Remarks</span></span>

<span data-ttu-id="beb3a-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="beb3a-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="beb3a-115">**\_D3d9 D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="beb3a-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="beb3a-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="beb3a-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="beb3a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="beb3a-117">Requirements</span></span>



| <span data-ttu-id="beb3a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb3a-118">Requirement</span></span> | <span data-ttu-id="beb3a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="beb3a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb3a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="beb3a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="beb3a-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="beb3a-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="beb3a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="beb3a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="beb3a-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="beb3a-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="beb3a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="beb3a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="beb3a-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb3a-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb3a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="beb3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb3a-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="beb3a-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="beb3a-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="beb3a-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="beb3a-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="beb3a-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




