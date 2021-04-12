---
title: Cenni preliminari sulle proprietà di automazione interfaccia utente
description: I provider di automazione interfaccia utente Microsoft espongono proprietà sugli elementi di automazione interfaccia utente. Le proprietà consentono alle applicazioni client di recuperare informazioni sui controlli.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automazione interfaccia utente, panoramica delle proprietà
- Automazione interfaccia utente, proprietà e eventi
- Automazione interfaccia utente, eventi e proprietà
- Proprietà, informazioni
- Proprietà, identificatori
- Proprietà, valori
- Proprietà, eventi
- eventi, proprietà
- Proprietà, dinamiche
- proprietà dinamiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220863"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="acf85-114">Cenni preliminari sulle proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="acf85-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="acf85-115">I provider di automazione interfaccia utente Microsoft espongono proprietà sugli elementi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="acf85-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="acf85-116">Le proprietà consentono alle applicazioni client di recuperare informazioni sui controlli.</span><span class="sxs-lookup"><span data-stu-id="acf85-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="acf85-117">Automazione interfaccia utente espone due tipi diversi di proprietà: le *proprietà degli elementi di automazione* e i pattern di *controllo*.</span><span class="sxs-lookup"><span data-stu-id="acf85-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="acf85-118">Le proprietà degli elementi di automazione sono costituite da un set comune di proprietà, ad esempio Name, AcceleratorKey e NomeClasse, che sono esposte da tutti gli elementi di automazione interfaccia utente, indipendentemente dal tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="acf85-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="acf85-119">La maggior parte delle proprietà degli elementi di automazione sono valori statici.</span><span class="sxs-lookup"><span data-stu-id="acf85-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="acf85-120">Le proprietà del pattern di controllo sono quelle esposte da un controllo che supporta un particolare pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="acf85-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="acf85-121">Ogni pattern di controllo ha un set corrispondente di proprietà del pattern di controllo che il controllo deve esporre.</span><span class="sxs-lookup"><span data-stu-id="acf85-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="acf85-122">Ad esempio, un controllo che supporta il pattern di controllo [Grid](uiauto-implementinggrid.md) espone le proprietà ColumnCount e RowCount.</span><span class="sxs-lookup"><span data-stu-id="acf85-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="acf85-123">La maggior parte delle proprietà dei pattern di controllo sono valori dinamici.</span><span class="sxs-lookup"><span data-stu-id="acf85-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="acf85-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="acf85-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="acf85-125">Identificatori di proprietà</span><span class="sxs-lookup"><span data-stu-id="acf85-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="acf85-126">Valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="acf85-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="acf85-127">Proprietà ed eventi</span><span class="sxs-lookup"><span data-stu-id="acf85-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="acf85-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acf85-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="acf85-129">Identificatori di proprietà</span><span class="sxs-lookup"><span data-stu-id="acf85-129">Property Identifiers</span></span>

<span data-ttu-id="acf85-130">Ogni proprietà è identificata da un valore numerico **PROPERTYID** denominato *identificatore di proprietà* (ID).</span><span class="sxs-lookup"><span data-stu-id="acf85-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="acf85-131">I provider e i client utilizzano gli ID numerici nelle chiamate al metodo, ad esempio [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**IUIAutomationElement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) per identificare le richieste di proprietà.</span><span class="sxs-lookup"><span data-stu-id="acf85-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="acf85-132">Per una descrizione dettagliata di ogni identificatore di proprietà di automazione interfaccia utente, inclusi il tipo di dati e il valore predefinito di ogni proprietà, vedere [identificatori di proprietà](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="acf85-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="acf85-133">Valori della proprietà</span><span class="sxs-lookup"><span data-stu-id="acf85-133">Property Values</span></span>

<span data-ttu-id="acf85-134">Tutte le proprietà sono di sola lettura, sebbene alcune possano essere modificate utilizzando metodi che agiscono sul controllo, ad esempio [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) o [**IUIAutomationDockPattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span><span class="sxs-lookup"><span data-stu-id="acf85-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="acf85-135">Per informazioni sul recupero dei valori delle proprietà, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="acf85-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="acf85-136">Proprietà ed eventi</span><span class="sxs-lookup"><span data-stu-id="acf85-136">Properties and Events</span></span>

<span data-ttu-id="acf85-137">Strettamente associato alle proprietà in automazione interfaccia utente è il concetto di *eventi di modifica della proprietà*.</span><span class="sxs-lookup"><span data-stu-id="acf85-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="acf85-138">Per le proprietà dinamiche, un'applicazione client necessita di un modo per capire che un valore di proprietà è stato modificato, in modo che possa aggiornare la cache delle informazioni o rispondere in altro modo alle nuove informazioni.</span><span class="sxs-lookup"><span data-stu-id="acf85-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="acf85-139">I client possono eseguire la registrazione per restare in ascolto degli eventi di modifica della proprietà su qualsiasi proprietà.</span><span class="sxs-lookup"><span data-stu-id="acf85-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="acf85-140">I provider generano eventi quando viene modificato un elemento nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="acf85-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="acf85-141">Se, ad esempio, una casella di controllo è selezionata o deselezionata, viene generato un evento di modifica della proprietà dall'implementazione del provider del pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="acf85-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="acf85-142">I provider possono generare gli eventi in modo selettivo, a seconda che i client siano in ascolto di eventi oppure di eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="acf85-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="acf85-143">Non tutte le modifiche di proprietà generano eventi. Questo dipende totalmente dall'implementazione del provider di automazione interfaccia utente per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="acf85-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="acf85-144">Ad esempio, i provider di proxy standard per le caselle di riepilogo non generano un evento di modifica della proprietà quando la proprietà Selection viene modificata.</span><span class="sxs-lookup"><span data-stu-id="acf85-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="acf85-145">In questo caso, l'applicazione deve rimanere in ascolto dell'evento generato quando la selezione cambia ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="acf85-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="acf85-146">I client restano in ascolto degli eventi sottoscrivendoli, come descritto in [sottoscrizione di eventi di automazione interfaccia utente](uiauto-eventsforclients.md).</span><span class="sxs-lookup"><span data-stu-id="acf85-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="acf85-147">Per gli eventi di modifica delle proprietà in particolare, i client devono implementare [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) e passare l'interfaccia a [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span><span class="sxs-lookup"><span data-stu-id="acf85-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acf85-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acf85-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="acf85-149">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="acf85-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="acf85-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="acf85-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="acf85-151">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="acf85-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="acf85-152">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="acf85-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="acf85-153">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="acf85-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="acf85-154">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="acf85-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="acf85-155">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="acf85-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="acf85-156">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="acf85-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="acf85-157">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="acf85-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




