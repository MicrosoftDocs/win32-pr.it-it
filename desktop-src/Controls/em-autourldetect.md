---
title: Messaggio di EM_AUTOURLDETECT (RichEdit. h)
description: Abilita o Disabilita il rilevamento automatico dei collegamenti ipertestuali da un controllo Rich Edit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Controlli di Windows Message EM_AUTOURLDETECT
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964482"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="99ec6-104">\_Messaggio AUTOURLDETECT em</span><span class="sxs-lookup"><span data-stu-id="99ec6-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="99ec6-105">Abilita o Disabilita il rilevamento automatico dei collegamenti ipertestuali da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="99ec6-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="99ec6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99ec6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99ec6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99ec6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99ec6-108">Specificare 0 per disabilitare il rilevamento automatico dei collegamenti oppure uno dei valori seguenti per abilitare vari tipi di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="99ec6-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="99ec6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="99ec6-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="99ec6-110">Significato</span><span class="sxs-lookup"><span data-stu-id="99ec6-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="99ec6-111"><dt>**\_DISABLEMIXEDLGC AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="99ec6-112">**Windows 8**: disabilitare il riconoscimento dei nomi di dominio che contengono etichette con caratteri appartenenti a più di uno degli script seguenti: Latino, greco e cirillico.</span><span class="sxs-lookup"><span data-stu-id="99ec6-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="99ec6-113"><dt>**\_ENABLEDRIVELETTERS AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="99ec6-114">**Windows 8**: riconoscere i nomi di file con una specifica di unità, ad esempio c: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="99ec6-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="99ec6-115"><dt>**\_ENABLEEA AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="99ec6-116">Questo valore è deprecato; in alternativa, usare **AURL \_ ENABLEEAURLS** .</span><span class="sxs-lookup"><span data-stu-id="99ec6-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="99ec6-117"><dt>**\_ENABLEEAURLS AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="99ec6-118">Riconoscere gli URL che contengono caratteri asiatici orientali.</span><span class="sxs-lookup"><span data-stu-id="99ec6-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="99ec6-119"><dt>**\_ENABLEEMAILADDR AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="99ec6-120">**Windows 8**: riconoscere gli indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="99ec6-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="99ec6-121"><dt>**\_ENABLETELNO AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="99ec6-122">**Windows 8**: riconoscere i numeri di telefono.</span><span class="sxs-lookup"><span data-stu-id="99ec6-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="99ec6-123"><dt>**\_ENABLEURL AURL**</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="99ec6-124">**Windows 8**: riconoscere gli URL che includono il percorso.</span><span class="sxs-lookup"><span data-stu-id="99ec6-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="99ec6-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99ec6-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99ec6-126">Questo parametro determina gli schemi URL riconosciuti se il **\_ ENABLEURL AURL** è attivo.</span><span class="sxs-lookup"><span data-stu-id="99ec6-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="99ec6-127">Se *lParam* è null, viene usato l'elenco dei nomi di schema predefinito (vedere la sezione Osservazioni).</span><span class="sxs-lookup"><span data-stu-id="99ec6-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="99ec6-128">In alternativa, *lParam* può puntare a una stringa con terminazione null costituita da un massimo di 50 nomi di schema con terminazione dei due punti che sostituiscono l'elenco dei nomi di schema predefiniti.</span><span class="sxs-lookup"><span data-stu-id="99ec6-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="99ec6-129">Ad esempio, la stringa può essere "News: http: FTP: Telnet:".</span><span class="sxs-lookup"><span data-stu-id="99ec6-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="99ec6-130">La sintassi del nome dello schema è definita nel sito Web dell' [URI (Uniform Resource Identifier): documento di sintassi generico]( https://www.ietf.org/rfc/rfc2396.txt) nel sito Web IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="99ec6-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="99ec6-131">In particolare, un nome di schema può contenere un massimo di 13 caratteri (inclusi i due punti), deve iniziare con un carattere alfabetico ASCII e può essere seguito da una combinazione di alphabetics ASCII, cifre e tre caratteri di punteggiatura: ".", "+" e "-".</span><span class="sxs-lookup"><span data-stu-id="99ec6-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="99ec6-132">Il tipo stringa può essere **char \** _ o _*WCHAR \*\*_. il controllo Rich Edit rileva automaticamente il tipo.</span><span class="sxs-lookup"><span data-stu-id="99ec6-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99ec6-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99ec6-133">Return value</span></span>

<span data-ttu-id="99ec6-134">Se il messaggio ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="99ec6-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="99ec6-135">Se il messaggio ha esito negativo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="99ec6-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="99ec6-136">Ad esempio, il messaggio potrebbe non riuscire a causa di memoria insufficiente, un'opzione di rilevamento non valida o una stringa del nome di schema non valida.</span><span class="sxs-lookup"><span data-stu-id="99ec6-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="99ec6-137">Se _lParam \* contiene più di 50 nomi di schema, il messaggio ha esito negativo con un valore restituito di **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="99ec6-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ec6-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="99ec6-138">Remarks</span></span>

<span data-ttu-id="99ec6-139">Se il rilevamento automatico degli URL è abilitato, ovvero *wParam* include **AURL \_ ENABLEURL**, il controllo Rich Edit esegue l'analisi di qualsiasi testo modificato per determinare se il testo corrisponde al formato di un URL o, più in generale, in Windows 8 o versioni successive, un identificatore di risorsa internazionale IRI.</span><span class="sxs-lookup"><span data-stu-id="99ec6-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="99ec6-140">Se *lParam* è null, il controllo rileva gli URL che iniziano con i nomi di schema seguenti:</span><span class="sxs-lookup"><span data-stu-id="99ec6-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="99ec6-141">callto</span><span class="sxs-lookup"><span data-stu-id="99ec6-141">callto</span></span>
-   <span data-ttu-id="99ec6-142">file</span><span class="sxs-lookup"><span data-stu-id="99ec6-142">file</span></span>
-   <span data-ttu-id="99ec6-143">ftp</span><span class="sxs-lookup"><span data-stu-id="99ec6-143">ftp</span></span>
-   <span data-ttu-id="99ec6-144">gopher</span><span class="sxs-lookup"><span data-stu-id="99ec6-144">gopher</span></span>
-   <span data-ttu-id="99ec6-145">http</span><span class="sxs-lookup"><span data-stu-id="99ec6-145">http</span></span>
-   <span data-ttu-id="99ec6-146">https</span><span class="sxs-lookup"><span data-stu-id="99ec6-146">https</span></span>
-   <span data-ttu-id="99ec6-147">mailto</span><span class="sxs-lookup"><span data-stu-id="99ec6-147">mailto</span></span>
-   <span data-ttu-id="99ec6-148">news</span><span class="sxs-lookup"><span data-stu-id="99ec6-148">news</span></span>
-   <span data-ttu-id="99ec6-149">di HDInsight</span><span class="sxs-lookup"><span data-stu-id="99ec6-149">notes</span></span>
-   <span data-ttu-id="99ec6-150">NNTP</span><span class="sxs-lookup"><span data-stu-id="99ec6-150">nntp</span></span>
-   <span data-ttu-id="99ec6-151">onenote</span><span class="sxs-lookup"><span data-stu-id="99ec6-151">onenote</span></span>
-   <span data-ttu-id="99ec6-152">Outlook</span><span class="sxs-lookup"><span data-stu-id="99ec6-152">outlook</span></span>
-   <span data-ttu-id="99ec6-153">Prospero</span><span class="sxs-lookup"><span data-stu-id="99ec6-153">prospero</span></span>
-   <span data-ttu-id="99ec6-154">tel</span><span class="sxs-lookup"><span data-stu-id="99ec6-154">tel</span></span>
-   <span data-ttu-id="99ec6-155">telnet</span><span class="sxs-lookup"><span data-stu-id="99ec6-155">telnet</span></span>
-   <span data-ttu-id="99ec6-156">wais</span><span class="sxs-lookup"><span data-stu-id="99ec6-156">wais</span></span>
-   <span data-ttu-id="99ec6-157">webcal</span><span class="sxs-lookup"><span data-stu-id="99ec6-157">webcal</span></span>

<span data-ttu-id="99ec6-158">Quando il rilevamento automatico dei collegamenti è abilitato, il controllo Rich Edit rimuove l'effetto del **\_ collegamento CFE** dal testo modificato che non ha un formato riconosciuto dal controllo.</span><span class="sxs-lookup"><span data-stu-id="99ec6-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="99ec6-159">Se l'applicazione usa l'effetto del **\_ collegamento CFE** per contrassegnare altri tipi di testo, non abilitare il rilevamento automatico dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="99ec6-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="99ec6-160">Il controllo Rich Edit non controlla se esiste un collegamento rilevato; tale responsabilità appartiene al client.</span><span class="sxs-lookup"><span data-stu-id="99ec6-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="99ec6-161">Un controllo Rich Edit Invia la notifica di [ \_ collegamento en](en-link.md) quando riceve diversi messaggi quando il puntatore del mouse è sopra il testo con l'effetto del **\_ collegamento CFE** .</span><span class="sxs-lookup"><span data-stu-id="99ec6-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="99ec6-162">Per ulteriori informazioni, vedere [collegamenti ipertestuali automatici RichEdit](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [collegamenti ipertestuali con nome descrittivo](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span><span class="sxs-lookup"><span data-stu-id="99ec6-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="99ec6-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99ec6-163">Requirements</span></span>



| <span data-ttu-id="99ec6-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ec6-164">Requirement</span></span> | <span data-ttu-id="99ec6-165">Valore</span><span class="sxs-lookup"><span data-stu-id="99ec6-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99ec6-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99ec6-166">Minimum supported client</span></span><br/> | <span data-ttu-id="99ec6-167">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99ec6-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99ec6-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99ec6-168">Minimum supported server</span></span><br/> | <span data-ttu-id="99ec6-169">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99ec6-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99ec6-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99ec6-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="99ec6-171"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="99ec6-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ec6-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99ec6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ec6-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="99ec6-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="99ec6-174">\_collegamento en</span><span class="sxs-lookup"><span data-stu-id="99ec6-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

