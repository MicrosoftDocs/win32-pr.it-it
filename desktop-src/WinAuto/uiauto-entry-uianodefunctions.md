---
title: Funzioni del nodo deprecate
description: Funzioni del nodo deprecate
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963528"
---
# <a name="deprecated-node-functions"></a><span data-ttu-id="0aca5-103">Funzioni del nodo deprecate</span><span class="sxs-lookup"><span data-stu-id="0aca5-103">Deprecated Node Functions</span></span>

> [!Note]  
> <span data-ttu-id="0aca5-104">Le funzioni del pattern di controllo descritte in questa sezione sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="0aca5-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="0aca5-105">Le applicazioni client devono usare le interfacce Component Object Model (COM) descritte nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0aca5-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="0aca5-106">Interfacce degli elementi di automazione interfaccia utente per i client</span><span class="sxs-lookup"><span data-stu-id="0aca5-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="0aca5-107">Interfaccia della condizione di proprietà per i client</span><span class="sxs-lookup"><span data-stu-id="0aca5-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="0aca5-108">Interfacce del pattern di controllo per i client</span><span class="sxs-lookup"><span data-stu-id="0aca5-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="0aca5-109">Interfacce di gestione degli eventi per i client</span><span class="sxs-lookup"><span data-stu-id="0aca5-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="0aca5-110">Interfacce Factory proxy per i client</span><span class="sxs-lookup"><span data-stu-id="0aca5-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="0aca5-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0aca5-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aca5-112">Funzione</span><span class="sxs-lookup"><span data-stu-id="0aca5-112">Function</span></span></th>
<th><span data-ttu-id="0aca5-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aca5-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aca5-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-115">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-115">This function is deprecated.</span></span> <span data-ttu-id="0aca5-116">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0aca5-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-117">Aggiunge un listener per gli eventi in un nodo nell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-117">Adds a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-119">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-119">This function is deprecated.</span></span> <span data-ttu-id="0aca5-120">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-121">Aggiunge una finestra al listener di eventi.</span><span class="sxs-lookup"><span data-stu-id="0aca5-121">Adds a window to the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-123">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-123">This function is deprecated.</span></span> <span data-ttu-id="0aca5-124">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-125">Funzione implementata dal client chiamata dall'automazione interfaccia utente quando viene generato un evento che il client ha sottoscritto.</span><span class="sxs-lookup"><span data-stu-id="0aca5-125">A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-127">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-127">This function is deprecated.</span></span> <span data-ttu-id="0aca5-128">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-129">Rimuove una finestra dal listener di eventi.</span><span class="sxs-lookup"><span data-stu-id="0aca5-129">Removes a window from the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-131">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-131">This function is deprecated.</span></span> <span data-ttu-id="0aca5-132">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-133">Recupera uno o più nodi di automazione interfaccia utente che corrispondono ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0aca5-133">Retrieves one or more UI Automation nodes that match the search criteria.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-135">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-135">This function is deprecated.</span></span> <span data-ttu-id="0aca5-136">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-137">Ottiene una stringa di errore in modo che possa essere passata al client.</span><span class="sxs-lookup"><span data-stu-id="0aca5-137">Gets an error string so that it can be passed to the client.</span></span> <span data-ttu-id="0aca5-138">Questo metodo non viene utilizzato direttamente dai client.</span><span class="sxs-lookup"><span data-stu-id="0aca5-138">This method is not used directly by clients.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-140">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-140">This function is deprecated.</span></span> <span data-ttu-id="0aca5-141">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-141">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-142">Recupera un <em>pattern di controllo</em>.</span><span class="sxs-lookup"><span data-stu-id="0aca5-142">Retrieves a <em>control pattern</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-144">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-144">This function is deprecated.</span></span> <span data-ttu-id="0aca5-145">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-145">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-146">Recupera il valore di una proprietà di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-146">Retrieves the value of a UI Automation property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-148">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-148">This function is deprecated.</span></span> <span data-ttu-id="0aca5-149">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-149">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-150">Recupera il nodo di automazione interfaccia utente radice.</span><span class="sxs-lookup"><span data-stu-id="0aca5-150">Retrieves the root UI Automation node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-152">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-152">This function is deprecated.</span></span> <span data-ttu-id="0aca5-153">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-153">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-154">Recupera l'identificatore di runtime di un nodo di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-154">Retrieves the runtime identifier of a UI Automation node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-156">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-156">This function is deprecated.</span></span> <span data-ttu-id="0aca5-157">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-157">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-158">Aggiorna la cache dei valori delle proprietà e dei pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="0aca5-158">Updates the cache of property values and control patterns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-160">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-160">This function is deprecated.</span></span> <span data-ttu-id="0aca5-161">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-161">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-162">Ottiene un oggetto pattern di controllo da un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0aca5-162">Gets a control pattern object from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-164">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-164">This function is deprecated.</span></span> <span data-ttu-id="0aca5-165">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-165">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-166">Ottiene un intervallo di testo da un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0aca5-166">Gets a text range from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-168">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-168">This function is deprecated.</span></span> <span data-ttu-id="0aca5-169">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-169">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-170">Ottiene un HUIANODE da un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0aca5-170">Gets an HUIANODE from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-172">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-172">This function is deprecated.</span></span> <span data-ttu-id="0aca5-173">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-173">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-174">Ottiene l'identificatore di tipo integer che può essere utilizzato nei metodi che richiedono PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID o EVENTId.</span><span class="sxs-lookup"><span data-stu-id="0aca5-174">Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-176">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-176">This function is deprecated.</span></span> <span data-ttu-id="0aca5-177">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-177">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-178">Naviga nell'albero di automazione interfaccia utente, recuperando facoltativamente le informazioni memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="0aca5-178">Navigates in the UI Automation tree, optionally retrieving cached information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-180">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-180">This function is deprecated.</span></span> <span data-ttu-id="0aca5-181">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-181">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-182">Recupera il nodo di automazione interfaccia utente per l'elemento dell'interfaccia utente che ha attualmente lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="0aca5-182">Retrieves the UI Automation node for the UI element that currently has input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-184">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-184">This function is deprecated.</span></span> <span data-ttu-id="0aca5-185">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-185">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-186">Recupera il nodo di automazione interfaccia utente associato a una finestra.</span><span class="sxs-lookup"><span data-stu-id="0aca5-186">Retrieves the UI Automation node associated with a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-188">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-188">This function is deprecated.</span></span> <span data-ttu-id="0aca5-189">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-189">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-190">Recupera il nodo di automazione interfaccia utente per l'elemento in corrispondenza del punto specificato.</span><span class="sxs-lookup"><span data-stu-id="0aca5-190">Retrieves the UI Automation node for the element at the specified point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-192">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-192">This function is deprecated.</span></span> <span data-ttu-id="0aca5-193">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-193">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-194">Recupera il nodo di automazione interfaccia utente per un provider di elementi non elaborati.</span><span class="sxs-lookup"><span data-stu-id="0aca5-194">Retrieves the UI Automation node for a raw element provider.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-196">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-196">This function is deprecated.</span></span> <span data-ttu-id="0aca5-197">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-197">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-198">Elimina un nodo dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="0aca5-198">Deletes a node from memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-200">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-200">This function is deprecated.</span></span> <span data-ttu-id="0aca5-201">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-201">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-202">Elimina un oggetto modello allocato dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="0aca5-202">Deletes an allocated pattern object from memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-204">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-204">This function is deprecated.</span></span> <span data-ttu-id="0aca5-205">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-205">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-206">Funzione definita dall'applicazione chiamata dall'automazione interfaccia utente per ottenere un provider sul lato client per un elemento.</span><span class="sxs-lookup"><span data-stu-id="0aca5-206">An application-defined function that is called by UI Automation to obtain a client-side provider for an element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-208">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-208">This function is deprecated.</span></span> <span data-ttu-id="0aca5-209">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-209">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-210">Ottiene un valore booleano che specifica se le coordinate di un rettangolo sono impostate su 0.</span><span class="sxs-lookup"><span data-stu-id="0aca5-210">Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-212">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-212">This function is deprecated.</span></span> <span data-ttu-id="0aca5-213">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-213">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-214">Imposta gli elementi di una struttura <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> su 0.</span><span class="sxs-lookup"><span data-stu-id="0aca5-214">Sets the elements of a <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> structure to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-216">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-216">This function is deprecated.</span></span> <span data-ttu-id="0aca5-217">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-218">Registra il metodo definito dall'applicazione chiamato dall'automazione interfaccia utente per ottenere un provider per un elemento.</span><span class="sxs-lookup"><span data-stu-id="0aca5-218">Registers the application-defined method that is called by UI Automation to obtain a provider for an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-220">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-220">This function is deprecated.</span></span> <span data-ttu-id="0aca5-221">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-222">Rimuove un listener per gli eventi in un nodo nell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-222">Removes a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aca5-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-224">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-224">This function is deprecated.</span></span> <span data-ttu-id="0aca5-225">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-226">Imposta lo stato attivo per l'input sull'elemento specificato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-226">Sets the input focus to the specified element in the UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aca5-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aca5-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="0aca5-228">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0aca5-228">This function is deprecated.</span></span> <span data-ttu-id="0aca5-229">Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0aca5-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aca5-230">Elimina un oggetto intervallo di testo allocato dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="0aca5-230">Deletes an allocated text range object from memory.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0aca5-231">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0aca5-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aca5-232">Client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0aca5-232">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

