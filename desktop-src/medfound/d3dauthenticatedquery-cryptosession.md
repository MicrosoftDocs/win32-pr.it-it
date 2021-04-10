---
description: Restituisce handle per la sessione di crittografia e il dispositivo Direct3D associati a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) specificato.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225814"
---
# <a name="d3dauthenticatedquery_cryptosession"></a><span data-ttu-id="d0480-103">\_CRYPTOSESSION D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="d0480-103">D3DAUTHENTICATEDQUERY\_CRYPTOSESSION</span></span>

<span data-ttu-id="d0480-104">Restituisce handle per la sessione di crittografia e il dispositivo Direct3D associati a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) specificato.</span><span class="sxs-lookup"><span data-stu-id="d0480-104">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>



| <span data-ttu-id="d0480-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0480-105">Requirement</span></span> | <span data-ttu-id="d0480-106">Valore</span><span class="sxs-lookup"><span data-stu-id="d0480-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0480-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="d0480-107">Query GUID</span></span>  | <span data-ttu-id="d0480-108">**\_CRYPTOSESSION D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="d0480-108">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>                                                                         |
| <span data-ttu-id="d0480-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="d0480-109">Input data</span></span>  | [<span data-ttu-id="d0480-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="d0480-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                             |
| <span data-ttu-id="d0480-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="d0480-111">Return data</span></span> | [<span data-ttu-id="d0480-112">**\_Output QUERYCRYPTOSESSION \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="d0480-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT**</span></span>](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="d0480-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0480-113">Remarks</span></span>

<span data-ttu-id="d0480-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="d0480-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="d0480-115">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="d0480-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="d0480-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="d0480-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="d0480-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0480-117">Requirements</span></span>



| <span data-ttu-id="d0480-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0480-118">Requirement</span></span> | <span data-ttu-id="d0480-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d0480-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0480-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0480-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0480-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0480-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0480-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0480-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0480-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0480-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0480-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0480-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0480-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0480-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0480-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0480-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0480-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="d0480-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="d0480-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="d0480-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="d0480-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="d0480-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




