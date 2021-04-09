---
title: Messaggio di EM_GETIMEPROPERTY (RichEdit. h)
description: Recupera la proprietà e le funzionalità dell'IME (Input Method Editor) associate alle impostazioni locali di input correnti.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Controlli di Windows Message EM_GETIMEPROPERTY
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120734"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="575c7-104">\_Messaggio GETIMEPROPERTY em</span><span class="sxs-lookup"><span data-stu-id="575c7-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="575c7-105">Recupera la proprietà e le funzionalità dell'IME (Input Method Editor) associate alle impostazioni locali di input correnti.</span><span class="sxs-lookup"><span data-stu-id="575c7-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="575c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="575c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="575c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="575c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="575c7-108">Specifica il tipo di informazioni di proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="575c7-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="575c7-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="575c7-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="575c7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="575c7-111">Significato</span><span class="sxs-lookup"><span data-stu-id="575c7-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="575c7-112"><dt>**\_Proprietà IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="575c7-113">Informazioni sulle proprietà.</span><span class="sxs-lookup"><span data-stu-id="575c7-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="575c7-114"><dt>**\_conversione IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="575c7-115">Funzionalità di conversione.</span><span class="sxs-lookup"><span data-stu-id="575c7-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="575c7-116"><dt>**\_frase IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="575c7-117">Funzionalità della modalità frase.</span><span class="sxs-lookup"><span data-stu-id="575c7-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="575c7-118"><dt>**\_interfaccia utente IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="575c7-119">Funzionalità dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="575c7-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="575c7-120"><dt>**\_SETCOMPSTR IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="575c7-121">Funzionalità della stringa di composizione.</span><span class="sxs-lookup"><span data-stu-id="575c7-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="575c7-122"><dt>**\_Select IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="575c7-123">Funzionalità di ereditarietà della selezione.</span><span class="sxs-lookup"><span data-stu-id="575c7-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="575c7-124"><dt>**\_GETIMEVERSION IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="575c7-125">Recupera il numero di versione del sistema per il quale è stato creato l'IME specificato.</span><span class="sxs-lookup"><span data-stu-id="575c7-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="575c7-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="575c7-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="575c7-127">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="575c7-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="575c7-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="575c7-128">Return value</span></span>

<span data-ttu-id="575c7-129">Restituisce la proprietà o il valore della funzionalità, a seconda del valore del parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="575c7-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="575c7-130">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="575c7-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="575c7-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="575c7-131">Remarks</span></span>

