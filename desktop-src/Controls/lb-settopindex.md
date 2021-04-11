---
title: Messaggio LB_SETTOPINDEX (winuser. h)
description: Assicura che l'elemento specificato in una casella di riepilogo sia visibile.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- Controlli di Windows Message LB_SETTOPINDEX
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120999"
---
# <a name="lb_settopindex-message"></a><span data-ttu-id="e6a5e-104">\_Messaggio SETTOPINDEX lb</span><span class="sxs-lookup"><span data-stu-id="e6a5e-104">LB\_SETTOPINDEX message</span></span>

<span data-ttu-id="e6a5e-105">Assicura che l'elemento specificato in una casella di riepilogo sia visibile.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-105">Ensures that the specified item in a list box is visible.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6a5e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6a5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a5e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6a5e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a5e-108">Indice in base zero dell'elemento nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-108">The zero-based index of the item in the list box.</span></span>

<span data-ttu-id="e6a5e-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="e6a5e-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="e6a5e-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="e6a5e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6a5e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a5e-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a5e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6a5e-114">Return value</span></span>

<span data-ttu-id="e6a5e-115">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a5e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6a5e-116">Remarks</span></span>

<span data-ttu-id="e6a5e-117">Il sistema scorre il contenuto della casella di riepilogo in modo che l'elemento specificato venga visualizzato nella parte superiore della casella di riepilogo oppure che sia stato raggiunto l'intervallo massimo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-117">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a5e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6a5e-118">Requirements</span></span>



| <span data-ttu-id="e6a5e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a5e-119">Requirement</span></span> | <span data-ttu-id="e6a5e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e6a5e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a5e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a5e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a5e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6a5e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6a5e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a5e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a5e-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6a5e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6a5e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6a5e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a5e-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6a5e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a5e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6a5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a5e-128">**\_GETTOPINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="e6a5e-128">**LB\_GETTOPINDEX**</span></span>](lb-gettopindex.md)
</dt> </dl>

 

 





