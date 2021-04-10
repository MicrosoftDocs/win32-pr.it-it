---
description: Restituisce il tipo di crittografia applicato prima che il contenuto diventi accessibile alla CPU o al bus.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225815"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="85961-103">\_CURRENTENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="85961-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="85961-104">Restituisce il tipo di crittografia applicato prima che il contenuto diventi accessibile alla CPU o al bus.</span><span class="sxs-lookup"><span data-stu-id="85961-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="85961-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="85961-105">Requirement</span></span> | <span data-ttu-id="85961-106">Valore</span><span class="sxs-lookup"><span data-stu-id="85961-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85961-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="85961-107">Query GUID</span></span>  | <span data-ttu-id="85961-108">**\_CURRENTENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="85961-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="85961-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="85961-109">Input data</span></span>  | [<span data-ttu-id="85961-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="85961-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="85961-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="85961-111">Return data</span></span> | [<span data-ttu-id="85961-112">**\_Output QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="85961-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="85961-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="85961-113">Remarks</span></span>

<span data-ttu-id="85961-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="85961-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="85961-115">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="85961-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="85961-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="85961-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="85961-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85961-117">Requirements</span></span>



| <span data-ttu-id="85961-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="85961-118">Requirement</span></span> | <span data-ttu-id="85961-119">Valore</span><span class="sxs-lookup"><span data-stu-id="85961-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85961-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85961-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85961-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="85961-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="85961-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85961-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85961-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="85961-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="85961-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85961-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="85961-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="85961-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85961-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85961-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85961-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="85961-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="85961-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="85961-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="85961-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="85961-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




