---
title: Messaggio LB_SETCURSEL (winuser. h)
description: Seleziona una stringa e la scorre nella visualizzazione, se necessario. Quando la nuova stringa è selezionata, la casella di riepilogo rimuove l'evidenziazione dalla stringa selezionata in precedenza.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Controlli di Windows Message LB_SETCURSEL
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302296"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="59b6f-105">\_Messaggio con maledizione lb</span><span class="sxs-lookup"><span data-stu-id="59b6f-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="59b6f-106">Seleziona una stringa e la scorre nella visualizzazione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="59b6f-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="59b6f-107">Quando la nuova stringa è selezionata, la casella di riepilogo rimuove l'evidenziazione dalla stringa selezionata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="59b6f-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="59b6f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="59b6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b6f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59b6f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59b6f-110">Specifica l'indice in base zero della stringa selezionata.</span><span class="sxs-lookup"><span data-stu-id="59b6f-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="59b6f-111">Se questo parametro è-1, la casella di riepilogo è impostata su nessuna selezione.</span><span class="sxs-lookup"><span data-stu-id="59b6f-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="59b6f-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="59b6f-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="59b6f-113">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="59b6f-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="59b6f-114">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="59b6f-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="59b6f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59b6f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59b6f-116">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="59b6f-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b6f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59b6f-117">Return value</span></span>

<span data-ttu-id="59b6f-118">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="59b6f-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="59b6f-119">Se il parametro *wParam* è-1, il valore restituito è lb \_ Err anche se non si è verificato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="59b6f-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b6f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="59b6f-120">Remarks</span></span>

<span data-ttu-id="59b6f-121">Utilizzare questo messaggio solo con le caselle di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="59b6f-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="59b6f-122">Non è possibile usarlo per impostare o rimuovere una selezione in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="59b6f-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b6f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59b6f-123">Requirements</span></span>



| <span data-ttu-id="59b6f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b6f-124">Requirement</span></span> | <span data-ttu-id="59b6f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="59b6f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b6f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59b6f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="59b6f-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59b6f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="59b6f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59b6f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="59b6f-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59b6f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59b6f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59b6f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b6f-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59b6f-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b6f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59b6f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b6f-133">**LB \_ GETcursel**</span><span class="sxs-lookup"><span data-stu-id="59b6f-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





