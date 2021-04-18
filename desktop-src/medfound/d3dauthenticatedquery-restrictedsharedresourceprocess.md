---
description: Restituisce informazioni su un processo autorizzato ad aprire risorse condivise con accesso limitato.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305419"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="183a2-103">\_RESTRICTEDSHAREDRESOURCEPROCESS D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="183a2-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="183a2-104">Restituisce informazioni su un processo autorizzato ad aprire risorse condivise con accesso limitato.</span><span class="sxs-lookup"><span data-stu-id="183a2-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="183a2-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="183a2-105">Requirement</span></span> | <span data-ttu-id="183a2-106">Valore</span><span class="sxs-lookup"><span data-stu-id="183a2-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="183a2-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="183a2-107">Query GUID</span></span>  | <span data-ttu-id="183a2-108">**\_RESTRICTEDSHAREDRESOURCEPROCESS D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="183a2-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="183a2-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="183a2-109">Input data</span></span>  | [<span data-ttu-id="183a2-110">**\_Input QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="183a2-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="183a2-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="183a2-111">Return data</span></span> | [<span data-ttu-id="183a2-112">**\_Output QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="183a2-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="183a2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="183a2-113">Remarks</span></span>

<span data-ttu-id="183a2-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="183a2-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="183a2-115">**\_D3d9 D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="183a2-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="183a2-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="183a2-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="183a2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="183a2-117">Requirements</span></span>



| <span data-ttu-id="183a2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="183a2-118">Requirement</span></span> | <span data-ttu-id="183a2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="183a2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="183a2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="183a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="183a2-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="183a2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="183a2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="183a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="183a2-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="183a2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="183a2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="183a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="183a2-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="183a2-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="183a2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="183a2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="183a2-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="183a2-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="183a2-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="183a2-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="183a2-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="183a2-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




