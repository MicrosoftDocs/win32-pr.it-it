---
title: Messaggio LB_RESETCONTENT (winuser. h)
description: Rimuove tutti gli elementi da una casella di riepilogo.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- Controlli di Windows Message LB_RESETCONTENT
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874349"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="3a241-104">\_Messaggio ResetContent lb</span><span class="sxs-lookup"><span data-stu-id="3a241-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="3a241-105">Rimuove tutti gli elementi da una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3a241-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a241-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a241-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a241-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a241-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a241-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a241-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a241-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a241-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a241-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a241-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a241-111">Return value</span></span>

<span data-ttu-id="3a241-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="3a241-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a241-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a241-113">Remarks</span></span>

<span data-ttu-id="3a241-114">Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il proprietario della casella di riepilogo riceve un messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) per ogni elemento nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="3a241-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a241-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a241-115">Requirements</span></span>



| <span data-ttu-id="3a241-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a241-116">Requirement</span></span> | <span data-ttu-id="3a241-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3a241-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a241-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a241-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a241-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a241-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a241-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a241-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a241-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a241-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a241-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a241-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a241-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a241-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a241-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a241-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a241-125">**\_DeleteItem WM**</span><span class="sxs-lookup"><span data-stu-id="3a241-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





