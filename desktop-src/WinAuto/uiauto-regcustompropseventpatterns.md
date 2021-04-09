---
title: Registrare proprietà, eventi e pattern di controllo personalizzati
description: Prima di poter usare una proprietà personalizzata, un evento o un pattern di controllo, sia il provider che il client devono registrare la proprietà, l'evento o il pattern di controllo in fase di esecuzione.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Automazione interfaccia utente, proprietà personalizzate
- Automazione interfaccia utente, panoramica degli eventi
- Automazione interfaccia utente, Cenni preliminari sui pattern di controllo
- Automazione interfaccia utente, registrazione di proprietà personalizzate
- Automazione interfaccia utente, registrazione di eventi
- Automazione interfaccia utente, registrazione di pattern di controllo
- Proprietà personalizzate, registrazione
- eventi, registrazione
- pattern di controllo, registrazione
- registrazione, proprietà personalizzate
- registrazione, eventi
- registrazione, pattern di controllo
- pattern di controllo, personalizzati
- pattern di controllo, implementazione personalizzata
- implementazione di pattern di controllo personalizzati
- pattern di controllo personalizzati
- wrapper client
- gestori di modelli
- implementazione di gestori di modelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047184"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="f8823-122">Registrare proprietà, eventi e pattern di controllo personalizzati</span><span class="sxs-lookup"><span data-stu-id="f8823-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="f8823-123">Prima di poter usare una proprietà personalizzata, un evento o un pattern di controllo, sia il provider che il client devono registrare la proprietà, l'evento o il pattern di controllo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f8823-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="f8823-124">La registrazione è efficace a livello globale all'interno di un processo dell'applicazione e rimane effettiva fino alla chiusura del processo o all'ultima rilasciata all'interno del processo l'ultimo oggetto dell'elemento di automazione interfaccia utente Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) o [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)).</span><span class="sxs-lookup"><span data-stu-id="f8823-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="f8823-125">Per la registrazione è necessario passare un GUID all'automazione interfaccia utente, insieme a informazioni dettagliate sulla proprietà personalizzata, sull'evento o sul pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="f8823-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="f8823-126">Il tentativo di registrare lo stesso GUID una seconda volta con le stesse informazioni avrà esito positivo, ma il tentativo di registrare lo stesso GUID una seconda volta ma con informazioni diverse, ad esempio una proprietà personalizzata di un tipo diverso, avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f8823-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="f8823-127">In futuro, se la specifica personalizzata viene accettata e integrata nel core di automazione interfaccia utente, l'automazione dell'interfaccia utente convaliderà le informazioni di registrazione personalizzate e utilizzerà il codice già registrato anziché l'implementazione del Framework "ufficiale", riducendo al minimo i problemi di compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f8823-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="f8823-128">Non è possibile rimuovere proprietà, eventi o pattern di controllo che sono già registrati.</span><span class="sxs-lookup"><span data-stu-id="f8823-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="f8823-129">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8823-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f8823-130">Registrazione di proprietà ed eventi personalizzati</span><span class="sxs-lookup"><span data-stu-id="f8823-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="f8823-131">Implementazione di pattern di controllo personalizzati</span><span class="sxs-lookup"><span data-stu-id="f8823-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="f8823-132">Il wrapper client e il gestore pattern</span><span class="sxs-lookup"><span data-stu-id="f8823-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="f8823-133">Implementazione del wrapper client</span><span class="sxs-lookup"><span data-stu-id="f8823-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="f8823-134">Implementazione del gestore pattern</span><span class="sxs-lookup"><span data-stu-id="f8823-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="f8823-135">Registrazione di un pattern di controllo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f8823-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="f8823-136">Implementazione di esempio di un pattern di controllo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f8823-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="f8823-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8823-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="f8823-138">Registrazione di proprietà ed eventi personalizzati</span><span class="sxs-lookup"><span data-stu-id="f8823-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="f8823-139">La registrazione di un evento o di una proprietà personalizzata consente al provider e al client di ottenere un ID per la proprietà o l'evento, che può quindi essere passato a vari metodi API che accettano gli ID come parametri.</span><span class="sxs-lookup"><span data-stu-id="f8823-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="f8823-140">Per registrare una proprietà o un evento:</span><span class="sxs-lookup"><span data-stu-id="f8823-140">To register a property or event:</span></span>

