---
description: Restituisce un handle per il dispositivo associato a questo canale autenticato.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305425"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="893d5-103">\_DEVICEHANDLE D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="893d5-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="893d5-104">Restituisce un handle per il dispositivo associato a questo canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="893d5-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="893d5-105">È possibile utilizzare questo handle per verificare se due canali autenticati comunicano con lo stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="893d5-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="893d5-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="893d5-106">Requirement</span></span> | <span data-ttu-id="893d5-107">Valore</span><span class="sxs-lookup"><span data-stu-id="893d5-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="893d5-108">GUID query</span><span class="sxs-lookup"><span data-stu-id="893d5-108">Query GUID</span></span>  | <span data-ttu-id="893d5-109">**\_DEVICEHANDLE D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="893d5-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="893d5-110">Dati di input</span><span class="sxs-lookup"><span data-stu-id="893d5-110">Input data</span></span>  | [<span data-ttu-id="893d5-111">**\_Input query \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="893d5-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="893d5-112">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="893d5-112">Return data</span></span> | [<span data-ttu-id="893d5-113">**\_Output QUERYDEVICEHANDLE \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="893d5-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="893d5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="893d5-114">Remarks</span></span>

<span data-ttu-id="893d5-115">Questa query è valida per tutti i tipi di canale.</span><span class="sxs-lookup"><span data-stu-id="893d5-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="893d5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="893d5-116">Requirements</span></span>



| <span data-ttu-id="893d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="893d5-117">Requirement</span></span> | <span data-ttu-id="893d5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="893d5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="893d5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="893d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="893d5-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="893d5-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="893d5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="893d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="893d5-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="893d5-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="893d5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="893d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="893d5-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="893d5-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="893d5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="893d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893d5-126">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="893d5-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="893d5-127">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="893d5-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="893d5-128">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="893d5-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




