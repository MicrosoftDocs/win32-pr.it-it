---
title: Messaggio EM_SETIMESTATUS (winuser. h)
description: Imposta i flag di stato che determinano il modo in cui un controllo di modifica interagisce con l'IME (Input Method Editor).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Controlli di Windows Message EM_SETIMESTATUS
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742010"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="34038-104">\_Messaggio SETIMESTATUS em</span><span class="sxs-lookup"><span data-stu-id="34038-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="34038-105">Imposta i flag di stato che determinano il modo in cui un controllo di modifica interagisce con l'IME (Input Method Editor).</span><span class="sxs-lookup"><span data-stu-id="34038-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="34038-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34038-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34038-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34038-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34038-108">Tipo di stato da impostare.</span><span class="sxs-lookup"><span data-stu-id="34038-108">The type of status to set.</span></span> <span data-ttu-id="34038-109">Questo parametro può essere il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="34038-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="34038-110">Valore</span><span class="sxs-lookup"><span data-stu-id="34038-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="34038-111">Significato</span><span class="sxs-lookup"><span data-stu-id="34038-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="34038-112"><dt>**\_COMPOSITIONSTRING EMSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="34038-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="34038-113">Imposta il comportamento per la stringa di composizione di gestione.</span><span class="sxs-lookup"><span data-stu-id="34038-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34038-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34038-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34038-115">Dati specifici del tipo di stato.</span><span class="sxs-lookup"><span data-stu-id="34038-115">Data specific to the status type.</span></span> <span data-ttu-id="34038-116">Se *wParam* è **EMSIS \_ COMPOSITIONSTRING**, questo parametro può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="34038-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="34038-117">Valore</span><span class="sxs-lookup"><span data-stu-id="34038-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="34038-118">Significato</span><span class="sxs-lookup"><span data-stu-id="34038-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="34038-119"><dt>**\_GETCOMPSTRATONCE EIMES**</dt></span><span class="sxs-lookup"><span data-stu-id="34038-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="34038-120">Se questo flag è impostato, il controllo di modifica associa il messaggio di [**\_ \_ composizione IME WM**](/windows/desktop/Intl/wm-ime-composition) con *lParam* impostato su cataloghi globali \_ RESULTSTR e restituisce immediatamente la stringa di risultato.</span><span class="sxs-lookup"><span data-stu-id="34038-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="34038-121">Se questo flag non è impostato, il controllo di modifica passa il messaggio di **\_ \_ composizione IME WM** alla routine della finestra predefinita e gestisce la stringa di risultato dal messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; questo è il comportamento predefinito del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="34038-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="34038-122"><dt>**\_CANCELCOMPSTRINFOCUS EIMES**</dt></span><span class="sxs-lookup"><span data-stu-id="34038-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="34038-123">Se questo flag è impostato, il controllo di modifica annulla la stringa di composizione quando riceve il messaggio di [**\_ SetFocus di WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="34038-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="34038-124">Se questo flag non è impostato, il controllo di modifica non annulla la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="34038-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="34038-125"><dt>**\_COMPLETECOMPSTRKILLFOCUS EIMES**</dt></span><span class="sxs-lookup"><span data-stu-id="34038-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="34038-126">Se questo flag è impostato, il controllo di modifica completa la stringa di composizione al momento della ricezione del messaggio [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="34038-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="34038-127">Se questo flag non è impostato, il controllo di modifica non completerà la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="34038-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34038-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34038-128">Return value</span></span>

<span data-ttu-id="34038-129">Restituisce il valore precedente del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="34038-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="34038-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="34038-130">Remarks</span></span>

<span data-ttu-id="34038-131">**Modifica avanzata:** Il **messaggio \_ SETIMESTATUS em** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="34038-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="34038-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34038-132">Requirements</span></span>



| <span data-ttu-id="34038-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="34038-133">Requirement</span></span> | <span data-ttu-id="34038-134">Valore</span><span class="sxs-lookup"><span data-stu-id="34038-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34038-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34038-135">Minimum supported client</span></span><br/> | <span data-ttu-id="34038-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34038-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34038-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34038-137">Minimum supported server</span></span><br/> | <span data-ttu-id="34038-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34038-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34038-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34038-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="34038-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34038-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34038-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34038-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34038-142">**\_GETIMESTATUS em**</span><span class="sxs-lookup"><span data-stu-id="34038-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

