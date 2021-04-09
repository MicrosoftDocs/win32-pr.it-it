---
title: Messaggio di EM_SETTEXTMODE (RichEdit. h)
description: Imposta la modalità testo o il livello di annullamento di un controllo Rich Edit. Il messaggio ha esito negativo se il controllo contiene testo.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Controlli di Windows Message EM_SETTEXTMODE
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964387"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="f48b9-105">\_Messaggio SETTEXTMODE em</span><span class="sxs-lookup"><span data-stu-id="f48b9-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="f48b9-106">Imposta la modalità testo o il livello di annullamento di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f48b9-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="f48b9-107">Il messaggio ha esito negativo se il controllo contiene testo.</span><span class="sxs-lookup"><span data-stu-id="f48b9-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="f48b9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f48b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f48b9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f48b9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f48b9-110">Uno o più valori del tipo di enumerazione [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="f48b9-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="f48b9-111">I valori specificano le nuove impostazioni per la modalità testo del controllo e i parametri del livello di annullamento.</span><span class="sxs-lookup"><span data-stu-id="f48b9-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="f48b9-112">Specificare uno dei valori seguenti per impostare il parametro della modalità testo.</span><span class="sxs-lookup"><span data-stu-id="f48b9-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="f48b9-113">Se non si specifica un valore in modalità testo, la modalità testo rimane in corrispondenza dell'impostazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f48b9-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="f48b9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f48b9-114">Value</span></span>                                          | <span data-ttu-id="f48b9-115">Significato</span><span class="sxs-lookup"><span data-stu-id="f48b9-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f48b9-116">**\_testo normale TM**</span><span class="sxs-lookup"><span data-stu-id="f48b9-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="f48b9-117">Indica la modalità testo normale, in cui il controllo è simile a un controllo di modifica standard.</span><span class="sxs-lookup"><span data-stu-id="f48b9-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="f48b9-118">Per ulteriori informazioni sulla modalità testo normale, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="f48b9-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="f48b9-119">**TM \_ RichText**</span><span class="sxs-lookup"><span data-stu-id="f48b9-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="f48b9-120">Indica la modalità RTF, in cui il controllo ha una funzionalità di modifica avanzata standard.</span><span class="sxs-lookup"><span data-stu-id="f48b9-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="f48b9-121">La modalità RTF è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f48b9-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="f48b9-122">Specificare uno dei valori seguenti per impostare il parametro del livello di annullamento.</span><span class="sxs-lookup"><span data-stu-id="f48b9-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="f48b9-123">Se non si specifica un valore del livello di annullamento, il livello di annullamento rimane in corrispondenza dell'impostazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f48b9-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="f48b9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f48b9-124">Value</span></span>                                                      | <span data-ttu-id="f48b9-125">Significato</span><span class="sxs-lookup"><span data-stu-id="f48b9-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f48b9-126">**TM \_ SINGLELEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="f48b9-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="f48b9-127">Il controllo consente all'utente di annullare solo l'ultima azione che può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="f48b9-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="f48b9-128">**TM \_ MULTILEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="f48b9-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="f48b9-129">Il controllo supporta più operazioni di annullamento.</span><span class="sxs-lookup"><span data-stu-id="f48b9-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="f48b9-130">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f48b9-130">This is the default setting.</span></span> <span data-ttu-id="f48b9-131">Usare il [**messaggio \_ SETUNDOLIMIT em**](em-setundolimit.md) per impostare il numero massimo di azioni di annullamento.</span><span class="sxs-lookup"><span data-stu-id="f48b9-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="f48b9-132">Specificare uno dei valori seguenti per impostare il parametro della tabella codici.</span><span class="sxs-lookup"><span data-stu-id="f48b9-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="f48b9-133">Se non si specifica un valore della tabella codici, la tabella codici rimane in corrispondenza dell'impostazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f48b9-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="f48b9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f48b9-134">Value</span></span>                                                    | <span data-ttu-id="f48b9-135">Significato</span><span class="sxs-lookup"><span data-stu-id="f48b9-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f48b9-136">**TM \_ SINGLECODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="f48b9-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="f48b9-137">Il controllo consente solo la tastiera inglese e una tastiera corrispondente al set di caratteri predefinito.</span><span class="sxs-lookup"><span data-stu-id="f48b9-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="f48b9-138">Ad esempio, è possibile avere il greco e l'inglese.</span><span class="sxs-lookup"><span data-stu-id="f48b9-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="f48b9-139">Si noti che in questo modo si impedisce al testo Unicode di immettere il controllo.</span><span class="sxs-lookup"><span data-stu-id="f48b9-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="f48b9-140">Usare, ad esempio, questo valore se un controllo Rich Edit deve essere limitato al testo ANSI.</span><span class="sxs-lookup"><span data-stu-id="f48b9-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="f48b9-141">**TM \_ MULTICODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="f48b9-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="f48b9-142">Il controllo consente di accedere a più tabelle codici e testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="f48b9-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="f48b9-143">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f48b9-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="f48b9-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f48b9-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f48b9-145">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f48b9-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f48b9-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f48b9-146">Return value</span></span>

