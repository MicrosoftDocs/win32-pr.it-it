---
title: Raggruppamenti
description: Raggruppamenti
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Framework servizi di testo (TSF), raggruppamenti
- TSF (Text Services Framework), raggruppamenti
- Servizi di testo, raggruppamenti
- Applicazioni abilitate per TSF, raggruppamenti
- raggruppamenti
- Framework servizi di testo (TSF), tipi di raggruppamento
- TSF (Framework dei servizi di testo), tipi di raggruppamento
- Servizi di testo, tipi di raggruppamento
- Applicazioni abilitate per TSF, tipi di raggruppamento
- tipi di raggruppamento
- Framework servizi di testo (TSF), notifiche di modifica raggruppamento
- TSF (Text Services Framework), notifiche di modifica di raggruppamento
- Servizi di testo, notifiche di modifica raggruppamento
- Applicazioni abilitate per TSF, notifiche di modifica del raggruppamento
- notifiche di modifica raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221185"
---
# <a name="compartments"></a><span data-ttu-id="ac61a-118">Raggruppamenti</span><span class="sxs-lookup"><span data-stu-id="ac61a-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="ac61a-119">Tipi di raggruppamento</span><span class="sxs-lookup"><span data-stu-id="ac61a-119">Compartment Types</span></span>

