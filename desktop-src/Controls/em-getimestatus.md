---
title: Messaggio EM_GETIMESTATUS (winuser. h)
description: Ottiene un set di flag di stato che indicano il modo in cui il controllo di modifica interagisce con l'IME (Input Method Editor).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Controlli di Windows Message EM_GETIMESTATUS
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120731"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="7ca8b-104">\_Messaggio GETIMESTATUS em</span><span class="sxs-lookup"><span data-stu-id="7ca8b-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="7ca8b-105">Ottiene un set di flag di stato che indicano il modo in cui il controllo di modifica interagisce con l'IME (Input Method Editor).</span><span class="sxs-lookup"><span data-stu-id="7ca8b-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="7ca8b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ca8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca8b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ca8b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca8b-108">Tipo di stato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-108">The type of status to retrieve.</span></span> <span data-ttu-id="7ca8b-109">Questo parametro può essere il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="7ca8b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7ca8b-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="7ca8b-111">Significato</span><span class="sxs-lookup"><span data-stu-id="7ca8b-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="7ca8b-112"><dt>**\_COMPOSITIONSTRING EMSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca8b-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="7ca8b-113">Imposta il comportamento per la gestione della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7ca8b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ca8b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca8b-115">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca8b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ca8b-116">Return value</span></span>

<span data-ttu-id="7ca8b-117">Dati specifici del tipo di stato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="7ca8b-118">Con il valore **EMSIS \_ COMPOSITIONSTRING** per *status*, questo valore restituito corrisponde a uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="7ca8b-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ca8b-119">Return code</span></span>                                                                                                    | <span data-ttu-id="7ca8b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ca8b-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ca8b-121"><dt>**\_GETCOMPSTRATONCE EIMES**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca8b-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="7ca8b-122">Se questo flag è impostato, il controllo di modifica associa il messaggio di [**\_ \_ composizione IME WM**](/windows/desktop/Intl/wm-ime-composition) a *fFlags* impostato su GC \_ RESULTSTR e restituisce immediatamente la stringa di risultato.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="7ca8b-123">Se questo flag non è impostato, il controllo di modifica passa il messaggio di **\_ \_ composizione IME WM** alla routine della finestra predefinita ed elabora la stringa di risultato dal messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; questo è il comportamento predefinito del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="7ca8b-124"><dt>**\_CANCELCOMPSTRINFOCUS EIMES**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca8b-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="7ca8b-125">Se questo flag è impostato, il controllo di modifica annulla la stringa di composizione quando riceve il messaggio di [**\_ SetFocus di WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="7ca8b-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="7ca8b-126">Se questo flag non è impostato, il controllo di modifica non annulla la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="7ca8b-127"><dt>**\_COMPLETECOMPSTRKILLFOCUS EIMES**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca8b-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="7ca8b-128">Se questo flag è impostato, il controllo di modifica completa la stringa di composizione al momento della ricezione del messaggio [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="7ca8b-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="7ca8b-129">Se questo flag non è impostato, il controllo di modifica non completerà la stringa di composizione. Questo è il comportamento predefinito del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="7ca8b-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ca8b-130">Remarks</span></span>

<span data-ttu-id="7ca8b-131">**Modifica avanzata:** Il **messaggio \_ GETIMESTATUS em** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7ca8b-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca8b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ca8b-132">Requirements</span></span>



| <span data-ttu-id="7ca8b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ca8b-133">Requirement</span></span> | <span data-ttu-id="7ca8b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7ca8b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca8b-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ca8b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca8b-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ca8b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ca8b-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ca8b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca8b-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ca8b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7ca8b-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ca8b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca8b-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca8b-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca8b-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ca8b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca8b-142">**\_SETIMESTATUS em**</span><span class="sxs-lookup"><span data-stu-id="7ca8b-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

