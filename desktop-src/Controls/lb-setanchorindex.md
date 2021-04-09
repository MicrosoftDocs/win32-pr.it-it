---
title: Messaggio LB_SETANCHORINDEX (winuser. h)
description: Imposta l'elemento di ancoraggio \ 8212, ovvero l'elemento da cui inizia una selezione multipla. Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Controlli di Windows Message LB_SETANCHORINDEX
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121010"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="404ff-105">\_Messaggio SETANCHORINDEX lb</span><span class="sxs-lookup"><span data-stu-id="404ff-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="404ff-106">Imposta l'elemento di ancoraggio, ovvero l'elemento da cui inizia una selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="404ff-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="404ff-107">Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="404ff-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="404ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="404ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="404ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="404ff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="404ff-110">Specifica l'indice del nuovo elemento di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="404ff-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="404ff-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="404ff-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="404ff-112">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="404ff-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="404ff-113">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="404ff-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="404ff-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="404ff-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="404ff-115">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="404ff-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="404ff-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="404ff-116">Return value</span></span>

<span data-ttu-id="404ff-117">Se il messaggio ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="404ff-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="404ff-118">Se il messaggio ha esito negativo, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="404ff-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="404ff-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="404ff-119">Requirements</span></span>



| <span data-ttu-id="404ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="404ff-120">Requirement</span></span> | <span data-ttu-id="404ff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="404ff-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="404ff-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="404ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="404ff-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="404ff-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="404ff-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="404ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="404ff-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="404ff-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="404ff-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="404ff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="404ff-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="404ff-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="404ff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="404ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404ff-129">**\_GETANCHORINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="404ff-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





