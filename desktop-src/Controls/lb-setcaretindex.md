---
title: Messaggio LB_SETCARETINDEX (winuser. h)
description: Imposta il rettangolo di attivazione sull'elemento in corrispondenza dell'indice specificato in una casella di riepilogo a selezione multipla. Se l'elemento non è visibile, viene spostato nella visualizzazione.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Controlli di Windows Message LB_SETCARETINDEX
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874341"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="efac4-105">\_Messaggio SETCARETINDEX lb</span><span class="sxs-lookup"><span data-stu-id="efac4-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="efac4-106">Imposta il rettangolo di attivazione sull'elemento in corrispondenza dell'indice specificato in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="efac4-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="efac4-107">Se l'elemento non è visibile, viene spostato nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="efac4-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="efac4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efac4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efac4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efac4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efac4-110">Specifica l'indice in base zero dell'elemento della casella di riepilogo che deve ricevere il rettangolo di attivazione.</span><span class="sxs-lookup"><span data-stu-id="efac4-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="efac4-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="efac4-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="efac4-112">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="efac4-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="efac4-113">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="efac4-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="efac4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efac4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efac4-115">Se questo valore è **false**, l'elemento viene spostato fino a quando non è completamente visibile; Se è **true**, l'elemento viene sottoposta a scorrimento fino a quando non è visibile almeno parzialmente.</span><span class="sxs-lookup"><span data-stu-id="efac4-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efac4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efac4-116">Return value</span></span>

<span data-ttu-id="efac4-117">Se si verifica un errore, il valore restituito è LB \_ Err (-1).</span><span class="sxs-lookup"><span data-stu-id="efac4-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="efac4-118">In caso contrario, \_ viene restituito lb OK (0).</span><span class="sxs-lookup"><span data-stu-id="efac4-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="efac4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="efac4-119">Remarks</span></span>

<span data-ttu-id="efac4-120">Se questo messaggio viene inviato a una casella di riepilogo a selezione singola che non contiene un elemento selezionato, l'indice del cursore viene impostato sull'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="efac4-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="efac4-121">Se la casella di riepilogo a selezione singola contiene un elemento selezionato, la casella di riepilogo restituisce LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="efac4-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="efac4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efac4-122">Requirements</span></span>



| <span data-ttu-id="efac4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="efac4-123">Requirement</span></span> | <span data-ttu-id="efac4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="efac4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efac4-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efac4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="efac4-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efac4-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="efac4-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efac4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="efac4-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efac4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="efac4-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efac4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="efac4-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efac4-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efac4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efac4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efac4-132">**\_GETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="efac4-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





