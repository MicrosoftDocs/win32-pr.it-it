---
title: Funzioni del pattern di controllo deprecate
description: Funzioni del pattern di controllo deprecate
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395470"
---
# <a name="deprecated-control-pattern-functions"></a><span data-ttu-id="ba464-103">Funzioni del pattern di controllo deprecate</span><span class="sxs-lookup"><span data-stu-id="ba464-103">Deprecated Control Pattern Functions</span></span>

> [!Note]  
> <span data-ttu-id="ba464-104">Le funzioni del pattern di controllo descritte in questa sezione sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="ba464-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="ba464-105">Le applicazioni client devono usare le interfacce Component Object Model (COM) descritte nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba464-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="ba464-106">Interfacce degli elementi di automazione interfaccia utente per i client</span><span class="sxs-lookup"><span data-stu-id="ba464-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="ba464-107">Interfaccia della condizione di proprietà per i client</span><span class="sxs-lookup"><span data-stu-id="ba464-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="ba464-108">Interfacce del pattern di controllo per i client</span><span class="sxs-lookup"><span data-stu-id="ba464-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="ba464-109">Interfacce di gestione degli eventi per i client</span><span class="sxs-lookup"><span data-stu-id="ba464-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="ba464-110">Interfacce Factory proxy per i client</span><span class="sxs-lookup"><span data-stu-id="ba464-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="ba464-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ba464-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba464-112">Funzione</span><span class="sxs-lookup"><span data-stu-id="ba464-112">Function</span></span></th>
<th><span data-ttu-id="ba464-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba464-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ba464-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-115">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-115">This function is deprecated.</span></span> <span data-ttu-id="ba464-116">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ba464-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-117">Ancora l'elemento di automazione interfaccia utente in corrispondenza della <em>impostata su DockPosition</em> richiesta all'interno di un contenitore di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="ba464-117">Docks the UI Automation element at the requested <em>dockPosition</em> within a docking container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-119">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-119">This function is deprecated.</span></span> <span data-ttu-id="ba464-120">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-121">Nasconde tutti i nodi, i controlli o il contenuto discendente dell'elemento di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-121">Hides all descendant nodes, controls, or content of the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-123">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-123">This function is deprecated.</span></span> <span data-ttu-id="ba464-124">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-125">Espande un controllo sullo schermo in modo da visualizzare altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ba464-125">Expands a control on the screen so that it shows more information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-127">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-127">This function is deprecated.</span></span> <span data-ttu-id="ba464-128">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-129">Ottiene il nodo per un elemento in una griglia.</span><span class="sxs-lookup"><span data-stu-id="ba464-129">Gets the node for an item in a grid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-131">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-131">This function is deprecated.</span></span> <span data-ttu-id="ba464-132">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-133">Invia una richiesta per l'attivazione di un controllo e l'avvio dell'azione singola e non ambigua corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ba464-133">Sends a request to activate a control and initiate its single, unambiguous action.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-135">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-135">This function is deprecated.</span></span> <span data-ttu-id="ba464-136">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-137">Recupera un nodo all'interno di un nodo contenitore, in base al valore di una proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="ba464-137">Retrieves a node within a containing node, based on a specified property value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-139">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-139">This function is deprecated.</span></span> <span data-ttu-id="ba464-140">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-140">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-141">Esegue l'azione predefinita Microsoft Active Accessibility per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ba464-141">Performs the Microsoft Active Accessibility default action for the element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-143">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-143">This function is deprecated.</span></span> <span data-ttu-id="ba464-144">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-144">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-145">Recupera un oggetto <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> che corrisponde all'elemento di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-145">Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> object that corresponds to the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-147">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-147">This function is deprecated.</span></span> <span data-ttu-id="ba464-148">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-148">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-149">Esegue una selezione di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="ba464-149">Performs a Microsoft Active Accessibility selection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-151">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-151">This function is deprecated.</span></span> <span data-ttu-id="ba464-152">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-152">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-153">Imposta la proprietà del valore di Microsoft Active Accessibility per il nodo.</span><span class="sxs-lookup"><span data-stu-id="ba464-153">Sets the Microsoft Active Accessibility value property for the node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-155">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-155">This function is deprecated.</span></span> <span data-ttu-id="ba464-156">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-156">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-157">Recupera il nome di una visualizzazione specifica del controllo.</span><span class="sxs-lookup"><span data-stu-id="ba464-157">Retrieves the name of a control-specific view.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-159">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-159">This function is deprecated.</span></span> <span data-ttu-id="ba464-160">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-160">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-161">Imposta un controllo su un layout diverso.</span><span class="sxs-lookup"><span data-stu-id="ba464-161">Sets a control to a different layout.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-163">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-163">This function is deprecated.</span></span> <span data-ttu-id="ba464-164">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-164">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-165">Imposta il valore di un controllo che ha un intervallo numerico.</span><span class="sxs-lookup"><span data-stu-id="ba464-165">Sets the value of a control that has a numerical range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-167">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-167">This function is deprecated.</span></span> <span data-ttu-id="ba464-168">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-168">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-169">Scorre l'area di contenuto di un oggetto contenitore per visualizzare l'elemento di automazione interfaccia utente all'interno dell'area visibile (viewport) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ba464-169">Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-171">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-171">This function is deprecated.</span></span> <span data-ttu-id="ba464-172">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-172">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-173">Scorre l'area attualmente visibile dell'area di contenuto del <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>specificato, orizzontalmente, verticalmente o entrambi.</span><span class="sxs-lookup"><span data-stu-id="ba464-173">Scrolls the currently visible region of the content area the specified <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-175">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-175">This function is deprecated.</span></span> <span data-ttu-id="ba464-176">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-176">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-177">Scorre un contenitore in una posizione specifica orizzontalmente, verticalmente o entrambi.</span><span class="sxs-lookup"><span data-stu-id="ba464-177">Scrolls a container to a specific position horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-179">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-179">This function is deprecated.</span></span> <span data-ttu-id="ba464-180">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-180">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-181">Aggiunge un elemento non selezionato a una selezione in un controllo.</span><span class="sxs-lookup"><span data-stu-id="ba464-181">Adds an unselected element to a selection in a control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-183">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-183">This function is deprecated.</span></span> <span data-ttu-id="ba464-184">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-184">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-185">Rimuove un elemento dalla selezione in un contenitore di selezione.</span><span class="sxs-lookup"><span data-stu-id="ba464-185">Removes an element from the selection in a selection container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-187">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-187">This function is deprecated.</span></span> <span data-ttu-id="ba464-188">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-188">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-189">Seleziona un elemento in un contenitore di selezione.</span><span class="sxs-lookup"><span data-stu-id="ba464-189">Selects an element in a selection container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-191">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-191">This function is deprecated.</span></span> <span data-ttu-id="ba464-192">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-192">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-193">Causa l'interruzione dell'ascolto da parte del provider di automazione interfaccia utente per l'input del mouse o della tastiera.</span><span class="sxs-lookup"><span data-stu-id="ba464-193">Causes the UI Automation provider to stop listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-195">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-195">This function is deprecated.</span></span> <span data-ttu-id="ba464-196">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-196">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-197">Fa in modo che il provider di automazione interfaccia utente inizi ad ascoltare l'input del mouse o della tastiera.</span><span class="sxs-lookup"><span data-stu-id="ba464-197">Causes the UI Automation provider to start listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-199">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-199">This function is deprecated.</span></span> <span data-ttu-id="ba464-200">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-200">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-201">Ottiene l'intervallo di testo per l'intero documento.</span><span class="sxs-lookup"><span data-stu-id="ba464-201">Gets the text range for the entire document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-203">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-203">This function is deprecated.</span></span> <span data-ttu-id="ba464-204">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-204">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-205">Verifica se il contenuto del contenitore di testo può essere selezionato e deselezionato.</span><span class="sxs-lookup"><span data-stu-id="ba464-205">Ascertains whether the text container's contents can be selected and deselected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-207">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-207">This function is deprecated.</span></span> <span data-ttu-id="ba464-208">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-208">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-209">Ottiene l'intervallo corrente del testo selezionato da un contenitore di testo che supporta il pattern di testo.</span><span class="sxs-lookup"><span data-stu-id="ba464-209">Gets the current range of selected text from a text container supporting the text pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-211">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-211">This function is deprecated.</span></span> <span data-ttu-id="ba464-212">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-212">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-213">Recupera una matrice di intervalli di testo non contigui da un contenitore di testo in cui ogni intervallo di testo inizia con la prima riga parzialmente visibile fino alla fine dell'ultima riga parzialmente visibile.</span><span class="sxs-lookup"><span data-stu-id="ba464-213">Retrieves an array of disjoint text ranges from a text container where each text range begins with the first partially visible line through to the end of the last partially visible line.</span></span> <span data-ttu-id="ba464-214">Un layout a più colonne, ad esempio, in cui le colonne vengono parzialmente esposte all'esterno dell'area visibile del viewport e il contenuto passa dalla parte inferiore di una colonna alla parte superiore della successiva.</span><span class="sxs-lookup"><span data-stu-id="ba464-214">For example, a multi-column layout where the columns are partially scrolled out of the visible area of the viewport and the content flows from the bottom of one column to the top of the next.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-216">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-216">This function is deprecated.</span></span> <span data-ttu-id="ba464-217">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-218">Ottiene l'intervallo di testo su cui si estende un determinato nodo.</span><span class="sxs-lookup"><span data-stu-id="ba464-218">Gets the text range that a given node spans.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-220">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-220">This function is deprecated.</span></span> <span data-ttu-id="ba464-221">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-222">Recupera l'intervallo di testo degenerato (vuoto) più vicino alle coordinate dello schermo specificate.</span><span class="sxs-lookup"><span data-stu-id="ba464-222">Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-224">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-224">This function is deprecated.</span></span> <span data-ttu-id="ba464-225">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-226">Aggiunge alla raccolta esistente del testo evidenziato in un contenitore di testo che supporta più selezioni non contigue evidenziando il testo supplementare corrispondente agli endpoint <em>iniziale</em> e <em>finale</em> dell'intervallo di testo chiamante.</span><span class="sxs-lookup"><span data-stu-id="ba464-226">Adds to the existing collection of highlighted text in a text container that supports multiple, disjoint selections by highlighting supplementary text corresponding to the calling text range <em>Start</em> and <em>End</em> endpoints.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-228">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-228">This function is deprecated.</span></span> <span data-ttu-id="ba464-229">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-230">Copia un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="ba464-230">Copies a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-232">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-232">This function is deprecated.</span></span> <span data-ttu-id="ba464-233">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-233">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-234">Confronta due intervalli di testo.</span><span class="sxs-lookup"><span data-stu-id="ba464-234">Compares two text ranges.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-236">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-236">This function is deprecated.</span></span> <span data-ttu-id="ba464-237">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-237">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-238">Restituisce un valore che indica se due intervalli di testo hanno endpoint identici.</span><span class="sxs-lookup"><span data-stu-id="ba464-238">Returns a value indicating whether two text ranges have identical endpoints.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-240">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-240">This function is deprecated.</span></span> <span data-ttu-id="ba464-241">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-241">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-242">Espande l'intervallo di testo a un'unità più grande o più piccola, ad esempio carattere, parola, riga o pagina.</span><span class="sxs-lookup"><span data-stu-id="ba464-242">Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-244">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-244">This function is deprecated.</span></span> <span data-ttu-id="ba464-245">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-245">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-246">Cerca in una direzione specificata la prima parte di testo che supporta un attributo di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba464-246">Searches in a specified direction for the first piece of text supporting a specified text attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-248">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-248">This function is deprecated.</span></span> <span data-ttu-id="ba464-249">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-249">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-250">Restituisce il primo intervallo di testo nella direzione specificata che contiene il testo che il client sta cercando.</span><span class="sxs-lookup"><span data-stu-id="ba464-250">Returns the first text range in the specified direction that contains the text the client is searching for.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-252">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-252">This function is deprecated.</span></span> <span data-ttu-id="ba464-253">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-253">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-254">Ottiene il valore di un attributo di testo per un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="ba464-254">Gets the value of an text attribute for a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-256">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-256">This function is deprecated.</span></span> <span data-ttu-id="ba464-257">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-257">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-258">Recupera il numero minimo di rettangoli di delimitazione che possono racchiudere l'intervallo, un rettangolo per riga.</span><span class="sxs-lookup"><span data-stu-id="ba464-258">Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-260">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-260">This function is deprecated.</span></span> <span data-ttu-id="ba464-261">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-261">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-262">Restituisce tutti gli elementi di automazione interfaccia utente contenuti all'interno dell'intervallo di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba464-262">Returns all UI Automation elements contained within the specified text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-264">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-264">This function is deprecated.</span></span> <span data-ttu-id="ba464-265">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-265">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-266">Restituisce il nodo per il provider più piccolo successivo che copre l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="ba464-266">Returns the node for the next smallest provider that covers the range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-268">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-268">This function is deprecated.</span></span> <span data-ttu-id="ba464-269">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-269">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-270">Restituisce il testo in un intervallo di testo, fino a un numero di caratteri specificato.</span><span class="sxs-lookup"><span data-stu-id="ba464-270">Returns the text in a text range, up to a specified number of characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-272">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-272">This function is deprecated.</span></span> <span data-ttu-id="ba464-273">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-273">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-274">Sposta l'intervallo di testo del numero di unità specificato richiesto dal client.</span><span class="sxs-lookup"><span data-stu-id="ba464-274">Moves the text range the specified number of units requested by the client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-276">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-276">This function is deprecated.</span></span> <span data-ttu-id="ba464-277">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-277">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-278">Sposta un endpoint di un intervallo nell'endpoint di un altro intervallo.</span><span class="sxs-lookup"><span data-stu-id="ba464-278">Moves an endpoint of one range to the endpoint of another range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-280">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-280">This function is deprecated.</span></span> <span data-ttu-id="ba464-281">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-281">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-282">Sposta un endpoint dell'intervallo del numero di unità specificato.</span><span class="sxs-lookup"><span data-stu-id="ba464-282">Moves an endpoint of the range the specified number of units.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-284">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-284">This function is deprecated.</span></span> <span data-ttu-id="ba464-285">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-285">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-286">Rimuove il testo selezionato, corrispondente all'intervallo di testo chiamante <em>TextPatternRangeEndpoint_Start</em> e <em>TextPatternRangeEndpoint_End</em> endpoint, da una raccolta esistente di testo selezionato in un contenitore di testo che supporta selezioni multiple non contigue.</span><span class="sxs-lookup"><span data-stu-id="ba464-286">Removes the selected text, corresponding to the calling text range <em>TextPatternRangeEndpoint_Start</em> and <em>TextPatternRangeEndpoint_End</em> endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-288">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-288">This function is deprecated.</span></span> <span data-ttu-id="ba464-289">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-289">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-290">Scorre il testo in modo che l'intervallo specificato sia visibile nel viewport.</span><span class="sxs-lookup"><span data-stu-id="ba464-290">Scrolls the text so the specified range is visible in the viewport.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-292">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-292">This function is deprecated.</span></span> <span data-ttu-id="ba464-293">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-293">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-294">Seleziona un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="ba464-294">Selects a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-296">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-296">This function is deprecated.</span></span> <span data-ttu-id="ba464-297">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-297">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-298">Consente di impostare un controllo sullo stato successivo supportato.</span><span class="sxs-lookup"><span data-stu-id="ba464-298">Toggles a control to its next supported state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-300">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-300">This function is deprecated.</span></span> <span data-ttu-id="ba464-301">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-301">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-302">Sposta un elemento in una posizione specificata sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="ba464-302">Moves an element to a specified location on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-304">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-304">This function is deprecated.</span></span> <span data-ttu-id="ba464-305">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-305">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-306">Ridimensiona un elemento sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="ba464-306">Resizes an element on the screen.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-308">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-308">This function is deprecated.</span></span> <span data-ttu-id="ba464-309">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-309">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-310">Ruota un elemento sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="ba464-310">Rotates an element on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-312">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-312">This function is deprecated.</span></span> <span data-ttu-id="ba464-313">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-313">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-314">Imposta il valore di testo di un elemento.</span><span class="sxs-lookup"><span data-stu-id="ba464-314">Sets the text value of an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-316">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-316">This function is deprecated.</span></span> <span data-ttu-id="ba464-317">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-317">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-318">Rende l'elemento virtuale completamente accessibile come elemento di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-318">Makes the virtual item fully accessible as a UI Automation element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-320">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-320">This function is deprecated.</span></span> <span data-ttu-id="ba464-321">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-321">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-322">Chiude una finestra aperta.</span><span class="sxs-lookup"><span data-stu-id="ba464-322">Closes an open window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba464-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-324">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-324">This function is deprecated.</span></span> <span data-ttu-id="ba464-325">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-325">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-326">Imposta lo stato di visualizzazione di una finestra; ad esempio, per ingrandire una finestra.</span><span class="sxs-lookup"><span data-stu-id="ba464-326">Sets the visual state of a window; for example, to maximize a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba464-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba464-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ba464-328">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ba464-328">This function is deprecated.</span></span> <span data-ttu-id="ba464-329">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ba464-329">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="ba464-330">Comporta il blocco del codice chiamante per il lasso di tempo specificato o finché il processo associato non entra in stato di inattività, in base alla prima condizione che viene soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="ba464-330">Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ba464-331">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba464-331">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba464-332">Client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ba464-332">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





