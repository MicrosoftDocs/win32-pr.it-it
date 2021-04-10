---
title: Messaggio LB_GETSELCOUNT (winuser. h)
description: Ottiene il numero totale di elementi selezionati in una casella di riepilogo a selezione multipla.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- Controlli di Windows Message LB_GETSELCOUNT
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119474"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="6b76e-104">\_Messaggio GETSELCOUNT lb</span><span class="sxs-lookup"><span data-stu-id="6b76e-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="6b76e-105">Ottiene il numero totale di elementi selezionati in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="6b76e-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b76e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b76e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b76e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b76e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b76e-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6b76e-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b76e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b76e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b76e-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6b76e-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b76e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b76e-111">Return value</span></span>

<span data-ttu-id="6b76e-112">Il valore restituito è il numero di elementi selezionati nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6b76e-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="6b76e-113">Se la casella di riepilogo è una casella di riepilogo a selezione singola, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6b76e-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b76e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b76e-114">Requirements</span></span>



| <span data-ttu-id="6b76e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b76e-115">Requirement</span></span> | <span data-ttu-id="6b76e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6b76e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b76e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b76e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b76e-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b76e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6b76e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b76e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b76e-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b76e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b76e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b76e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b76e-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b76e-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b76e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b76e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b76e-124">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="6b76e-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