<span data-ttu-id="ac61a-120">Sono disponibili diversi tipi di raggruppamenti.</span><span class="sxs-lookup"><span data-stu-id="ac61a-120">There are several different types of compartments.</span></span> <span data-ttu-id="ac61a-121">È presente un raggruppamento globale e ogni gestore di thread, gestione documenti e contesto può contenere un raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="ac61a-122">Il raggruppamento globale consente ai client di condividere i dati tra i processi.</span><span class="sxs-lookup"><span data-stu-id="ac61a-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="ac61a-123">Per ottenere il gestore di raggruppamento globale, chiamare [**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span><span class="sxs-lookup"><span data-stu-id="ac61a-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="ac61a-124">Gestione thread contiene un gestore di raggruppamento che contiene i raggruppamenti in base ai singoli thread.</span><span class="sxs-lookup"><span data-stu-id="ac61a-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="ac61a-125">In questo modo è possibile condividere i dati all'interno di un thread.</span><span class="sxs-lookup"><span data-stu-id="ac61a-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="ac61a-126">Per ottenere un gestore di raggruppamento di gestione thread, chiamare **ITfThreadMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="ac61a-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="ac61a-127">Ogni gestore di documenti creato contiene anche un gestore di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="ac61a-128">In questo modo è possibile condividere i dati all'interno di un gestore di documenti specifico.</span><span class="sxs-lookup"><span data-stu-id="ac61a-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="ac61a-129">Per ottenere il gestore di raggruppamento di gestione documenti, chiamare **ITfDocumentMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="ac61a-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="ac61a-130">Ogni contesto creato contiene anche un gestore di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="ac61a-131">In questo modo è possibile condividere i dati in un contesto specifico.</span><span class="sxs-lookup"><span data-stu-id="ac61a-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="ac61a-132">Per ottenere un gestore di raggruppamento del contesto, chiamare **ITfContext:: QueryInterface** con IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="ac61a-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="ac61a-133">Creazione ed eliminazione di un raggruppamento</span><span class="sxs-lookup"><span data-stu-id="ac61a-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="ac61a-134">Viene creato un raggruppamento la prima volta che [**ITfCompartmentMgr:: Compartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) viene chiamato con il GUID di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="ac61a-135">Il client di installazione deve impostare il valore iniziale del raggruppamento usando [**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span><span class="sxs-lookup"><span data-stu-id="ac61a-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="ac61a-136">Fino a quando non viene impostato un valore, il valore del raggruppamento è vuoto.</span><span class="sxs-lookup"><span data-stu-id="ac61a-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="ac61a-137">Per questo motivo, non esiste alcun modo per verificare che il raggruppamento esista prima della chiamata a **Compartment** .</span><span class="sxs-lookup"><span data-stu-id="ac61a-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="ac61a-138">Per evitare questa situazione, il client di installazione deve impostare il valore su un valore iniziale, in modo che gli altri client possano determinare se il raggruppamento esiste già.</span><span class="sxs-lookup"><span data-stu-id="ac61a-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="ac61a-139">Il metodo [**ITfCompartmentMgr:: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) viene usato per rimuovere un raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="ac61a-140">Eventuali riferimenti esistenti al raggruppamento sono contrassegnati come non validi.</span><span class="sxs-lookup"><span data-stu-id="ac61a-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="ac61a-141">Recupero di raggruppamenti</span><span class="sxs-lookup"><span data-stu-id="ac61a-141">Obtaining Compartments</span></span>

<span data-ttu-id="ac61a-142">Usando l'interfaccia [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , un client può enumerare i raggruppamenti chiamando [**ITfCompartmentMgr:: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span><span class="sxs-lookup"><span data-stu-id="ac61a-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="ac61a-143">Questo metodo fornisce un oggetto **IEnumGUID** che contiene i GUID di tutti i raggruppamenti installati.</span><span class="sxs-lookup"><span data-stu-id="ac61a-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="ac61a-144">Usando il GUID di raggruppamento, **ITfCompartmentMgr:: Compartment** viene usato per ottenere un raggruppamento specifico.</span><span class="sxs-lookup"><span data-stu-id="ac61a-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="ac61a-145">Questo metodo fornisce al chiamante un oggetto [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) che può ottenere e impostare i dati del raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="ac61a-146">Ricezione delle notifiche di modifica del raggruppamento</span><span class="sxs-lookup"><span data-stu-id="ac61a-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="ac61a-147">Quando viene modificato il valore di un raggruppamento, il gestore di TSF invia una notifica ai sink di avviso installati che il raggruppamento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="ac61a-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="ac61a-148">Per installare un sink di notifica della modifica del raggruppamento, creare un oggetto che implementi [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span><span class="sxs-lookup"><span data-stu-id="ac61a-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="ac61a-149">Quindi, chiamare **ITfCompartment:: QueryInterface** con IID \_ ITfSource sull'oggetto Compartment da monitorare per ottenere un'interfaccia [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) .</span><span class="sxs-lookup"><span data-stu-id="ac61a-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="ac61a-150">A questo punto, chiamare [**ITfSource:: adviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfCompartmentEventSink e il puntatore all'oggetto **ITfCompartmentEventSink** .</span><span class="sxs-lookup"><span data-stu-id="ac61a-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="ac61a-151">Quando viene modificato il valore del raggruppamento, il sink di notifica [**ITfCompartmentEventSink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) viene chiamato con il GUID del raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ac61a-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="ac61a-152">Il sink di notifica può chiamare [**ITfCompartment:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) per ottenere il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="ac61a-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac61a-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac61a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac61a-154">**ITfCompartmentMgr**</span><span class="sxs-lookup"><span data-stu-id="ac61a-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="ac61a-155">**ITfCompartment**</span><span class="sxs-lookup"><span data-stu-id="ac61a-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="ac61a-156">**ITfCompartmentEventSink**</span><span class="sxs-lookup"><span data-stu-id="ac61a-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="ac61a-157">**TfClientId**</span><span class="sxs-lookup"><span data-stu-id="ac61a-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="ac61a-158">**ITfThreadMgr:: GetGlobalCompartment**</span><span class="sxs-lookup"><span data-stu-id="ac61a-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="ac61a-159">**ITfCompartmentMgr:: Compartment**</span><span class="sxs-lookup"><span data-stu-id="ac61a-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="ac61a-160">**ITfCompartment:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="ac61a-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="ac61a-161">**ITfCompartmentMgr::ClearCompartment**</span><span class="sxs-lookup"><span data-stu-id="ac61a-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="ac61a-162">**ITfCompartmentMgr::EnumCompartments**</span><span class="sxs-lookup"><span data-stu-id="ac61a-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="ac61a-163">**ITfSource**</span><span class="sxs-lookup"><span data-stu-id="ac61a-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="ac61a-164">**ITfSource:: AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="ac61a-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="ac61a-165">**ITfCompartmentEventSink:: OnChange**</span><span class="sxs-lookup"><span data-stu-id="ac61a-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




