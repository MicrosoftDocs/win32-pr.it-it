---
title: Messaggio LB_GETCARETINDEX (winuser. h)
description: Recupera l'indice dell'elemento con lo stato attivo in una casella di riepilogo a selezione multipla. L'elemento può essere selezionato o meno.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Controlli di Windows Message LB_GETCARETINDEX
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048710"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="034ff-105">\_Messaggio GETCARETINDEX lb</span><span class="sxs-lookup"><span data-stu-id="034ff-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="034ff-106">Recupera l'indice dell'elemento con lo stato attivo in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="034ff-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="034ff-107">L'elemento può essere selezionato o meno.</span><span class="sxs-lookup"><span data-stu-id="034ff-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="034ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="034ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="034ff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="034ff-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="034ff-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="034ff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="034ff-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="034ff-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="034ff-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="034ff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="034ff-113">Return value</span></span>

<span data-ttu-id="034ff-114">Il valore restituito è l'indice in base zero dell'elemento della casella di riepilogo con stato attivo oppure 0 se nessun elemento ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="034ff-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="034ff-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="034ff-115">Remarks</span></span>

<span data-ttu-id="034ff-116">Questo messaggio può essere usato anche per ottenere l'indice dell'elemento attualmente selezionato in una casella di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="034ff-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="034ff-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="034ff-117">Requirements</span></span>



| <span data-ttu-id="034ff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="034ff-118">Requirement</span></span> | <span data-ttu-id="034ff-119">Valore</span><span class="sxs-lookup"><span data-stu-id="034ff-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="034ff-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="034ff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="034ff-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="034ff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="034ff-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="034ff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="034ff-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="034ff-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="034ff-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="034ff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="034ff-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="034ff-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034ff-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="034ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034ff-127">**\_SETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="034ff-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