1.  <span data-ttu-id="f8823-141">Definire un GUID per la proprietà o l'evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="f8823-142">Compilare una struttura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) con le informazioni sulla proprietà o sull'evento, inclusi il GUID e una stringa non localizzabile che contiene il nome della proprietà o dell'evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="f8823-143">Per le proprietà personalizzate è inoltre necessario specificare il tipo di dati della proprietà, ad esempio se la proprietà include un Integer o una stringa.</span><span class="sxs-lookup"><span data-stu-id="f8823-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="f8823-144">Il tipo di dati deve essere uno dei seguenti tipi specificati dall'enumerazione [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) .</span><span class="sxs-lookup"><span data-stu-id="f8823-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="f8823-145">Non sono supportati altri tipi di dati per le proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="f8823-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="f8823-146">**\_Bool UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="f8823-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="f8823-147">**UIAutomationType \_ Double**</span><span class="sxs-lookup"><span data-stu-id="f8823-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="f8823-148">**\_Elemento UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="f8823-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="f8823-149">**\_Int UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="f8823-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="f8823-150">**Punto di UIAutomationType \_**</span><span class="sxs-lookup"><span data-stu-id="f8823-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="f8823-151">**\_Stringa UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="f8823-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="f8823-152">Utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'oggetto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperare un puntatore all'interfaccia [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8823-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="f8823-153">Chiamare il metodo [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) e passare l'indirizzo della struttura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o della struttura [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .</span><span class="sxs-lookup"><span data-stu-id="f8823-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="f8823-154">Il metodo [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**REGISTEREVENT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) restituisce un ID di proprietà o un ID evento che un'applicazione può passare a qualsiasi metodo di automazione interfaccia utente che accetta tale identificatore come parametro.</span><span class="sxs-lookup"><span data-stu-id="f8823-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="f8823-155">Ad esempio, è possibile passare un ID di proprietà registrato al metodo [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) o al metodo [**IUIAutomation:: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .</span><span class="sxs-lookup"><span data-stu-id="f8823-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="f8823-156">Nell'esempio seguente viene illustrato come registrare una proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f8823-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="f8823-157">Gli identificatori di proprietà e di evento recuperati dai metodi [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) e [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) sono validi solo nel contesto dell'applicazione che li recupera e solo per la durata della durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8823-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="f8823-158">I metodi di registrazione possono restituire valori integer diversi per lo stesso GUID quando viene chiamato su istanze di runtime diverse della stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8823-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="f8823-159">Non esiste alcun metodo che annulla la registrazione di una proprietà o di un evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="f8823-160">Viene invece annullata la registrazione in modo implicito quando viene rilasciato l'ultimo oggetto di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f8823-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8823-161">Se il codice è un client Microsoft Active Accessibility (MSAA), è necessario chiamare la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) quando si modifica il valore di una proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f8823-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="f8823-162">Implementazione di pattern di controllo personalizzati</span><span class="sxs-lookup"><span data-stu-id="f8823-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="f8823-163">Un pattern di controllo personalizzato non è incluso nell'API di automazione interfaccia utente, ma viene fornito da terze parti in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f8823-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="f8823-164">Gli sviluppatori di applicazioni client e provider devono collaborare per definire un pattern di controllo personalizzato, inclusi i metodi, le proprietà e gli eventi che il pattern di controllo supporterà.</span><span class="sxs-lookup"><span data-stu-id="f8823-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="f8823-165">Dopo aver definito il pattern di controllo, sia il client che il provider devono implementare oggetti di supporto Component Object Model (COM), insieme al codice per registrare il pattern di controllo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f8823-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="f8823-166">Un pattern di controllo personalizzato richiede l'implementazione di due oggetti COM: un wrapper client e un gestore di pattern.</span><span class="sxs-lookup"><span data-stu-id="f8823-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="f8823-167">Gli esempi negli argomenti seguenti illustrano come implementare un pattern di controllo personalizzato che duplica la funzionalità del pattern di controllo [value](uiauto-implementingvalue.md) esistente.</span><span class="sxs-lookup"><span data-stu-id="f8823-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="f8823-168">Questi esempi sono solo a scopo informativo.</span><span class="sxs-lookup"><span data-stu-id="f8823-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="f8823-169">Un pattern di controllo personalizzato effettivo deve fornire funzionalità non disponibili nei modelli di controllo di automazione interfaccia utente standard.</span><span class="sxs-lookup"><span data-stu-id="f8823-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="f8823-170">Il wrapper client e il gestore pattern</span><span class="sxs-lookup"><span data-stu-id="f8823-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="f8823-171">Il wrapper client implementa l'API usata dal client per recuperare le proprietà e chiamare i metodi esposti dal pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="f8823-172">L'API viene implementata come interfaccia COM che passa tutte le richieste di proprietà e le chiamate al metodo al core di automazione interfaccia utente, che quindi esegue il marshalling delle richieste e delle chiamate al provider.</span><span class="sxs-lookup"><span data-stu-id="f8823-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="f8823-173">Il codice che registra un pattern di controllo personalizzato deve fornire un class factory che l'automazione interfaccia utente possa usare per creare istanze dell'oggetto wrapper client.</span><span class="sxs-lookup"><span data-stu-id="f8823-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="f8823-174">Quando un pattern di controllo personalizzato viene registrato correttamente, l'automazione interfaccia utente restituisce un puntatore a interfaccia [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) che viene usato dal client per l'invio delle richieste di proprietà e delle chiamate ai metodi al core di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f8823-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="f8823-175">Sul lato del provider, il nucleo di automazione interfaccia utente acquisisce le richieste di proprietà e le chiamate ai metodi dal client e le passa all'oggetto del gestore di pattern.</span><span class="sxs-lookup"><span data-stu-id="f8823-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="f8823-176">Il gestore pattern chiama quindi i metodi appropriati nell'interfaccia del provider per il pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="f8823-177">Il codice che registra un pattern di controllo personalizzato crea l'oggetto del gestore pattern e, quando si registra il pattern di controllo, fornisce l'automazione dell'interfaccia utente con un puntatore all'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8823-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="f8823-178">Il diagramma seguente illustra il flusso di una richiesta di proprietà client o di una chiamata al metodo dal wrapper client, tramite i componenti di base di automazione interfaccia utente al gestore pattern e quindi all'interfaccia del provider.</span><span class="sxs-lookup"><span data-stu-id="f8823-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![diagramma che mostra il flusso dal wrapper client al gestore pattern e il provider](images/custompatternsupport.jpg)

<span data-ttu-id="f8823-180">Gli oggetti che implementano le interfacce del gestore del modello e del wrapper client devono essere a thread libero.</span><span class="sxs-lookup"><span data-stu-id="f8823-180">The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id="f8823-181">Inoltre, il nucleo di automazione interfaccia utente deve essere in grado di chiamare direttamente gli oggetti senza alcun codice di marshalling intermedio.</span><span class="sxs-lookup"><span data-stu-id="f8823-181">Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name="implementing-the-client-wrapper"></a><span data-ttu-id="f8823-182">Implementazione del wrapper client</span><span class="sxs-lookup"><span data-stu-id="f8823-182">Implementing the Client Wrapper</span></span>

<span data-ttu-id="f8823-183">Il wrapper client è un oggetto che espone un'interfaccia IXxxPattern che il client usa per richiedere proprietà e chiamare metodi supportati dal pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-183">The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id="f8823-184">L'interfaccia è costituita da una coppia di metodi "getter" per ogni proprietà supportata (Get \_ CurrentXxx e Get \_ CachedXxx Method) e un metodo "Caller" per ogni metodo supportato.</span><span class="sxs-lookup"><span data-stu-id="f8823-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="f8823-185">Quando viene creata un'istanza dell'oggetto, il costruttore dell'oggetto riceve un puntatore all'interfaccia [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , implementata dal core di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f8823-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="f8823-186">I metodi dell'interfaccia IXxxPattern usano i metodi [**IUIAutomationPatternInstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) e [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) per inviare le richieste di proprietà e le chiamate al metodo al core di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f8823-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="f8823-187">Nell'esempio seguente viene illustrato come implementare un oggetto wrapper client per un semplice pattern di controllo personalizzato che supporta una singola proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8823-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="f8823-188">Per un esempio più complesso, vedere [implementazione di esempio di un pattern di controllo personalizzato](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="f8823-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="f8823-189">Implementazione del gestore pattern</span><span class="sxs-lookup"><span data-stu-id="f8823-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="f8823-190">Il gestore dei criteri è un oggetto che implementa l'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) .</span><span class="sxs-lookup"><span data-stu-id="f8823-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="f8823-191">Questa interfaccia dispone di due metodi: [**IUIAutomationPatternHandler:: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) e [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span><span class="sxs-lookup"><span data-stu-id="f8823-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="f8823-192">Il metodo **CreateClientWrapper** viene chiamato dal core di automazione interfaccia utente e riceve un puntatore all'interfaccia [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) .</span><span class="sxs-lookup"><span data-stu-id="f8823-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="f8823-193">**CreateClientWrapper** risponde creando un'istanza dell'oggetto wrapper client e passando il puntatore all'interfaccia **IUIAutomationPatternInstance** al costruttore del wrapper client.</span><span class="sxs-lookup"><span data-stu-id="f8823-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="f8823-194">Il metodo [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) viene usato dal core di automazione interfaccia utente per passare le richieste di proprietà e le chiamate ai metodi all'interfaccia del provider per il pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="f8823-195">I parametri includono un puntatore all'interfaccia del provider, l'indice in base zero del metodo di richiamo della proprietà o del metodo chiamato e una matrice di strutture [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) che contengono i parametri da passare al provider.</span><span class="sxs-lookup"><span data-stu-id="f8823-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="f8823-196">Il gestore di pattern risponde controllando il parametro index per determinare il metodo del provider da chiamare e quindi chiama l'interfaccia del provider, passando i parametri contenuti nelle strutture **UIAutomationParameter** .</span><span class="sxs-lookup"><span data-stu-id="f8823-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="f8823-197">Viene creata un'istanza dell'oggetto pattern handler dallo stesso codice che registra il pattern di controllo personalizzato, prima che il pattern di controllo venga registrato.</span><span class="sxs-lookup"><span data-stu-id="f8823-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="f8823-198">Il codice deve passare il puntatore all'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) dell'oggetto gestore pattern al core di automazione interfaccia utente al momento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="f8823-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="f8823-199">Nell'esempio seguente viene illustrato come implementare un oggetto gestore di pattern per un semplice pattern di controllo personalizzato che supporta una singola proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8823-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="f8823-200">Per un esempio più complesso, vedere [implementazione di esempio di un pattern di controllo personalizzato](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="f8823-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="f8823-201">Registrazione di un pattern di controllo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f8823-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="f8823-202">Prima di poter essere usato, un pattern di controllo personalizzato deve essere registrato sia dal provider che dal client.</span><span class="sxs-lookup"><span data-stu-id="f8823-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="f8823-203">La registrazione fornisce al core di automazione interfaccia utente informazioni dettagliate sul pattern di controllo e fornisce il provider o il client con l'ID del pattern di controllo e gli ID per le proprietà e gli eventi supportati dal pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="f8823-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="f8823-204">Sul lato del provider, il pattern di controllo personalizzato deve essere registrato prima che il controllo associato gestisca il messaggio [**WM \_ GetObject**](wm-getobject.md) o nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="f8823-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="f8823-205">Quando si registra un pattern di controllo personalizzato, il provider o il client fornisce le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8823-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="f8823-206">GUID del pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="f8823-207">Stringa non localizzabile che contiene il nome del pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="f8823-208">GUID dell'interfaccia del provider che supporta il pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="f8823-209">GUID dell'interfaccia client che supporta il pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="f8823-210">Matrice di strutture [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) che descrivono le proprietà supportate dal pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="f8823-211">Per ogni proprietà è necessario specificare il GUID, il nome della proprietà e il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="f8823-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="f8823-212">Matrice di strutture [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) che descrivono i metodi supportati dal pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="f8823-213">Per ogni metodo, la struttura include le informazioni seguenti: il nome del metodo, il conteggio dei parametri, un elenco di tipi di dati dei parametri e un elenco dei nomi di parametro.</span><span class="sxs-lookup"><span data-stu-id="f8823-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="f8823-214">Matrice di strutture [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) che descrivono gli eventi generati dal pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="f8823-215">Per ogni evento, è necessario specificare il GUID e il nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f8823-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="f8823-216">Indirizzo dell'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) dell'oggetto gestore di pattern che rende disponibile il pattern di controllo personalizzato ai client.</span><span class="sxs-lookup"><span data-stu-id="f8823-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="f8823-217">Per registrare il pattern di controllo personalizzato, il codice client o il provider deve eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8823-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="f8823-218">Riempire una struttura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) con le informazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="f8823-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="f8823-219">Utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'oggetto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperare un puntatore all'interfaccia [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8823-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="f8823-220">Chiamare il metodo [**IUIAutomationRegistrar:: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , passando l'indirizzo della struttura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .</span><span class="sxs-lookup"><span data-stu-id="f8823-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="f8823-221">Il metodo [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) restituisce un ID pattern di controllo, insieme a un elenco di ID di proprietà e ID evento.</span><span class="sxs-lookup"><span data-stu-id="f8823-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="f8823-222">Un'applicazione può passare questi ID a qualsiasi metodo di automazione interfaccia utente che accetta tale identificatore come parametro.</span><span class="sxs-lookup"><span data-stu-id="f8823-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="f8823-223">Ad esempio, è possibile passare un ID modello registrato al metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) per recuperare un puntatore all'interfaccia del provider per il pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="f8823-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="f8823-224">Non esiste alcun metodo che annulla la registrazione di un pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="f8823-225">Viene invece annullata la registrazione in modo implicito quando viene rilasciato l'ultimo oggetto di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f8823-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="f8823-226">Per un esempio in cui viene illustrato come registrare un pattern di controllo personalizzato, vedere la sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="f8823-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="f8823-227">Implementazione di esempio di un pattern di controllo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f8823-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="f8823-228">Questa sezione contiene codice di esempio che illustra come implementare gli oggetti wrapper client e gestore pattern per un pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8823-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="f8823-229">Nell'esempio viene implementato un pattern di controllo personalizzato basato sul pattern di controllo [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f8823-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f8823-230">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8823-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f8823-231">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f8823-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8823-232">Progettazione di proprietà, eventi e pattern di controllo personalizzati</span><span class="sxs-lookup"><span data-stu-id="f8823-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="f8823-233">Cenni preliminari sulle proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f8823-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="f8823-234">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f8823-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="f8823-235">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f8823-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 