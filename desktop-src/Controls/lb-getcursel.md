---
title: Messaggio LB_GETCURSEL (winuser. h)
description: Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Controlli di Windows Message LB_GETCURSEL
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048709"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="c4c1c-104">LB- \_ messaggio GETcursel</span><span class="sxs-lookup"><span data-stu-id="c4c1c-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="c4c1c-105">Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4c1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c1c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4c1c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c1c-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4c1c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4c1c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c1c-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c1c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4c1c-111">Return value</span></span>

<span data-ttu-id="c4c1c-112">In una casella di riepilogo a selezione singola, il valore restituito è l'indice in base zero dell'elemento attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="c4c1c-113">Se non è presente alcuna selezione, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c1c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4c1c-114">Remarks</span></span>

<span data-ttu-id="c4c1c-115">Per recuperare gli indici degli elementi selezionati in una casella di riepilogo a selezione multipla, usare il messaggio [**lb \_ GETSELITEMS**](lb-getselitems.md) .</span><span class="sxs-lookup"><span data-stu-id="c4c1c-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="c4c1c-116">Per determinare se l'elemento con il rettangolo di attivazione in una casella di riepilogo a selezione multipla è selezionato, usare il messaggio [**lb \_ GETSEL**](lb-getsel.md) .</span><span class="sxs-lookup"><span data-stu-id="c4c1c-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="c4c1c-117">Se viene inviato a una casella di riepilogo a selezione multipla, **lb \_ GetCurSel** restituisce l'indice dell'elemento con il rettangolo di attivazione.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="c4c1c-118">Se non è selezionato alcun elemento, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c1c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4c1c-119">Requirements</span></span>



| <span data-ttu-id="c4c1c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c1c-120">Requirement</span></span> | <span data-ttu-id="c4c1c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c1c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c1c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c1c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c1c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4c1c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4c1c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c1c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c1c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4c1c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4c1c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4c1c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c1c-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c1c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c1c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4c1c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4c1c-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c4c1c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4c1c-130">**\_GETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="c4c1c-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="c4c1c-131">**\_GETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="c4c1c-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="c4c1c-132">**\_GETSELITEMS lb**</span><span class="sxs-lookup"><span data-stu-id="c4c1c-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="c4c1c-133">**di \_ lb**</span><span class="sxs-lookup"><span data-stu-id="c4c1c-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





