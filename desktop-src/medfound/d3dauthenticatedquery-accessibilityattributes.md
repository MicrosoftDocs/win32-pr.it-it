---
description: Restituisce il tipo di bus di I/O utilizzato per inviare i dati alla GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401540"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="c1886-103">\_ACCESSIBILITYATTRIBUTES D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="c1886-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="c1886-104">Restituisce il tipo di bus di I/O utilizzato per inviare i dati alla GPU.</span><span class="sxs-lookup"><span data-stu-id="c1886-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="c1886-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1886-105">Requirement</span></span> | <span data-ttu-id="c1886-106">Valore</span><span class="sxs-lookup"><span data-stu-id="c1886-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1886-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="c1886-107">Query GUID</span></span>  | <span data-ttu-id="c1886-108">**\_ACCESSIBILITYATTRIBUTES D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="c1886-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="c1886-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="c1886-109">Input data</span></span>  | [<span data-ttu-id="c1886-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1886-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="c1886-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="c1886-111">Return data</span></span> | [<span data-ttu-id="c1886-112">**\_Output QUERYINFOBUSTYPE \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1886-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="c1886-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1886-113">Remarks</span></span>

<span data-ttu-id="c1886-114">Questa query restituisce anche informazioni sul modo in cui il contenuto viene inserito nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="c1886-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="c1886-115">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="c1886-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="c1886-116">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1886-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="c1886-117">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1886-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="c1886-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1886-118">Requirements</span></span>



| <span data-ttu-id="c1886-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1886-119">Requirement</span></span> | <span data-ttu-id="c1886-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c1886-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1886-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1886-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1886-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1886-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1886-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1886-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1886-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1886-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c1886-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1886-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1886-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1886-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1886-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1886-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1886-128">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="c1886-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="c1886-129">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="c1886-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="c1886-130">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="c1886-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




