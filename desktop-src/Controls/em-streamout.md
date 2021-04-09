---
title: Messaggio di EM_STREAMOUT (RichEdit. h)
description: Fa in modo che un controllo Rich Edit passi il contenuto a un'applicazione \ 8211; definita funzione di callback EditStreamCallback. La funzione di callback può quindi scrivere il flusso di dati in un file o in qualsiasi altra posizione scelta.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Controlli di Windows Message EM_STREAMOUT
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964261"
---
# <a name="em_streamout-message"></a><span data-ttu-id="4613a-105">\_Messaggio di streaming em</span><span class="sxs-lookup"><span data-stu-id="4613a-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="4613a-106">Causa il passaggio del contenuto di un controllo Rich Edit a una funzione di callback [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4613a-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="4613a-107">La funzione di callback può quindi scrivere il flusso di dati in un file o in qualsiasi altra posizione scelta.</span><span class="sxs-lookup"><span data-stu-id="4613a-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="4613a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4613a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4613a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4613a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4613a-110">Specifica il formato dei dati e le opzioni di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="4613a-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="4613a-111">Questo valore deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4613a-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="4613a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="4613a-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="4613a-113">Significato</span><span class="sxs-lookup"><span data-stu-id="4613a-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="4613a-114"><dt>**RTF per SF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="4613a-115">RTF.</span><span class="sxs-lookup"><span data-stu-id="4613a-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="4613a-116"><dt>**\_RTFNOOBJS SF**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="4613a-117">RTF con spazi al posto degli oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="4613a-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="4613a-118"><dt>**\_testo SF**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="4613a-119">Testo con spazi al posto degli oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="4613a-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="4613a-120"><dt>**SF con \_ testo**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="4613a-121">Testo con rappresentazione testuale di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="4613a-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="4613a-122">L'opzione **SF \_ RTFNOOBJS** è utile se un'applicazione archivia oggetti com, perché la rappresentazione RTF degli oggetti com non è molto compatta.</span><span class="sxs-lookup"><span data-stu-id="4613a-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="4613a-123">Il controllo Word, \\ objattph, seguito da uno spazio indica la posizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4613a-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="4613a-124">Inoltre, è possibile specificare i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="4613a-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="4613a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4613a-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="4613a-126">Significato</span><span class="sxs-lookup"><span data-stu-id="4613a-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="4613a-127"><dt>**\_PLAINRTF SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="4613a-128">Se specificato, il controllo Rich Edit trasmette solo le parole chiave comuni a tutti i linguaggi, ignorando le parole chiave specifiche della lingua.</span><span class="sxs-lookup"><span data-stu-id="4613a-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="4613a-129">Se non è specificato, il controllo Rich Edit trasmette tutte le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="4613a-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="4613a-130">È possibile combinare questo flag con il contrassegno **SF \_ RTF** o **SF \_ RTFNOOBJS** .</span><span class="sxs-lookup"><span data-stu-id="4613a-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="4613a-131"><dt>**\_selezione SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="4613a-132">Se specificato, il controllo Rich Edit trasmette solo il contenuto della selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="4613a-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="4613a-133">Se non specificato, il controllo trasmette l'intero contenuto.</span><span class="sxs-lookup"><span data-stu-id="4613a-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="4613a-134">È possibile combinare questo flag con qualsiasi valore di formato dati.</span><span class="sxs-lookup"><span data-stu-id="4613a-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="4613a-135"><dt>**\_Unicode SF**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="4613a-136">**Microsoft Rich Edit 2,0 e versioni successive:** Indica il testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="4613a-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="4613a-137">È possibile combinare questo flag con il flag di **\_ testo SF** .</span><span class="sxs-lookup"><span data-stu-id="4613a-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="4613a-138"><dt>**\_USECODEPAGE SF**</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="4613a-139">**Rich Edit 3,0 e versioni successive:** Genera il formato UTF-8 RTF e il testo utilizzando altre tabelle codici.</span><span class="sxs-lookup"><span data-stu-id="4613a-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="4613a-140">La tabella codici è impostata nella parola alta di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="4613a-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="4613a-141">Ad esempio, per UTF-8 RTF, impostare *wParam* su (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| SF \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="4613a-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="4613a-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4613a-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4613a-143">Puntatore a una struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="4613a-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="4613a-144">In fase di input, il membro **pfnCallback** di questa struttura deve puntare a una funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4613a-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="4613a-145">Nell'output il membro **dwError** può contenere un codice di errore diverso da zero se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="4613a-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4613a-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4613a-146">Return value</span></span>

<span data-ttu-id="4613a-147">Questo messaggio restituisce il numero di caratteri scritti nel flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="4613a-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="4613a-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="4613a-148">Remarks</span></span>

<span data-ttu-id="4613a-149">Quando si invia un messaggio di **\_ flusso em** , il controllo Rich Edit effettua chiamate ripetute alla funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) specificata dal membro **pfnCallback** della struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="4613a-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="4613a-150">Ogni volta che chiama la funzione di callback, il controllo passa un buffer contenente una parte del contenuto del controllo.</span><span class="sxs-lookup"><span data-stu-id="4613a-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="4613a-151">Questo processo continua fino a quando il controllo non ha passato tutto il contenuto alla funzione di callback o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4613a-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="4613a-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4613a-152">Requirements</span></span>



| <span data-ttu-id="4613a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="4613a-153">Requirement</span></span> | <span data-ttu-id="4613a-154">Valore</span><span class="sxs-lookup"><span data-stu-id="4613a-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4613a-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4613a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4613a-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4613a-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4613a-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4613a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4613a-158">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4613a-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4613a-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4613a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="4613a-160"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4613a-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4613a-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4613a-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="4613a-162">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4613a-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4613a-163">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="4613a-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="4613a-164">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="4613a-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="4613a-165">**flusso EMin \_**</span><span class="sxs-lookup"><span data-stu-id="4613a-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





