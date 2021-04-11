---
title: Blocchi del documento
description: Blocchi del documento
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Framework servizi di testo (TSF), blocchi di documenti
- TSF (Framework dei servizi di testo), blocchi del documento
- Applicazioni abilitate per TSF, blocchi di documenti
- blocchi del documento
- Framework servizi di testo (TSF), posizione carattere applicazione (ACP)
- TSF (Framework dei servizi di testo), posizione dei caratteri dell'applicazione (ACP)
- Applicazioni abilitate per TSF, posizione del carattere dell'applicazione (ACP)
- Posizione carattere applicazione (ACP)
- ACP (posizione carattere applicazione)
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework di servizi di testo), ancoraggi
- Applicazioni abilitate per TSF, ancoraggi
- ancoraggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221184"
---
# <a name="document-locks"></a><span data-ttu-id="7b132-116">Blocchi del documento</span><span class="sxs-lookup"><span data-stu-id="7b132-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="7b132-117">Protocollo di blocco del documento</span><span class="sxs-lookup"><span data-stu-id="7b132-117">The Document Lock Protocol</span></span>

<span data-ttu-id="7b132-118">Per richiedere un blocco del documento per le applicazioni basate su ACP, il gestore di TSF chiama [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span><span class="sxs-lookup"><span data-stu-id="7b132-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="7b132-119">Per le applicazioni basate su ancoraggio, il gestore di TSF chiama [ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span><span class="sxs-lookup"><span data-stu-id="7b132-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="7b132-120">L'applicazione concede il blocco del documento chiamando [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (applicazioni basate su ACP) o [ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (applicazioni basate su ancoraggio) all'interno di **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="7b132-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="7b132-121">Il blocco è valido solo durante la chiamata **OnLockGranted** .</span><span class="sxs-lookup"><span data-stu-id="7b132-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="7b132-122">Quando **OnLockGranted** restituisce, il documento viene considerato sbloccato.</span><span class="sxs-lookup"><span data-stu-id="7b132-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="7b132-123">Tipi di blocchi di documenti</span><span class="sxs-lookup"><span data-stu-id="7b132-123">Types of Document Locks</span></span>

<span data-ttu-id="7b132-124">Esistono due tipi di blocchi di documento, di sola lettura e di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7b132-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="7b132-125">Un blocco di sola lettura consente al gestore di leggere il testo, ma non di modificare o inserire testo.</span><span class="sxs-lookup"><span data-stu-id="7b132-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="7b132-126">Un blocco di lettura/scrittura consente al gestore di leggere, modificare e inserire testo.</span><span class="sxs-lookup"><span data-stu-id="7b132-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="7b132-127">È necessario un blocco di sola lettura specificando TS \_ LF \_ Read in *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="7b132-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="7b132-128">È necessario un blocco di lettura/scrittura specificando TS \_ LF \_ ReadWrite in *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="7b132-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="7b132-129">Richieste asincrone e sincrone</span><span class="sxs-lookup"><span data-stu-id="7b132-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="7b132-130">Una richiesta di blocco può essere sincrona o asincrona.</span><span class="sxs-lookup"><span data-stu-id="7b132-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="7b132-131">Il gestore richiede un blocco sincrono tramite il flag di sincronizzazione di TS \_ LF \_ in *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="7b132-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="7b132-132">Se questo flag non è presente, la richiesta è asincrona.</span><span class="sxs-lookup"><span data-stu-id="7b132-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="7b132-133">Concessione del blocco</span><span class="sxs-lookup"><span data-stu-id="7b132-133">Granting the Lock</span></span>

<span data-ttu-id="7b132-134">Quando viene chiamato **RequestLock** , l'applicazione deve determinare se il documento è attualmente bloccato.</span><span class="sxs-lookup"><span data-stu-id="7b132-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="7b132-135">Se il documento non è bloccato e non esistono altri motivi per negare il blocco, l'applicazione deve impostare *phrSession* su S \_ OK e restituire s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b132-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="7b132-136">Se il documento è bloccato e la richiesta di blocco è sincrona, l'applicazione deve impostare *phrSession* su TS e \_ \_ sincrono e restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b132-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="7b132-137">Indica che non è possibile concedere una richiesta sincrona.</span><span class="sxs-lookup"><span data-stu-id="7b132-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="7b132-138">Se il documento è bloccato e la richiesta di blocco è asincrona, l'applicazione deve accodare la richiesta, impostare *phrSession* su TS \_ S \_ Async e restituire s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b132-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="7b132-139">Quando il documento diventa disponibile, l'applicazione deve rimuovere la richiesta dalla coda e chiamare **OnLockGranted**.</span><span class="sxs-lookup"><span data-stu-id="7b132-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="7b132-140">Questo Accodamento di richieste di blocco è facoltativo. esiste uno scenario che un'applicazione deve supportare.</span><span class="sxs-lookup"><span data-stu-id="7b132-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="7b132-141">Se il documento ha un blocco di sola lettura, la nuova richiesta di blocco è di lettura/scrittura e la richiesta è asincrona, l'applicazione ha chiamato in **OnLockGranted** , che ha causato una chiamata rientrante a **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="7b132-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="7b132-142">L'applicazione deve impostare *phrSession* su TS \_ s \_ Async e restituire s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b132-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="7b132-143">Dopo che la chiamata a **OnLockGranted** restituisce, l'applicazione deve elaborare la richiesta di aggiornamento chiamando di nuovo **OnLockGranted** con TS \_ LF \_ ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="7b132-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="7b132-144">Imposizione del blocco</span><span class="sxs-lookup"><span data-stu-id="7b132-144">Lock Enforcement</span></span>

<span data-ttu-id="7b132-145">Prima di consentire l'accesso al documento, l'applicazione deve verificare che sia presente il tipo di blocco appropriato.</span><span class="sxs-lookup"><span data-stu-id="7b132-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="7b132-146">Ad esempio, l'applicazione deve verificare che un documento disponga di almeno un blocco di sola lettura prima di consentire a [ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) di continuare.</span><span class="sxs-lookup"><span data-stu-id="7b132-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="7b132-147">Se il blocco appropriato non esiste, l'applicazione deve restituire TF \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="7b132-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b132-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b132-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b132-149">Archivi di testo</span><span class="sxs-lookup"><span data-stu-id="7b132-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="7b132-150">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="7b132-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="7b132-151">ITextStoreACPSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="7b132-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="7b132-152">ITextStoreACP:: GetText</span><span class="sxs-lookup"><span data-stu-id="7b132-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="7b132-153">ITextStoreAnchor:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="7b132-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="7b132-154">ITextStoreAnchorSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="7b132-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="7b132-155">ITextStoreAnchor:: GetText</span><span class="sxs-lookup"><span data-stu-id="7b132-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




