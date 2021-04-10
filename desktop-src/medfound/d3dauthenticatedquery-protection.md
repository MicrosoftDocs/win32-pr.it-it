---
description: Restituisce il livello di protezione corrente per il dispositivo.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225812"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="0d7ac-103">\_Protezione D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="0d7ac-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="0d7ac-104">Restituisce il livello di protezione corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d7ac-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="0d7ac-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d7ac-105">Requirement</span></span> | <span data-ttu-id="0d7ac-106">Valore</span><span class="sxs-lookup"><span data-stu-id="0d7ac-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7ac-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="0d7ac-107">Query GUID</span></span>  | <span data-ttu-id="0d7ac-108">**\_Protezione D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="0d7ac-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="0d7ac-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="0d7ac-109">Input data</span></span>  | [<span data-ttu-id="0d7ac-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="0d7ac-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="0d7ac-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="0d7ac-111">Return data</span></span> | [<span data-ttu-id="0d7ac-112">**\_Output QUERYPROTECTION \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="0d7ac-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="0d7ac-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d7ac-113">Remarks</span></span>

<span data-ttu-id="0d7ac-114">Questa query è valida per tutti i tipi di canale.</span><span class="sxs-lookup"><span data-stu-id="0d7ac-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d7ac-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d7ac-115">Requirements</span></span>



| <span data-ttu-id="0d7ac-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d7ac-116">Requirement</span></span> | <span data-ttu-id="0d7ac-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0d7ac-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7ac-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d7ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d7ac-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d7ac-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0d7ac-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d7ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d7ac-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d7ac-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d7ac-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d7ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d7ac-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d7ac-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d7ac-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d7ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7ac-125">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="0d7ac-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="0d7ac-126">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="0d7ac-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="0d7ac-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="0d7ac-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




