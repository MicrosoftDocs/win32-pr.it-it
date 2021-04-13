---
title: Messaggio EM_GETLINECOUNT (winuser. h)
description: Ottiene il numero di righe in un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controlli di Windows Message EM_GETLINECOUNT
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475569"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="97f47-105">Messaggio EM_GETLINECOUNT (winuser. h)</span><span class="sxs-lookup"><span data-stu-id="97f47-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="97f47-106">Ottiene il numero di righe in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="97f47-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="97f47-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="97f47-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="97f47-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="97f47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97f47-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97f47-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97f47-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="97f47-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="97f47-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97f47-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97f47-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="97f47-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97f47-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97f47-113">Return value</span></span>

<span data-ttu-id="97f47-114">Il valore restituito è un Integer che specifica il numero totale di righe di testo nel controllo di modifica su più righe o in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="97f47-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="97f47-115">Se il controllo non ha testo, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="97f47-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="97f47-116">Il valore restituito non sarà mai minore di 1.</span><span class="sxs-lookup"><span data-stu-id="97f47-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="97f47-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="97f47-117">Remarks</span></span>

<span data-ttu-id="97f47-118">Il **messaggio \_ GETLINECOUNT em** Recupera il numero totale di righe di testo, non solo il numero di righe attualmente visibili.</span><span class="sxs-lookup"><span data-stu-id="97f47-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="97f47-119">Se la funzionalità WordWrap è abilitata, il numero di righe può cambiare quando cambiano le dimensioni della finestra di modifica.</span><span class="sxs-lookup"><span data-stu-id="97f47-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="97f47-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="97f47-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="97f47-121">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="97f47-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97f47-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97f47-122">Requirements</span></span>



| <span data-ttu-id="97f47-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="97f47-123">Requirement</span></span> | <span data-ttu-id="97f47-124">Valore</span><span class="sxs-lookup"><span data-stu-id="97f47-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f47-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97f47-125">Minimum supported client</span></span><br/> | <span data-ttu-id="97f47-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97f47-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97f47-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97f47-127">Minimum supported server</span></span><br/> | <span data-ttu-id="97f47-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97f47-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97f47-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97f47-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="97f47-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97f47-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f47-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97f47-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="97f47-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="97f47-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97f47-133">**\_riga em**</span><span class="sxs-lookup"><span data-stu-id="97f47-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="97f47-134">**\_LINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="97f47-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="97f47-135">**Modifica \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="97f47-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





