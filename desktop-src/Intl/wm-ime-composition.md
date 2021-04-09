---
description: Inviato a un'applicazione quando l'IME modifica lo stato di composizione come risultato di una sequenza di tasti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Messaggio WM_IME_COMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968676"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="32f57-104">\_Messaggio di \_ composizione IME WM</span><span class="sxs-lookup"><span data-stu-id="32f57-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="32f57-105">Inviato a un'applicazione quando l'IME modifica lo stato di composizione come risultato di una sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="32f57-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="32f57-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="32f57-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="32f57-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="32f57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f57-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="32f57-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="32f57-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="32f57-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="32f57-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32f57-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32f57-111">Carattere DBCS che rappresenta l'ultima modifica apportata alla stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="32f57-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="32f57-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32f57-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32f57-113">Valore che specifica la modalità di modifica della stringa o del carattere di composizione.</span><span class="sxs-lookup"><span data-stu-id="32f57-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="32f57-114">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32f57-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="32f57-115">Per ulteriori informazioni su questi valori, vedere [valori stringa di composizione IME](ime-composition-string-values.md).</span><span class="sxs-lookup"><span data-stu-id="32f57-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="32f57-116">**comaccarezzatore cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="32f57-117">**COMPCLAUSE cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="32f57-118">**COMPREADSTR cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="32f57-119">**COMPREADATTR cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="32f57-120">**COMPREADCLAUSE cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="32f57-121">**COMPSTR cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="32f57-122">**CURSORPOS cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="32f57-123">**DELTASTART cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="32f57-124">**RESULTCLAUSE cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="32f57-125">**RESULTREADCLAUSE cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="32f57-126">**RESULTREADSTR cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="32f57-127">**RESULTSTR cataloghi globali \_**</span><span class="sxs-lookup"><span data-stu-id="32f57-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="32f57-128">Il parametro *lParam* può avere anche uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32f57-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="32f57-129">Valore</span><span class="sxs-lookup"><span data-stu-id="32f57-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="32f57-130">Significato</span><span class="sxs-lookup"><span data-stu-id="32f57-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="32f57-131"><dt>**CS \_ INSERTCHAR**</dt></span><span class="sxs-lookup"><span data-stu-id="32f57-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="32f57-132">Inserire il carattere di composizione *wParam* in corrispondenza del punto di inserimento corrente.</span><span class="sxs-lookup"><span data-stu-id="32f57-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="32f57-133">Un'applicazione deve visualizzare il carattere di composizione se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="32f57-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="32f57-134"><dt>**CS \_ NOMOVECARET**</dt></span><span class="sxs-lookup"><span data-stu-id="32f57-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="32f57-135">Non spostare la posizione del punto di inserimento in seguito all'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="32f57-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="32f57-136">Se, ad esempio, un IME specifica una combinazione di CS \_ INSERTCHAR e cs \_ NOMOVECARET, l'applicazione deve inserire il carattere specificato nella posizione corrente del cursore, ma non deve spostare il punto di inserimento alla posizione successiva.</span><span class="sxs-lookup"><span data-stu-id="32f57-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="32f57-137">Un \_ \_ messaggio di composizione IME WM successivo con cataloghi globali \_ RESULTSTR sostituirà questo carattere.</span><span class="sxs-lookup"><span data-stu-id="32f57-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f57-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32f57-138">Return value</span></span>

<span data-ttu-id="32f57-139">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="32f57-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32f57-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="32f57-140">Remarks</span></span>

<span data-ttu-id="32f57-141">Un'applicazione deve elaborare questo messaggio se Visualizza caratteri di composizione.</span><span class="sxs-lookup"><span data-stu-id="32f57-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="32f57-142">In caso contrario, deve inviare il messaggio alla finestra IME.</span><span class="sxs-lookup"><span data-stu-id="32f57-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="32f57-143">Se l'applicazione ha creato una finestra IME, deve passare questo messaggio alla finestra.</span><span class="sxs-lookup"><span data-stu-id="32f57-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="32f57-144">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passandolo alla finestra IME predefinita.</span><span class="sxs-lookup"><span data-stu-id="32f57-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="32f57-145">La finestra IME elabora questo messaggio aggiornando l'aspetto in base al flag di modifica specificato.</span><span class="sxs-lookup"><span data-stu-id="32f57-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="32f57-146">Un'applicazione può chiamare [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) per recuperare il nuovo stato di composizione.</span><span class="sxs-lookup"><span data-stu-id="32f57-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="32f57-147">Se non è impostato alcun valore di cataloghi globali \_ , il messaggio indica che la composizione corrente è stata annullata e che le applicazioni che traggono la stringa di composizione devono eliminare la stringa.</span><span class="sxs-lookup"><span data-stu-id="32f57-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f57-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32f57-148">Requirements</span></span>



| <span data-ttu-id="32f57-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f57-149">Requirement</span></span> | <span data-ttu-id="32f57-150">Valore</span><span class="sxs-lookup"><span data-stu-id="32f57-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f57-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f57-151">Minimum supported client</span></span><br/> | <span data-ttu-id="32f57-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32f57-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="32f57-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f57-153">Minimum supported server</span></span><br/> | <span data-ttu-id="32f57-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32f57-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="32f57-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32f57-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f57-156"><dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32f57-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f57-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32f57-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f57-158">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="32f57-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="32f57-159">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="32f57-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="32f57-160">**ImmGetCompositionString**</span><span class="sxs-lookup"><span data-stu-id="32f57-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
