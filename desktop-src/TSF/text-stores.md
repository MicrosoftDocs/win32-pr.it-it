---
title: Archivi di testo
description: Archivi di testo
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Framework servizi di testo (TSF), archivi di testo
- TSF (Framework di servizi di testo), archivi di testo
- Applicazioni abilitate per TSF, archivi di testo
- archivi di testo
- Framework servizi di testo (TSF), posizione carattere applicazione (ACP)
- TSF (Framework dei servizi di testo), posizione dei caratteri dell'applicazione (ACP)
- Applicazioni abilitate per TSF, posizione del carattere dell'applicazione (ACP)
- Posizione carattere applicazione (ACP)
- ACP (posizione carattere applicazione)
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework di servizi di testo), ancoraggi
- Applicazioni abilitate per TSF, ancoraggi
- ancoraggi
- Framework servizi di testo (TSF), blocchi di documenti
- TSF (Framework dei servizi di testo), blocchi del documento
- Applicazioni abilitate per TSF, blocchi di documenti
- blocchi del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046934"
---
# <a name="text-stores"></a><span data-ttu-id="524f6-120">Archivi di testo</span><span class="sxs-lookup"><span data-stu-id="524f6-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="524f6-121">Posizione carattere applicazione (ACP)</span><span class="sxs-lookup"><span data-stu-id="524f6-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="524f6-122">Un ACP è la posizione di un carattere o di caratteri in un flusso di testo espresso come il numero di caratteri dall'inizio del flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="524f6-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="524f6-123">Poiché il modello ACP è in base zero, il primo carattere di un flusso di testo ha un ACP pari a zero.</span><span class="sxs-lookup"><span data-stu-id="524f6-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="524f6-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="524f6-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="524f6-125">Un archivio di testo implementa un oggetto che supporta l'interfaccia [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , che consente di esprimere il flusso di testo in un ACP.</span><span class="sxs-lookup"><span data-stu-id="524f6-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="524f6-126">I metodi dell'interfaccia **ITextStoreACP** utilizzano l'intervallo ACP del flusso di testo per modificare il testo.</span><span class="sxs-lookup"><span data-stu-id="524f6-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="524f6-127">Applicazioni Anchor-Based</span><span class="sxs-lookup"><span data-stu-id="524f6-127">Anchor-Based Applications</span></span>

<span data-ttu-id="524f6-128">Il gestore utilizza i metodi basati su ACP in modo nativo per modificare il testo.</span><span class="sxs-lookup"><span data-stu-id="524f6-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="524f6-129">Tuttavia, un approccio basato su ancoraggio è disponibile per i client [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) che supportano [ancoraggi](ranges.md), in cui il Manager usa i metodi [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) per eseguire il wrapping dei metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .</span><span class="sxs-lookup"><span data-stu-id="524f6-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="524f6-130">Controllo di accesso ai documenti</span><span class="sxs-lookup"><span data-stu-id="524f6-130">Document Access Control</span></span>

