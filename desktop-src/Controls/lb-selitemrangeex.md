---
title: Messaggio LB_SELITEMRANGEEX (winuser. h)
description: Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Controlli di Windows Message LB_SELITEMRANGEEX
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964751"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="ffd50-104">\_Messaggio SELITEMRANGEEX lb</span><span class="sxs-lookup"><span data-stu-id="ffd50-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="ffd50-105">Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="ffd50-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffd50-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffd50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd50-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffd50-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd50-108">Specifica l'indice in base zero del primo elemento da selezionare.</span><span class="sxs-lookup"><span data-stu-id="ffd50-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="ffd50-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ffd50-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="ffd50-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="ffd50-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="ffd50-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="ffd50-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ffd50-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffd50-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd50-113">Specifica l'indice in base zero dell'ultimo elemento da selezionare.</span><span class="sxs-lookup"><span data-stu-id="ffd50-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd50-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffd50-114">Return value</span></span>

<span data-ttu-id="ffd50-115">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ffd50-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd50-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffd50-116">Remarks</span></span>

<span data-ttu-id="ffd50-117">Se il parametro *wParam* è inferiore al parametro *lParam* , viene selezionato l'intervallo di elementi specificato.</span><span class="sxs-lookup"><span data-stu-id="ffd50-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="ffd50-118">Se *wParam* è maggiore o uguale a *lParam*, l'intervallo viene rimosso dall'intervallo di elementi specificato.</span><span class="sxs-lookup"><span data-stu-id="ffd50-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="ffd50-119">Per selezionare un solo elemento, selezionare due elementi, quindi deselezionare l'elemento indesiderato.</span><span class="sxs-lookup"><span data-stu-id="ffd50-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="ffd50-120">Utilizzare questo messaggio solo con caselle di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="ffd50-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="ffd50-121">Questo messaggio può selezionare un intervallo solo entro i primi 65.536 elementi.</span><span class="sxs-lookup"><span data-stu-id="ffd50-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd50-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffd50-122">Requirements</span></span>



| <span data-ttu-id="ffd50-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd50-123">Requirement</span></span> | <span data-ttu-id="ffd50-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ffd50-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd50-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffd50-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd50-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ffd50-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ffd50-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffd50-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd50-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ffd50-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ffd50-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffd50-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd50-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffd50-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffd50-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffd50-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ffd50-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ffd50-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd50-133">**\_SELITEMRANGE lb**</span><span class="sxs-lookup"><span data-stu-id="ffd50-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="ffd50-134">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="ffd50-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





