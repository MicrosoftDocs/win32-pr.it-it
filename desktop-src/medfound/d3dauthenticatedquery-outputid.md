---
description: Restituisce uno degli identificatori di output associato a una sessione di crittografia e a un dispositivo Direct3D specificati.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749295"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="c1fda-103">\_OUTPUTID D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="c1fda-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="c1fda-104">Restituisce uno degli identificatori di output associato a una sessione di crittografia e a un dispositivo Direct3D specificati.</span><span class="sxs-lookup"><span data-stu-id="c1fda-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="c1fda-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fda-105">Requirement</span></span> | <span data-ttu-id="c1fda-106">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fda-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fda-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="c1fda-107">Query GUID</span></span>  | <span data-ttu-id="c1fda-108">**\_OUTPUTID D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="c1fda-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="c1fda-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="c1fda-109">Input data</span></span>  | [<span data-ttu-id="c1fda-110">**\_Input QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1fda-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="c1fda-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="c1fda-111">Return data</span></span> | [<span data-ttu-id="c1fda-112">**\_Output QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1fda-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="c1fda-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1fda-113">Remarks</span></span>

<span data-ttu-id="c1fda-114">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="c1fda-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="c1fda-115">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1fda-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="c1fda-116">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="c1fda-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fda-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1fda-117">Requirements</span></span>



| <span data-ttu-id="c1fda-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fda-118">Requirement</span></span> | <span data-ttu-id="c1fda-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fda-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fda-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1fda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fda-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1fda-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1fda-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1fda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fda-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1fda-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c1fda-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1fda-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1fda-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1fda-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1fda-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1fda-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fda-127">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="c1fda-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="c1fda-128">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="c1fda-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="c1fda-129">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="c1fda-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




