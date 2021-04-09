---
title: Messaggio BM_GETCHECK (winuser. h)
description: Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro del pulsante \_ GetCheck.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Controlli di Windows Message BM_GETCHECK
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121163"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="182c8-105">\_Messaggio BM GETcheck</span><span class="sxs-lookup"><span data-stu-id="182c8-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="182c8-106">Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="182c8-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="182c8-107">È possibile inviare questo messaggio in modo esplicito o usare la macro del [**pulsante \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .</span><span class="sxs-lookup"><span data-stu-id="182c8-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="182c8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="182c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="182c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="182c8-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="182c8-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="182c8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="182c8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="182c8-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="182c8-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182c8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="182c8-113">Return value</span></span>

<span data-ttu-id="182c8-114">Il valore restituito da un pulsante creato con le [**caselle di controllo \_ AUTOCHECKBOX**](button-styles.md)BS, [**BS \_ AUTORADIOBUTTON**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), BS [**\_ CheckBox**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)o [**BS \_ 3STATE**](button-styles.md) può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="182c8-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="182c8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="182c8-115">Return code</span></span>                                                                                       | <span data-ttu-id="182c8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="182c8-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="182c8-117"><dt>**\_controllo BST**</dt></span><span class="sxs-lookup"><span data-stu-id="182c8-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="182c8-118">Pulsante selezionato.</span><span class="sxs-lookup"><span data-stu-id="182c8-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="182c8-119"><dt>**BST \_ INdeterminato**</dt></span><span class="sxs-lookup"><span data-stu-id="182c8-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="182c8-120">Il pulsante è visualizzato in grigio, che indica uno stato indeterminato (si applica solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="182c8-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="182c8-121"><dt>**BST \_ DEselezionata**</dt></span><span class="sxs-lookup"><span data-stu-id="182c8-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="182c8-122">Il pulsante è deselezionato</span><span class="sxs-lookup"><span data-stu-id="182c8-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="182c8-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="182c8-123">Remarks</span></span>

<span data-ttu-id="182c8-124">Se il pulsante presenta uno stile diverso da quelli elencati, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="182c8-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="182c8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="182c8-125">Requirements</span></span>



| <span data-ttu-id="182c8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="182c8-126">Requirement</span></span> | <span data-ttu-id="182c8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="182c8-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182c8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="182c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="182c8-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="182c8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="182c8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="182c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="182c8-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="182c8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="182c8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="182c8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="182c8-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="182c8-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="182c8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="182c8-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="182c8-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="182c8-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="182c8-136">**BM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="182c8-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="182c8-137">**\_controllo BM**</span><span class="sxs-lookup"><span data-stu-id="182c8-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





