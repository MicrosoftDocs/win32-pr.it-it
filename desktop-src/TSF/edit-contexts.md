---
title: Modificare i contesti
description: Modificare i contesti
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Framework servizi di testo (TSF), modifica contesti
- TSF (Framework dei servizi di testo), modificare i contesti
- Servizi di testo, modifica di contesti
- Applicazioni abilitate per TSF, modifica di contesti
- modificare i contesti
- Framework servizi di testo (TSF), modifica cookie
- TSF (Framework servizi di testo), modifica cookie
- Servizi di testo, modifica cookie
- Applicazioni abilitate per TSF, modifica cookie
- modifica cookie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855942"
---
# <a name="edit-contexts"></a><span data-ttu-id="48ff8-113">Modificare i contesti</span><span class="sxs-lookup"><span data-stu-id="48ff8-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="48ff8-114">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="48ff8-114">Applications</span></span>

<span data-ttu-id="48ff8-115">Per creare un contesto di modifica, un'applicazione chiama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="48ff8-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="48ff8-116">Servizi di testo</span><span class="sxs-lookup"><span data-stu-id="48ff8-116">Text Services</span></span>

<span data-ttu-id="48ff8-117">Un servizio di testo usa spesso il contesto di modifica attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="48ff8-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="48ff8-118">Il contesto di modifica attualmente attivo è il contesto di modifica nella parte superiore dello stack di gestione documenti attivi.</span><span class="sxs-lookup"><span data-stu-id="48ff8-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="48ff8-119">Per ottenere il contesto attualmente attivo, un servizio di testo chiama [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) per ottenere il gestore dei documenti attivi e quindi chiama [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) per ottenere il contesto di modifica all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="48ff8-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="48ff8-120">In alcuni casi, un servizio di testo richiede un proprio contesto di modifica.</span><span class="sxs-lookup"><span data-stu-id="48ff8-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="48ff8-121">Per creare un contesto di modifica, un servizio di testo chiama **ITfDocumentMgr:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="48ff8-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="48ff8-122">Modifica cookie</span><span class="sxs-lookup"><span data-stu-id="48ff8-122">Edit Cookies</span></span>

<span data-ttu-id="48ff8-123">Molti metodi, ad esempio [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), richiedono un modo per identificare un contesto di modifica con [blocco del documento](document-locks.md)di sola lettura o di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="48ff8-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="48ff8-124">Un blocco del documento viene ottenuto tramite una negoziazione tra gestione TSF e l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48ff8-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="48ff8-125">Un servizio di testo non è in grado di eseguire direttamente questa negoziazione.</span><span class="sxs-lookup"><span data-stu-id="48ff8-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="48ff8-126">Un servizio di testo può ottenere un blocco solo richiedendo una [sessione di modifica](edit-sessions.md) con un contesto specifico e accesso in sola lettura o in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="48ff8-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="48ff8-127">Quando viene concessa la sessione di modifica, il servizio di testo viene fornito con un *cookie di modifica* che identifica il contesto di modifica con l'accesso richiesto.</span><span class="sxs-lookup"><span data-stu-id="48ff8-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="48ff8-128">Questo cookie viene quindi passato al metodo per identificare il contesto di modifica con l'accesso appropriato.</span><span class="sxs-lookup"><span data-stu-id="48ff8-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="48ff8-129">**ITfDocumentMgr:: CreateContext** fornisce anche un cookie di modifica all'autore del contesto.</span><span class="sxs-lookup"><span data-stu-id="48ff8-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="48ff8-130">Questo cookie ha accesso in sola lettura e non è possibile modificare il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="48ff8-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="48ff8-131">In realtà, il gestore di TSF non negozia un blocco del documento per questo cookie di modifica.</span><span class="sxs-lookup"><span data-stu-id="48ff8-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="48ff8-132">Il cookie è contrassegnato internamente come di sola lettura, ma il documento non è effettivamente bloccato.</span><span class="sxs-lookup"><span data-stu-id="48ff8-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="48ff8-133">Se, ad esempio, l'autore del contesto chiama [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) con il cookie di modifica restituito da **ITfDocumentMgr:: CreateContext** , si ottiene la chiamata a [ITextStoreACP:: getselectation](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) o [ITextStoreAnchor:: getselect](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48ff8-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="48ff8-134">Prima di ottenere la selezione, l'applicazione determinerà se è presente un blocco del documento.</span><span class="sxs-lookup"><span data-stu-id="48ff8-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="48ff8-135">Poiché non esiste alcun blocco, l'applicazione avrà esito negativo con TS \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="48ff8-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="48ff8-136">Ovvero, se un'applicazione chiama un metodo con questo cookie che comporta la chiamata di uno dei metodi dell'archivio di testo dell'applicazione, deve gestire questo caso internamente perché l'applicazione non avrà effettivamente un blocco del documento.</span><span class="sxs-lookup"><span data-stu-id="48ff8-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="48ff8-137">Se il creatore del contesto richiede un cookie di modifica con accesso in lettura/scrittura, deve stabilire una propria sessione di modifica.</span><span class="sxs-lookup"><span data-stu-id="48ff8-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48ff8-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48ff8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48ff8-139">ITfContext</span><span class="sxs-lookup"><span data-stu-id="48ff8-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="48ff8-140">ITfDocumentMgr:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="48ff8-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="48ff8-141">ITfThreadMgr:: GetFocus</span><span class="sxs-lookup"><span data-stu-id="48ff8-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="48ff8-142">ITfDocumentMgr:: GetTop</span><span class="sxs-lookup"><span data-stu-id="48ff8-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="48ff8-143">ITfRange:: SetText</span><span class="sxs-lookup"><span data-stu-id="48ff8-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="48ff8-144">Blocchi del documento</span><span class="sxs-lookup"><span data-stu-id="48ff8-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="48ff8-145">Sessioni di modifica</span><span class="sxs-lookup"><span data-stu-id="48ff8-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="48ff8-146">ITfContext:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="48ff8-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="48ff8-147">ITextStoreACP:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="48ff8-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="48ff8-148">ITextStoreAnchor:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="48ff8-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