<span data-ttu-id="575c7-132">Se *wParam* è \_ la proprietà IGP, restituisce uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="575c7-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="575c7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="575c7-133">Requirement</span></span> | <span data-ttu-id="575c7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575c7-135">\_propt IME \_ al punto di \_ inserimento</span><span class="sxs-lookup"><span data-stu-id="575c7-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="575c7-136">Se impostato, la finestra di conversione si trova nella posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="575c7-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="575c7-137">Se è deselezionata, la finestra si trova vicino al punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="575c7-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="575c7-138">\_ \_ interfaccia utente speciale di IME Prop \_</span><span class="sxs-lookup"><span data-stu-id="575c7-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="575c7-139">Se impostato, l'IME ha un'interfaccia utente non standard.</span><span class="sxs-lookup"><span data-stu-id="575c7-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="575c7-140">Impossibile creare l'applicazione nella finestra IME.</span><span class="sxs-lookup"><span data-stu-id="575c7-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="575c7-141">\_ \_ \_ Inizio della pagina di inizio \_ della prop IME da \_ 1</span><span class="sxs-lookup"><span data-stu-id="575c7-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="575c7-142">Se impostato, le stringhe nell'elenco candidato sono numerate a partire da 1.</span><span class="sxs-lookup"><span data-stu-id="575c7-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="575c7-143">Se chiaro, le stringhe iniziano da zero.</span><span class="sxs-lookup"><span data-stu-id="575c7-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="575c7-144">\_Unicode Prop \_ IME</span><span class="sxs-lookup"><span data-stu-id="575c7-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="575c7-145">Se impostato, l'IME viene visualizzato come UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="575c7-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="575c7-146">Il sistema e l'IME comunicheranno tramite l'interfaccia UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="575c7-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="575c7-147">Se chiaro, l'IME utilizzerà l'interfaccia ANSI per comunicare con il sistema.</span><span class="sxs-lookup"><span data-stu-id="575c7-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="575c7-148">l' \_ operazione di propulsione IME è stata \_ completata \_ in \_ Unselect</span><span class="sxs-lookup"><span data-stu-id="575c7-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="575c7-149">Se impostato, la finestra di conversione si trova nella posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="575c7-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="575c7-150">Se è deselezionata, la finestra si trova vicino al punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="575c7-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="575c7-151">\_VKEY della prop IME \_ Accept \_ Wide \_</span><span class="sxs-lookup"><span data-stu-id="575c7-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="575c7-152">Se impostato, l'IME elabora il formato Unicode inserito dalla funzione [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) usando il \_ pacchetto VK.</span><span class="sxs-lookup"><span data-stu-id="575c7-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="575c7-153">Se chiaro, l'IME potrebbe non elaborare il formato Unicode inserito e il formato Unicode inserito potrebbe essere inviato direttamente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="575c7-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="575c7-154">Se *wParam* è \_ un'interfaccia utente IGP, restituisce uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="575c7-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="575c7-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="575c7-155">Requirement</span></span> | <span data-ttu-id="575c7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575c7-157">Estremità interfaccia utente \_ \_ 2700</span><span class="sxs-lookup"><span data-stu-id="575c7-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="575c7-158">Supporta i valori di escape del testo 0 o 2700.</span><span class="sxs-lookup"><span data-stu-id="575c7-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="575c7-159">Per ulteriori informazioni, vedere **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="575c7-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="575c7-160">Estremità interfaccia utente \_ \_ ROT90</span><span class="sxs-lookup"><span data-stu-id="575c7-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="575c7-161">Supporta i valori di escape del testo 0, 900, 1800 o 2700.</span><span class="sxs-lookup"><span data-stu-id="575c7-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="575c7-162">Per ulteriori informazioni, vedere **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="575c7-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="575c7-163">estremità interfaccia utente \_ \_ ROTANY</span><span class="sxs-lookup"><span data-stu-id="575c7-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="575c7-164">Supporta qualsiasi valore di escape del testo.</span><span class="sxs-lookup"><span data-stu-id="575c7-164">Supports any text escapement value.</span></span> <span data-ttu-id="575c7-165">Per ulteriori informazioni, vedere **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="575c7-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="575c7-166">Se *wParam* è IGP \_ SETCOMPSTR, restituisce uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="575c7-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="575c7-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="575c7-167">Requirement</span></span> | <span data-ttu-id="575c7-168">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575c7-169">\_COMPSTR Cap \_ SCS</span><span class="sxs-lookup"><span data-stu-id="575c7-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="575c7-170">È possibile creare la stringa di composizione chiamando la funzione [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con il \_ valore SCS SETSTR.</span><span class="sxs-lookup"><span data-stu-id="575c7-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="575c7-171">\_MAKEREAD Cap \_ SCS</span><span class="sxs-lookup"><span data-stu-id="575c7-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="575c7-172">Consente di creare la stringa di lettura dalla stringa di composizione corrispondente quando si usa la funzione [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con SCS \_ SETSTR e senza impostare *lpRead*.</span><span class="sxs-lookup"><span data-stu-id="575c7-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="575c7-173">\_SETRECONVERTSTRING Cap \_ SCS</span><span class="sxs-lookup"><span data-stu-id="575c7-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="575c7-174">Questo IME può supportare la riconversione.</span><span class="sxs-lookup"><span data-stu-id="575c7-174">This IME can support reconversion.</span></span> <span data-ttu-id="575c7-175">Usare [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) per eseguire la riconversione.</span><span class="sxs-lookup"><span data-stu-id="575c7-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="575c7-176">Se *wParam* è IGP \_ Select, restituisce uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="575c7-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="575c7-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="575c7-177">Requirement</span></span> | <span data-ttu-id="575c7-178">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="575c7-179">SELECT \_ Cap \_ CONVMODE</span><span class="sxs-lookup"><span data-stu-id="575c7-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="575c7-180">Eredita la modalità di conversione quando viene selezionato un nuovo IME.</span><span class="sxs-lookup"><span data-stu-id="575c7-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="575c7-181">Seleziona \_ \_ frase Cap</span><span class="sxs-lookup"><span data-stu-id="575c7-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="575c7-182">Eredita la modalità frase quando viene selezionato un nuovo IME.</span><span class="sxs-lookup"><span data-stu-id="575c7-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="575c7-183">Se *wParam* è IGP \_ GETIMEVERSION, restituisce uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="575c7-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="575c7-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="575c7-184">Requirement</span></span> | <span data-ttu-id="575c7-185">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="575c7-186">Immai \_ 0310</span><span class="sxs-lookup"><span data-stu-id="575c7-186">IMEVER\_0310</span></span> | <span data-ttu-id="575c7-187">L'IME è stato creato per Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="575c7-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="575c7-188">Immai \_ 0400</span><span class="sxs-lookup"><span data-stu-id="575c7-188">IMEVER\_0400</span></span> | <span data-ttu-id="575c7-189">L'IME è stato creato per Windows 95 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="575c7-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="575c7-190">Questo messaggio è simile a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), con la differenza che usa le impostazioni locali di input correnti.</span><span class="sxs-lookup"><span data-stu-id="575c7-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="575c7-191">Prima di chiamare questa funzione, l'applicazione deve chiamare [**em \_ ISIME**](em-isime.md) .</span><span class="sxs-lookup"><span data-stu-id="575c7-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="575c7-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="575c7-192">Requirements</span></span>



| <span data-ttu-id="575c7-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="575c7-193">Requirement</span></span> | <span data-ttu-id="575c7-194">Valore</span><span class="sxs-lookup"><span data-stu-id="575c7-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="575c7-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="575c7-195">Minimum supported client</span></span><br/> | <span data-ttu-id="575c7-196">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="575c7-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="575c7-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="575c7-197">Minimum supported server</span></span><br/> | <span data-ttu-id="575c7-198">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="575c7-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="575c7-199">Intestazione</span><span class="sxs-lookup"><span data-stu-id="575c7-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="575c7-200"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="575c7-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575c7-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="575c7-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="575c7-202">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="575c7-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="575c7-203">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="575c7-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="575c7-204">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="575c7-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="575c7-205">**ImmGetProperty**</span><span class="sxs-lookup"><span data-stu-id="575c7-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