<span data-ttu-id="524f6-131">L'archivio di testo controlla l'accesso al flusso di testo utilizzando i [blocchi del documento](document-locks.md).</span><span class="sxs-lookup"><span data-stu-id="524f6-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="524f6-132">Per leggere o modificare l'archivio di testo, il Manager deve innanzitutto installare un sink di notifica che supporta l'interfaccia [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) chiamando il metodo [ITextStoreACP:: adviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) e passando un puntatore a un sink di notifica.</span><span class="sxs-lookup"><span data-stu-id="524f6-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="524f6-133">Il sink di notifica consente al gestore di ottenere un blocco di documento nell'archivio di testo e ricevere notifiche quando l'archivio di testo viene modificato da un elemento diverso dal gestore, ad esempio l'input dell'utente tramite l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="524f6-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="524f6-134">I sink di notifica sono descritti più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="524f6-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="524f6-135">Come inizializzare l'archivio di testo</span><span class="sxs-lookup"><span data-stu-id="524f6-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="524f6-136">Un'applicazione Inizializza un archivio di testo completando i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="524f6-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="524f6-137">Creare un oggetto gestore thread basato sull'interfaccia [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) chiamando la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un puntatore a un oggetto gestore thread.</span><span class="sxs-lookup"><span data-stu-id="524f6-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="524f6-138">Di seguito è riportato un esempio di codice relativo all'implementazione di un oggetto gestore thread.</span><span class="sxs-lookup"><span data-stu-id="524f6-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="524f6-139">Attivare l'oggetto gestore thread chiamando il metodo [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) .</span><span class="sxs-lookup"><span data-stu-id="524f6-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="524f6-140">Questo metodo fornisce un puntatore a un [identificatore client](tfclientid.md) utilizzato per creare un oggetto di contesto.</span><span class="sxs-lookup"><span data-stu-id="524f6-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="524f6-141">Gestione thread viene utilizzato per implementare un oggetto di gestione documenti.</span><span class="sxs-lookup"><span data-stu-id="524f6-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="524f6-142">Creare un oggetto di gestione documenti basato sull'interfaccia [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) chiamando il metodo [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) con un puntatore all'oggetto gestione documenti.</span><span class="sxs-lookup"><span data-stu-id="524f6-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="524f6-143">L'oggetto gestione documenti viene utilizzato per implementare un oggetto di contesto che rappresenta l'archivio di testo.</span><span class="sxs-lookup"><span data-stu-id="524f6-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="524f6-144">Creare un oggetto di contesto da gestione documenti chiamando il metodo [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) con il puntatore all'oggetto archivio di testo e un puntatore all'identificatore client dall'attivazione di gestione thread.</span><span class="sxs-lookup"><span data-stu-id="524f6-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="524f6-145">Di seguito è riportato un esempio di creazione di un oggetto di contesto:</span><span class="sxs-lookup"><span data-stu-id="524f6-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="524f6-146">Eseguire il push dell'oggetto context nello stack con il metodo [ITfDocumentMgr::P USH](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) .</span><span class="sxs-lookup"><span data-stu-id="524f6-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="524f6-147">Di seguito è riportato un esempio di push dell'oggetto context nello stack:</span><span class="sxs-lookup"><span data-stu-id="524f6-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="524f6-148">Come modificare l'archivio di testo</span><span class="sxs-lookup"><span data-stu-id="524f6-148">How To Modify the Text Store</span></span>

<span data-ttu-id="524f6-149">Il metodo **ITfDocumentMgr::P USH** chiama **ITextStoreACP:: adviseSink** con un puntatore all'interfaccia di sink Advise per installare un nuovo sink di notifica o modificare un sink di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="524f6-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="524f6-150">Il sink di notifica riceve notifiche quando l'archivio di testo viene modificato da un elemento diverso dal gestore, ad esempio l'input dell'utente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="524f6-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="524f6-151">Le applicazioni devono chiamare il metodo [ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) quando il metodo di input ottiene lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="524f6-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="524f6-152">Altre notifiche per gestione thread vengono fornite chiamando i metodi di interfaccia **ITextStoreACPSink** appropriati.</span><span class="sxs-lookup"><span data-stu-id="524f6-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="524f6-153">Tuttavia, le applicazioni non devono chiamare i metodi dell'interfaccia **ITextStoreACPSink** in risposta ai metodi dell'interfaccia **ITextStoreACP** .</span><span class="sxs-lookup"><span data-stu-id="524f6-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="524f6-154">Le applicazioni devono chiamare solo i metodi dell'interfaccia **ITextStoreACPSink** quando l'archivio di testo viene modificato da un elemento diverso dal gestore.</span><span class="sxs-lookup"><span data-stu-id="524f6-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="524f6-155">Il contenuto dell'archivio di testo può essere modificato con uno stato di input temporaneo denominato [composizione](compositions.md).</span><span class="sxs-lookup"><span data-stu-id="524f6-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="524f6-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="524f6-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="524f6-157">Ancoraggi</span><span class="sxs-lookup"><span data-stu-id="524f6-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="524f6-158">Composizioni</span><span class="sxs-lookup"><span data-stu-id="524f6-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="524f6-159">Blocchi del documento</span><span class="sxs-lookup"><span data-stu-id="524f6-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="524f6-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="524f6-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="524f6-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="524f6-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="524f6-162">ITextStoreAnchor</span><span class="sxs-lookup"><span data-stu-id="524f6-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="524f6-163">ITextStoreAnchorSink</span><span class="sxs-lookup"><span data-stu-id="524f6-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="524f6-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="524f6-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="524f6-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="524f6-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="524f6-166">ITfThreadMgrEventSink:: OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="524f6-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="524f6-167">TfClientId</span><span class="sxs-lookup"><span data-stu-id="524f6-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="524f6-168">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="524f6-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 