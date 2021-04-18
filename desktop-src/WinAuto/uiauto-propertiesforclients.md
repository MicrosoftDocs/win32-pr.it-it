---
title: Recupero di proprietà da elementi di automazione interfaccia utente
description: Le proprietà degli oggetti IUIAutomationElement contengono informazioni sugli elementi dell'interfaccia utente, in genere i controlli.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- client, acquisizione di elementi di automazione interfaccia utente
- client, elementi di automazione interfaccia utente
- client, proprietà
- client, recupero di proprietà
- client, proprietà di automazione interfaccia utente
- Automazione interfaccia utente, recupero di elementi
- Automazione interfaccia utente, elementi
- Automazione interfaccia utente, proprietà
- Automazione interfaccia utente, recupero di proprietà
- recupero di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300267"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="52a00-113">Recupero di proprietà da elementi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="52a00-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="52a00-114">Le proprietà degli oggetti [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contengono informazioni sugli elementi dell'interfaccia utente, in genere i controlli.</span><span class="sxs-lookup"><span data-stu-id="52a00-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="52a00-115">Le proprietà di un elemento sono generiche. ovvero non è specifico di un tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="52a00-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="52a00-116">Le proprietà specifiche del controllo di un elemento sono esposte dalle relative interfacce del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="52a00-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="52a00-117">Le proprietà di automazione interfaccia utente Microsoft sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="52a00-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="52a00-118">Per impostare le proprietà di un controllo, è necessario usare i metodi del pattern di controllo appropriato.</span><span class="sxs-lookup"><span data-stu-id="52a00-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="52a00-119">Usare, ad esempio, [**IUIAutomationScrollPattern:: scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) per modificare i valori di posizione di una finestra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="52a00-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="52a00-120">Per migliorare le prestazioni, è possibile memorizzare nella cache i valori delle proprietà dei controlli e dei pattern di controllo quando vengono recuperati gli elementi.</span><span class="sxs-lookup"><span data-stu-id="52a00-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="52a00-121">Per altre informazioni, vedere [memorizzazione nella cache delle proprietà e dei pattern di controllo di automazione interfaccia utente](uiauto-cachingforclients.md).</span><span class="sxs-lookup"><span data-stu-id="52a00-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="52a00-122">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="52a00-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="52a00-123">ID di proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="52a00-124">Condizioni della proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="52a00-125">Recupero di proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="52a00-126">Valori di proprietà predefiniti</span><span class="sxs-lookup"><span data-stu-id="52a00-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="52a00-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52a00-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="52a00-128">ID di proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-128">Property IDs</span></span>

<span data-ttu-id="52a00-129">Gli identificatori di proprietà sono definiti in UIAutomationClient. h.</span><span class="sxs-lookup"><span data-stu-id="52a00-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="52a00-130">Vengono usati per specificare le proprietà quando si sottoscrivono eventi di modifica di proprietà, si recuperano i valori delle proprietà e si creano condizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="52a00-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="52a00-131">Gli identificatori di proprietà identificano anche la proprietà che è stata modificata quando viene chiamato [**IUIAutomationPropertyChangedEventHandler:: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .</span><span class="sxs-lookup"><span data-stu-id="52a00-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="52a00-132">Per un elenco degli identificatori di proprietà di automazione interfaccia utente, vedere [identificatori di proprietà](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="52a00-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="52a00-133">Condizioni della proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-133">Property Conditions</span></span>

<span data-ttu-id="52a00-134">Gli ID di proprietà vengono usati nella costruzione di oggetti [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) usati per trovare gli elementi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="52a00-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="52a00-135">Ad esempio, è possibile trovare un elemento con un determinato nome o tutti i controlli abilitati.</span><span class="sxs-lookup"><span data-stu-id="52a00-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="52a00-136">Ogni condizione di proprietà specifica un identificatore di proprietà e il valore a cui deve corrispondere la proprietà.</span><span class="sxs-lookup"><span data-stu-id="52a00-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="52a00-137">Per altre informazioni, vedere gli argomenti di riferimento riportati di seguito:</span><span class="sxs-lookup"><span data-stu-id="52a00-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="52a00-138">**IUIAutomation::CreatePropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="52a00-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="52a00-139">**IUIAutomation::CreatePropertyConditionEx**</span><span class="sxs-lookup"><span data-stu-id="52a00-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="52a00-140">**IUIAutomationElement:: FindFirst**</span><span class="sxs-lookup"><span data-stu-id="52a00-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="52a00-141">**IUIAutomationElement:: FindAll**</span><span class="sxs-lookup"><span data-stu-id="52a00-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="52a00-142">Recupero di proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-142">Retrieving Properties</span></span>

<span data-ttu-id="52a00-143">Alcune proprietà generiche e tutte le proprietà del pattern di controllo sono disponibili come proprietà nell'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) o pattern di controllo e possono essere recuperate tramite una funzione di accesso, ad esempio [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span><span class="sxs-lookup"><span data-stu-id="52a00-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="52a00-144">Inoltre, è possibile recuperare qualsiasi proprietà corrente o memorizzata nella cache (ad eccezione delle proprietà del pattern di controllo) utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="52a00-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="52a00-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="52a00-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="52a00-146">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="52a00-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="52a00-147">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="52a00-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="52a00-148">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="52a00-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="52a00-149">Questi metodi offrono prestazioni leggermente migliori e l'accesso alla gamma completa di proprietà.</span><span class="sxs-lookup"><span data-stu-id="52a00-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="52a00-150">Tuttavia, i valori vengono restituiti nelle strutture [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , mentre le singole funzioni di accesso alle proprietà eseguono il cast del valore al tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="52a00-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="52a00-151">Valori di proprietà predefiniti</span><span class="sxs-lookup"><span data-stu-id="52a00-151">Default Property Values</span></span>

<span data-ttu-id="52a00-152">Se un provider di automazione interfaccia utente non implementa una proprietà, l'automazione interfaccia utente può fornire un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="52a00-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="52a00-153">Ad esempio, se il provider per un controllo non supporta la proprietà identificata da [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), l'automazione interfaccia utente restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="52a00-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="52a00-154">Analogamente, se il provider non supporta la proprietà identificata da [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), automazione interfaccia utente restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="52a00-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="52a00-155">La differenza tra [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) e [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (e tra coppie simili di metodi) consiste nel fatto che il metodo "ex" può specificare che non deve essere restituito alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="52a00-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="52a00-156">In questo caso, il valore restituito è una costante univoca speciale, che indica che la proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="52a00-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="52a00-157">Quando riceve questo valore, l'applicazione può fornire il proprio valore o semplicemente ignorare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="52a00-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52a00-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52a00-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="52a00-159">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="52a00-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="52a00-160">Cenni preliminari sulle proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="52a00-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="52a00-161">Identificatori di proprietà</span><span class="sxs-lookup"><span data-stu-id="52a00-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 