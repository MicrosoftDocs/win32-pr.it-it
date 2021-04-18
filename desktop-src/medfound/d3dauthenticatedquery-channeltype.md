---
description: Restituisce il tipo di canale autenticato.
ms.assetid: eec4b117-a9f2-479d-99d7-e5d4053cf6b4
title: D3DAUTHENTICATEDQUERY_CHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 58ac84a0caca5a5709c74adbca567633e12daa10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305426"
---
# <a name="d3dauthenticatedquery_channeltype"></a><span data-ttu-id="de7b3-103">\_CHANNELTYPE D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="de7b3-103">D3DAUTHENTICATEDQUERY\_CHANNELTYPE</span></span>

<span data-ttu-id="de7b3-104">Restituisce il tipo di canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="de7b3-104">Returns the type of authenticated channel.</span></span>



| <span data-ttu-id="de7b3-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="de7b3-105">Requirement</span></span> | <span data-ttu-id="de7b3-106">Valore</span><span class="sxs-lookup"><span data-stu-id="de7b3-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de7b3-107">GUID query</span><span class="sxs-lookup"><span data-stu-id="de7b3-107">Query GUID</span></span>  | <span data-ttu-id="de7b3-108">**\_CHANNELTYPE D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="de7b3-108">**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**</span></span>                                                                       |
| <span data-ttu-id="de7b3-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="de7b3-109">Input data</span></span>  | [<span data-ttu-id="de7b3-110">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="de7b3-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="de7b3-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="de7b3-111">Return data</span></span> | [<span data-ttu-id="de7b3-112">**\_Output QUERYCHANNELTYPE \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="de7b3-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querychanneltype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="de7b3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="de7b3-113">Remarks</span></span>

<span data-ttu-id="de7b3-114">Questa query è valida per tutti i tipi di canale.</span><span class="sxs-lookup"><span data-stu-id="de7b3-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="de7b3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de7b3-115">Requirements</span></span>



| <span data-ttu-id="de7b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="de7b3-116">Requirement</span></span> | <span data-ttu-id="de7b3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="de7b3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de7b3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de7b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de7b3-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="de7b3-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de7b3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de7b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de7b3-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="de7b3-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="de7b3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de7b3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de7b3-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="de7b3-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7b3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de7b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7b3-125">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="de7b3-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="de7b3-126">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="de7b3-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="de7b3-127">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="de7b3-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




