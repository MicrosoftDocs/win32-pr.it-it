---
title: Messaggio LB_GETANCHORINDEX (winuser. h)
description: Ottiene l'indice dell'elemento di ancoraggio \ 8212, ovvero l'elemento da cui inizia una selezione multipla. Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- Controlli di Windows Message LB_GETANCHORINDEX
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5502a234424b818bb46e9c4326839b5aff2f83d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518868"
---
# <a name="lb_getanchorindex-message"></a><span data-ttu-id="5a28b-105">\_Messaggio GETANCHORINDEX lb</span><span class="sxs-lookup"><span data-stu-id="5a28b-105">LB\_GETANCHORINDEX message</span></span>

<span data-ttu-id="5a28b-106">Ottiene l'indice dell'elemento di ancoraggio, ovvero l'elemento da cui inizia una selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="5a28b-106">Gets the index of the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="5a28b-107">Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="5a28b-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a28b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a28b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a28b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a28b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a28b-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5a28b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5a28b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a28b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a28b-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5a28b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a28b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a28b-113">Return value</span></span>

<span data-ttu-id="5a28b-114">Il valore restituito è l'indice dell'elemento di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="5a28b-114">The return value is the index of the anchor item.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a28b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a28b-115">Requirements</span></span>



| <span data-ttu-id="5a28b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a28b-116">Requirement</span></span> | <span data-ttu-id="5a28b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5a28b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a28b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a28b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a28b-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a28b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a28b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a28b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a28b-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a28b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a28b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a28b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a28b-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a28b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a28b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a28b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a28b-125">**\_SETANCHORINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="5a28b-125">**LB\_SETANCHORINDEX**</span></span>](lb-setanchorindex.md)
</dt> </dl>

 

 





