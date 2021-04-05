---
title: Messaggio LB_GETSEL (winuser. h)
description: Ottiene lo stato di selezione di un elemento.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- Controlli di Windows Message LB_GETSEL
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874025"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="18178-104">\_Messaggio GETSEL lb</span><span class="sxs-lookup"><span data-stu-id="18178-104">LB\_GETSEL message</span></span>

<span data-ttu-id="18178-105">Ottiene lo stato di selezione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="18178-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="18178-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18178-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18178-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18178-108">Indice in base zero di un elemento.</span><span class="sxs-lookup"><span data-stu-id="18178-108">The zero-based index of the item.</span></span>

<span data-ttu-id="18178-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="18178-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="18178-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="18178-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="18178-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="18178-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="18178-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18178-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18178-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="18178-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18178-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18178-114">Return value</span></span>

<span data-ttu-id="18178-115">Se viene selezionato un elemento, il valore restituito è maggiore di zero; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="18178-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="18178-116">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="18178-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="18178-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18178-117">Requirements</span></span>



| <span data-ttu-id="18178-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="18178-118">Requirement</span></span> | <span data-ttu-id="18178-119">Valore</span><span class="sxs-lookup"><span data-stu-id="18178-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18178-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18178-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18178-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18178-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18178-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18178-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18178-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18178-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18178-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18178-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18178-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18178-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18178-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18178-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18178-127">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="18178-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