<span data-ttu-id="f48b9-147">Se il messaggio ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="f48b9-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="f48b9-148">Se il messaggio ha esito negativo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f48b9-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f48b9-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="f48b9-149">Remarks</span></span>

<span data-ttu-id="f48b9-150">In modalità RTF, un controllo Rich Edit ha una funzionalità di modifica avanzata standard.</span><span class="sxs-lookup"><span data-stu-id="f48b9-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="f48b9-151">Tuttavia, in modalità testo normale, il controllo è simile a un controllo di modifica standard:</span><span class="sxs-lookup"><span data-stu-id="f48b9-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="f48b9-152">Il testo in un controllo testo normale può avere un solo formato, ad esempio grassetto, 10pt Arial.</span><span class="sxs-lookup"><span data-stu-id="f48b9-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="f48b9-153">L'utente non può incollare formati RTF, ad esempio Rich Text Format (RTF) o oggetti incorporati in un controllo testo normale.</span><span class="sxs-lookup"><span data-stu-id="f48b9-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="f48b9-154">Per formattare i paragrafi, i controlli della modalità RTF hanno sempre un indicatore di fine del documento predefinito o un ritorno a capo.</span><span class="sxs-lookup"><span data-stu-id="f48b9-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="f48b9-155">I controlli di testo normale, d'altra parte, non necessitano del marcatore di fine del documento predefinito, pertanto viene omesso.</span><span class="sxs-lookup"><span data-stu-id="f48b9-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="f48b9-156">Il controllo non deve contenere testo quando riceve il messaggio **\_ SETTEXTMODE em** .</span><span class="sxs-lookup"><span data-stu-id="f48b9-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="f48b9-157">Per assicurarsi che non esistano testo, inviare un messaggio di [**\_ testo WM**](/windows/desktop/winmsg/wm-settext) con una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="f48b9-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="f48b9-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f48b9-158">Requirements</span></span>



| <span data-ttu-id="f48b9-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f48b9-159">Requirement</span></span> | <span data-ttu-id="f48b9-160">Valore</span><span class="sxs-lookup"><span data-stu-id="f48b9-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f48b9-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f48b9-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f48b9-162">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f48b9-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f48b9-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f48b9-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f48b9-164">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f48b9-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f48b9-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f48b9-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="f48b9-166"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f48b9-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f48b9-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f48b9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48b9-168">**\_GETTEXTMODE em**</span><span class="sxs-lookup"><span data-stu-id="f48b9-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="f48b9-169">**\_SETUNDOLIMIT em**</span><span class="sxs-lookup"><span data-stu-id="f48b9-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="f48b9-170">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="f48b9-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="f48b9-171">**\_testo WM**</span><span class="sxs-lookup"><span data-stu-id="f48b9-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

