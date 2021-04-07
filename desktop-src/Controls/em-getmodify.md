---
title: Messaggio EM_GETMODIFY (winuser. h)
description: Ottiene lo stato del flag di modifica del controllo di modifica. Il flag indica se il contenuto del controllo di modifica è stato modificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Controlli di Windows Message EM_GETMODIFY
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873433"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="42820-106">\_Messaggio GETMODIFY em</span><span class="sxs-lookup"><span data-stu-id="42820-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="42820-107">Ottiene lo stato del flag di modifica del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="42820-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="42820-108">Il flag indica se il contenuto del controllo di modifica è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="42820-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="42820-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="42820-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="42820-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="42820-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42820-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42820-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42820-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="42820-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="42820-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42820-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42820-114">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="42820-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42820-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42820-115">Return value</span></span>

<span data-ttu-id="42820-116">Se il contenuto del controllo di modifica è stato modificato, il valore restituito è diverso da zero; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="42820-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="42820-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="42820-117">Remarks</span></span>

<span data-ttu-id="42820-118">Il sistema cancella automaticamente il flag di modifica a zero quando viene creato il controllo.</span><span class="sxs-lookup"><span data-stu-id="42820-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="42820-119">Se l'utente modifica il testo del controllo, il sistema imposta il flag su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="42820-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="42820-120">Per impostare o deselezionare il flag, è possibile inviare il messaggio di modifica [**em \_**](em-setmodify.md) per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="42820-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="42820-121">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="42820-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="42820-122">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="42820-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42820-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42820-123">Requirements</span></span>



| <span data-ttu-id="42820-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42820-124">Requirement</span></span> | <span data-ttu-id="42820-125">Valore</span><span class="sxs-lookup"><span data-stu-id="42820-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42820-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42820-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42820-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42820-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42820-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42820-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42820-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42820-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42820-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42820-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="42820-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42820-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42820-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42820-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42820-133">**MODIFICA di EM \_**</span><span class="sxs-lookup"><span data-stu-id="42820-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 





