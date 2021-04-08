---
title: Messaggio BM_SETCHECK (winuser. h)
description: Imposta lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di controllo Button.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Controlli di Windows Message BM_SETCHECK
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047944"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="3481b-105">Messaggio BM ( \_ SEcheck)</span><span class="sxs-lookup"><span data-stu-id="3481b-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="3481b-106">Imposta lo stato di selezione di un pulsante di opzione o di una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="3481b-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="3481b-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**\_ controllo Button**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .</span><span class="sxs-lookup"><span data-stu-id="3481b-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3481b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3481b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3481b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3481b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3481b-110">Stato di selezione.</span><span class="sxs-lookup"><span data-stu-id="3481b-110">The check state.</span></span> <span data-ttu-id="3481b-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3481b-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3481b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3481b-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="3481b-113">Significato</span><span class="sxs-lookup"><span data-stu-id="3481b-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="3481b-114"><dt>**\_controllo BST**</dt></span><span class="sxs-lookup"><span data-stu-id="3481b-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="3481b-115">Imposta lo stato del pulsante su controllato.</span><span class="sxs-lookup"><span data-stu-id="3481b-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="3481b-116"><dt>**BST \_ INdeterminato**</dt></span><span class="sxs-lookup"><span data-stu-id="3481b-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="3481b-117">Imposta lo stato del pulsante su grigio, che indica uno stato indeterminato.</span><span class="sxs-lookup"><span data-stu-id="3481b-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="3481b-118">Usare questo valore solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3481b-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="3481b-119"><dt>**BST \_ DEselezionata**</dt></span><span class="sxs-lookup"><span data-stu-id="3481b-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="3481b-120">Imposta lo stato del pulsante su deselezionato.</span><span class="sxs-lookup"><span data-stu-id="3481b-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3481b-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3481b-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3481b-122">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3481b-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3481b-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3481b-123">Return value</span></span>

<span data-ttu-id="3481b-124">Questo messaggio restituisce sempre zero.</span><span class="sxs-lookup"><span data-stu-id="3481b-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3481b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3481b-125">Remarks</span></span>

<span data-ttu-id="3481b-126">Il messaggio **BM \_ secheck** non ha alcun effetto sui pulsanti di push.</span><span class="sxs-lookup"><span data-stu-id="3481b-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="3481b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3481b-127">Requirements</span></span>



| <span data-ttu-id="3481b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3481b-128">Requirement</span></span> | <span data-ttu-id="3481b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3481b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3481b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3481b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3481b-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3481b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3481b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3481b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3481b-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3481b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3481b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3481b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3481b-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3481b-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3481b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3481b-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="3481b-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3481b-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3481b-138">**GetCheck BM \_**</span><span class="sxs-lookup"><span data-stu-id="3481b-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="3481b-139">**BM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="3481b-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="3481b-140">**STATO di BM \_**</span><span class="sxs-lookup"><span data-stu-id="3481b-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





