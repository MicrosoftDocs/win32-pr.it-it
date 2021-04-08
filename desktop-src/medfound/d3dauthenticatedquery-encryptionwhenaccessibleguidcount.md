---
description: Restituisce il numero di tipi di crittografia che è possibile usare per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749298"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="7a0d4-103">\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="7a0d4-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="7a0d4-104">Restituisce il numero di tipi di crittografia che è possibile usare per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.</span><span class="sxs-lookup"><span data-stu-id="7a0d4-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="7a0d4-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a0d4-105">Requirement</span></span> | <span data-ttu-id="7a0d4-106">Valore</span><span class="sxs-lookup"><span data-stu-id="7a0d4-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0d4-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="7a0d4-107">Query GUID</span></span>  | <span data-ttu-id="7a0d4-108">**\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="7a0d4-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="7a0d4-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="7a0d4-109">Input data</span></span>  | [<span data-ttu-id="7a0d4-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="7a0d4-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="7a0d4-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="7a0d4-111">Return data</span></span> | [<span data-ttu-id="7a0d4-112">**\_Output QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="7a0d4-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="7a0d4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a0d4-113">Remarks</span></span>

<span data-ttu-id="7a0d4-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="7a0d4-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="7a0d4-115">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="7a0d4-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="7a0d4-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="7a0d4-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0d4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a0d4-117">Requirements</span></span>



| <span data-ttu-id="7a0d4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a0d4-118">Requirement</span></span> | <span data-ttu-id="7a0d4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7a0d4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0d4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a0d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0d4-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7a0d4-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7a0d4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a0d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0d4-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a0d4-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7a0d4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a0d4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a0d4-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0d4-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a0d4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a0d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0d4-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="7a0d4-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="7a0d4-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="7a0d4-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="7a0d4-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="7a0d4-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




