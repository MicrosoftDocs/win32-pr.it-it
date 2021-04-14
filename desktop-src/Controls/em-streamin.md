---
title: Messaggio di EM_STREAMIN (RichEdit. h)
description: Sostituisce il contenuto di un controllo Rich Edit con un flusso di dati fornito da un'applicazione definita \ 8211; Funzione di callback EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Controlli di Windows Message EM_STREAMIN
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478275"
---
# <a name="em_streamin-message"></a><span data-ttu-id="27e2a-104">\_Messaggio flusso Emin</span><span class="sxs-lookup"><span data-stu-id="27e2a-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="27e2a-105">Sostituisce il contenuto di un controllo Rich Edit con un flusso di dati fornito da una funzione di callback [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27e2a-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="27e2a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27e2a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27e2a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27e2a-108">Specifica il formato dei dati e le opzioni di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="27e2a-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="27e2a-109">Questo valore deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="27e2a-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="27e2a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="27e2a-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="27e2a-111">Significato</span><span class="sxs-lookup"><span data-stu-id="27e2a-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="27e2a-112"><dt>**RTF per SF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27e2a-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="27e2a-113">RTF</span><span class="sxs-lookup"><span data-stu-id="27e2a-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="27e2a-114"><dt>**\_testo SF**</dt></span><span class="sxs-lookup"><span data-stu-id="27e2a-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="27e2a-115">Testo</span><span class="sxs-lookup"><span data-stu-id="27e2a-115">Text</span></span><br/> |



 

<span data-ttu-id="27e2a-116">Inoltre, è possibile specificare i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="27e2a-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="27e2a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="27e2a-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="27e2a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="27e2a-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="27e2a-119"><dt>**\_PLAINRTF SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="27e2a-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="27e2a-120">Se specificato, solo le parole chiave comuni a tutti i linguaggi vengono trasmesse in.</span><span class="sxs-lookup"><span data-stu-id="27e2a-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="27e2a-121">Le parole chiave RTF specifiche del linguaggio nel flusso vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="27e2a-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="27e2a-122">Se non è specificato, tutte le parole chiave vengono trasmesse in.</span><span class="sxs-lookup"><span data-stu-id="27e2a-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="27e2a-123">È possibile combinare questo flag con il **flag \_ RTF di SF** .</span><span class="sxs-lookup"><span data-stu-id="27e2a-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="27e2a-124"><dt>**\_selezione SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="27e2a-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="27e2a-125">Se specificato, il flusso di dati sostituisce il contenuto della selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="27e2a-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="27e2a-126">Se non è specificato, il flusso di dati sostituisce l'intero contenuto del controllo.</span><span class="sxs-lookup"><span data-stu-id="27e2a-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="27e2a-127">È possibile combinare questo flag con i flag di **\_ testo SF** o **\_ RTF** .</span><span class="sxs-lookup"><span data-stu-id="27e2a-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="27e2a-128"><dt>**\_Unicode SF**</dt></span><span class="sxs-lookup"><span data-stu-id="27e2a-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="27e2a-129">**Microsoft Rich Edit 2,0 e versioni successive:** Indica il testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="27e2a-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="27e2a-130">È possibile combinare questo flag con il flag di **\_ testo SF** .</span><span class="sxs-lookup"><span data-stu-id="27e2a-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="27e2a-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27e2a-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27e2a-132">Puntatore a una struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="27e2a-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="27e2a-133">In fase di input, il membro **pfnCallback** di questa struttura deve puntare a una funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27e2a-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="27e2a-134">Nell'output il membro **dwError** può contenere un codice di errore diverso da zero se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="27e2a-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27e2a-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27e2a-135">Return value</span></span>

<span data-ttu-id="27e2a-136">Questo messaggio restituisce il numero di caratteri letti.</span><span class="sxs-lookup"><span data-stu-id="27e2a-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="27e2a-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="27e2a-137">Remarks</span></span>

<span data-ttu-id="27e2a-138">Quando si invia un **messaggio \_ flusso Emin** , il controllo Rich Edit effettua chiamate ripetute alla funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) specificata dal membro **pfnCallback** della struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="27e2a-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="27e2a-139">Ogni volta che viene chiamata la funzione di callback, riempie un buffer con i dati da leggere nel controllo.</span><span class="sxs-lookup"><span data-stu-id="27e2a-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="27e2a-140">Continua fino a quando la funzione di callback non indica che l'operazione del flusso è stata completata o si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="27e2a-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="27e2a-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27e2a-141">Requirements</span></span>



| <span data-ttu-id="27e2a-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="27e2a-142">Requirement</span></span> | <span data-ttu-id="27e2a-143">Valore</span><span class="sxs-lookup"><span data-stu-id="27e2a-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27e2a-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27e2a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="27e2a-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27e2a-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27e2a-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27e2a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="27e2a-147">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27e2a-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27e2a-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27e2a-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="27e2a-149"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27e2a-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e2a-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27e2a-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="27e2a-151">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="27e2a-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="27e2a-152">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="27e2a-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="27e2a-153">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="27e2a-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="27e2a-154">**\_flusso em**</span><span class="sxs-lookup"><span data-stu-id="27e2a-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





