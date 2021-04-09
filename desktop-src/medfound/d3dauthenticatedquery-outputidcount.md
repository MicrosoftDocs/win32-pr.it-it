---
description: Restituisce il numero di identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749290"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="e84b8-103">\_OUTPUTIDCOUNT D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="e84b8-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="e84b8-104">Restituisce il numero di identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.</span><span class="sxs-lookup"><span data-stu-id="e84b8-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="e84b8-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84b8-105">Requirement</span></span> | <span data-ttu-id="e84b8-106">Valore</span><span class="sxs-lookup"><span data-stu-id="e84b8-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e84b8-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="e84b8-107">Query GUID</span></span>  | <span data-ttu-id="e84b8-108">**\_OUTPUTIDCOUNT D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="e84b8-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="e84b8-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="e84b8-109">Input data</span></span>  | [<span data-ttu-id="e84b8-110">**\_Input QUERYOUTPUTIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e84b8-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="e84b8-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="e84b8-111">Return data</span></span> | [<span data-ttu-id="e84b8-112">**\_Output QUERYOUTPUTIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e84b8-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="e84b8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e84b8-113">Remarks</span></span>

<span data-ttu-id="e84b8-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="e84b8-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="e84b8-115">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e84b8-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="e84b8-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e84b8-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="e84b8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e84b8-117">Requirements</span></span>



| <span data-ttu-id="e84b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84b8-118">Requirement</span></span> | <span data-ttu-id="e84b8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e84b8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e84b8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e84b8-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e84b8-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e84b8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e84b8-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e84b8-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e84b8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e84b8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84b8-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e84b8-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84b8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e84b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84b8-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="e84b8-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="e84b8-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="e84b8-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e84b8-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="e84b8-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




