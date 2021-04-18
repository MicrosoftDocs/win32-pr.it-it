---
description: Restituisce uno dei tipi di crittografia che è possibile usare per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305424"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="db28d-103">\_ENCRYPTIONWHENACCESSIBLEGUID D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="db28d-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="db28d-104">Restituisce uno dei tipi di crittografia che è possibile usare per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.</span><span class="sxs-lookup"><span data-stu-id="db28d-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="db28d-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="db28d-105">Requirement</span></span> | <span data-ttu-id="db28d-106">Valore</span><span class="sxs-lookup"><span data-stu-id="db28d-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db28d-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="db28d-107">Query GUID</span></span>  | <span data-ttu-id="db28d-108">**\_ENCRYPTIONWHENACCESSIBLEGUID D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="db28d-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="db28d-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="db28d-109">Input data</span></span>  | [<span data-ttu-id="db28d-110">**\_Input QUERYEVICTIONENCRYPTIONGUID \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="db28d-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="db28d-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="db28d-111">Return data</span></span> | [<span data-ttu-id="db28d-112">**\_Output QUERYEVICTIONENCRYPTIONGUID \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="db28d-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="db28d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="db28d-113">Remarks</span></span>

<span data-ttu-id="db28d-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="db28d-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="db28d-115">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="db28d-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="db28d-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="db28d-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="db28d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db28d-117">Requirements</span></span>



| <span data-ttu-id="db28d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db28d-118">Requirement</span></span> | <span data-ttu-id="db28d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="db28d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db28d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db28d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db28d-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="db28d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db28d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db28d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db28d-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="db28d-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="db28d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db28d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db28d-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="db28d-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db28d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db28d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db28d-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="db28d-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="db28d-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="db28d-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="db28d-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="db28d-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




