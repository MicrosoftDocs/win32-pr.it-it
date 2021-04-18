---
title: Cenni preliminari su automazione interfaccia utente
description: Automazione interfaccia utente Microsoft è un Framework di accessibilità per Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automazione interfaccia utente, informazioni
- Automazione interfaccia utente, accessibilità
- Automazione interfaccia utente, componenti
- Automazione interfaccia utente, API provider
- Automazione interfaccia utente, API client
- Automazione interfaccia utente, file di intestazione
- Automazione interfaccia utente, modello
- components
- accessibilità
- API provider
- API client
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398519"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="09453-115">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-115">UI Automation Overview</span></span>

<span data-ttu-id="09453-116">Automazione interfaccia utente Microsoft è un Framework di accessibilità per Windows.</span><span class="sxs-lookup"><span data-stu-id="09453-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="09453-117">Consente l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop.</span><span class="sxs-lookup"><span data-stu-id="09453-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="09453-118">Consente ai prodotti di Assistive Technology, quali utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard.</span><span class="sxs-lookup"><span data-stu-id="09453-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="09453-119">Automazione interfaccia utente consente inoltre l'interazione degli script di test automatizzati con l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="09453-120">Automazione interfaccia utente era disponibile per la prima volta in Windows XP come parte del Framework Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="09453-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="09453-121">Anche se in quel momento è stata pubblicata anche un'API C++ non gestita, l'utilità delle funzioni client era limitata a causa di problemi di interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="09453-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="09453-122">Per Windows 7, l'API è stata riscritta nell'Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="09453-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="09453-123">Sebbene le funzioni della libreria introdotte nella versione precedente dell'automazione dell'interfaccia utente siano ancora documentate, non devono essere utilizzate nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="09453-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="09453-124">Le applicazioni client di automazione interfaccia utente possono essere scritte con la garanzia che funzioneranno su più framework di controllo di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="09453-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="09453-125">Il nucleo di automazione interfaccia utente maschera le eventuali differenze nei framework sottostanti le varie parti dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="09453-126">Ad esempio, la proprietà **Content** di un pulsante Windows Presentation Foundation (WPF), la proprietà **Caption** di un pulsante Microsoft Win32 e la proprietà **ALT** di un'immagine HTML sono tutte mappate a una singola proprietà, **Name**, nella visualizzazione di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="09453-127">Automazione interfaccia utente offre funzionalità complete nei sistemi operativi Windows XP, Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09453-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="09453-128">I provider di automazione interfaccia utente sono componenti che implementano il supporto di automazione interfaccia utente sui controlli e offrono supporto per le applicazioni client Microsoft Active Accessibility, tramite un servizio di bridging incorporato.</span><span class="sxs-lookup"><span data-stu-id="09453-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="09453-129">Automazione interfaccia utente non Abilita la comunicazione tra processi avviati da utenti diversi tramite il comando **Esegui come** .</span><span class="sxs-lookup"><span data-stu-id="09453-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="09453-130">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="09453-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="09453-131">Componenti di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="09453-132">File di intestazione di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="09453-133">Modello di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="09453-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09453-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="09453-135">Componenti di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-135">UI Automation Components</span></span>

<span data-ttu-id="09453-136">Automazione interfaccia utente dispone di quattro componenti principali, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="09453-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09453-137">Componente</span><span class="sxs-lookup"><span data-stu-id="09453-137">Component</span></span></th>
<th><span data-ttu-id="09453-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09453-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09453-139">API provider</span><span class="sxs-lookup"><span data-stu-id="09453-139">Provider API</span></span></td>
<td><span data-ttu-id="09453-140">Set di interfacce COM implementate dai provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="09453-141">I provider di automazione interfaccia utente sono oggetti che forniscono informazioni sugli elementi dell'interfaccia utente e rispondono a input a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="09453-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09453-142">API client</span><span class="sxs-lookup"><span data-stu-id="09453-142">Client API</span></span></td>
<td><span data-ttu-id="09453-143">Set di interfacce COM che consentono alle applicazioni client di ottenere informazioni sull'interfaccia utente e di inviare input ai controlli.</span><span class="sxs-lookup"><span data-stu-id="09453-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="09453-144">Le funzioni descritte in <a href="uiauto-entry-cpfunctions.md">funzioni del pattern di controllo deprecate</a> e <a href="uiauto-entry-uianodefunctions.md">funzioni di nodo deprecate</a> sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="09453-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="09453-145">Al contrario, le applicazioni client devono usare le interfacce COM di automazione interfaccia utente descritte nelle <a href="uiauto-entry-uiautoclientinterfaces.md">interfacce degli elementi di automazione interfaccia utente per i client</a>.</span><span class="sxs-lookup"><span data-stu-id="09453-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09453-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="09453-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="09453-147">La libreria di runtime, talvolta denominata Core di automazione interfaccia utente, che gestisce la comunicazione tra provider e client.</span><span class="sxs-lookup"><span data-stu-id="09453-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09453-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="09453-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="09453-149">La libreria di runtime per Microsoft Active Accessibility e gli oggetti proxy.</span><span class="sxs-lookup"><span data-stu-id="09453-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="09453-150">La libreria fornisce anche oggetti proxy usati da Microsoft Microsoft Active Accessibility al proxy di automazione interfaccia utente per supportare i controlli Win32.</span><span class="sxs-lookup"><span data-stu-id="09453-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="09453-151">Esistono due modi per usare l'automazione dell'interfaccia utente: per creare il supporto per i controlli personalizzati tramite l'API del provider e per creare applicazioni client che usano il core di automazione interfaccia utente per comunicare e recuperare informazioni sugli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="09453-152">In base allo stato attivo, è necessario fare riferimento a parti diverse della documentazione.</span><span class="sxs-lookup"><span data-stu-id="09453-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="09453-153">Se è necessario creare supporto per i controlli personalizzati, vedere [la guida per programmatori del provider di automazione interfaccia utente](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="09453-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="09453-154">Se è necessario comunicare con o recuperare informazioni sugli elementi dell'interfaccia utente, vedere [Guida per programmatori client di automazione interfaccia utente](uiauto-clientportal.md).</span><span class="sxs-lookup"><span data-stu-id="09453-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="09453-155">File di intestazione di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-155">UI Automation Header Files</span></span>

<span data-ttu-id="09453-156">L'API di automazione interfaccia utente è definita in diversi file di intestazione C/C++ inclusi in Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="09453-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="09453-157">I file di intestazione di automazione interfaccia utente sono descritti nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="09453-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="09453-158">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="09453-158">Header file</span></span>           | <span data-ttu-id="09453-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09453-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09453-160">UIAutomationClient. h</span><span class="sxs-lookup"><span data-stu-id="09453-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="09453-161">Definisce le interfacce e gli elementi di programmazione correlati utilizzati dai client di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="09453-162">UIAutomationCore. h</span><span class="sxs-lookup"><span data-stu-id="09453-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="09453-163">Definisce le interfacce e gli elementi di programmazione correlati utilizzati dai provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="09453-164">UIAutomationCoreApi. h</span><span class="sxs-lookup"><span data-stu-id="09453-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="09453-165">Definisce le costanti generali, i GUID, i tipi di dati e le strutture usati dai provider e dai client di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="09453-166">Contiene inoltre le definizioni per le funzioni deprecate node e pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="09453-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="09453-167">UIAutomation. h</span><span class="sxs-lookup"><span data-stu-id="09453-167">UIAutomation.h</span></span>        | <span data-ttu-id="09453-168">Include tutti gli altri file di intestazione di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="09453-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="09453-169">Poiché la maggior parte delle applicazioni di automazione interfaccia utente richiede elementi di tutti i file di intestazione di automazione interfaccia utente, è preferibile includere UIAutomation. h nei progetti dell'applicazione di automazione interfaccia utente anziché includere ogni singolo file.</span><span class="sxs-lookup"><span data-stu-id="09453-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="09453-170">Se si sviluppa un'applicazione che usa l'API di automazione interfaccia utente, è necessario includere UIAutomation. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="09453-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="09453-171">Se l'applicazione supporta Microsoft Active Accessibility, includere il file di intestazione oleacc. h.</span><span class="sxs-lookup"><span data-stu-id="09453-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="09453-172">Anche le applicazioni di automazione interfaccia utente che usano GUID richiedono il file di intestazione INITGUID. h.</span><span class="sxs-lookup"><span data-stu-id="09453-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="09453-173">Se necessario, è necessario includere Initguid. h prima di UIAutomation. h.</span><span class="sxs-lookup"><span data-stu-id="09453-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="09453-174">Modello di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-174">UI Automation Model</span></span>

<span data-ttu-id="09453-175">Automazione interfaccia utente espone ogni elemento dell'interfaccia utente alle applicazioni client come oggetto rappresentato dall'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) .</span><span class="sxs-lookup"><span data-stu-id="09453-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="09453-176">Gli elementi sono contenuti in una struttura ad albero, con il desktop come elemento radice.</span><span class="sxs-lookup"><span data-stu-id="09453-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="09453-177">I client possono filtrare la visualizzazione non elaborata della struttura ad albero come visualizzazione controlli o visualizzazione contenuto.</span><span class="sxs-lookup"><span data-stu-id="09453-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="09453-178">Queste visualizzazioni standard della struttura possono essere facilmente visualizzate usando l'applicazione di [ispezione](inspect-objects.md) inclusa nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="09453-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="09453-179">Le applicazioni possono inoltre creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="09453-179">Applications can also create custom views.</span></span>

<span data-ttu-id="09453-180">Un elemento di automazione interfaccia utente espone le proprietà del controllo o dell'elemento dell'interfaccia utente che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="09453-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="09453-181">Una di queste proprietà è il tipo di controllo, che definisce l'aspetto e la funzionalità di base del controllo o dell'elemento dell'interfaccia utente come un'unica entità riconoscibile, ad esempio un pulsante o una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="09453-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="09453-182">Per altre informazioni sui tipi di controllo, vedere [UI Automation Control types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="09453-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="09453-183">Inoltre, un elemento di automazione interfaccia utente espone uno o più pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="09453-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="09453-184">Un pattern di controllo fornisce un set di proprietà specifiche di un particolare tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="09453-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="09453-185">Un pattern di controllo espone anche metodi che consentono alle applicazioni client di ottenere altre informazioni sull'elemento e di fornire input all'elemento.</span><span class="sxs-lookup"><span data-stu-id="09453-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="09453-186">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="09453-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="09453-187">Non esiste una corrispondenza uno-a-uno tra tipi di controllo e pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="09453-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="09453-188">Un pattern di controllo può essere supportato da più tipi di controllo e un controllo può supportare più pattern di controllo, ognuno dei quali espone aspetti diversi del comportamento.</span><span class="sxs-lookup"><span data-stu-id="09453-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="09453-189">Ad esempio, una casella combinata dispone di almeno due pattern di controllo: uno che rappresenta la possibilità di espansione e compressione e un altro che rappresenta il meccanismo di selezione.</span><span class="sxs-lookup"><span data-stu-id="09453-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="09453-190">Tuttavia, un controllo può presentare un solo tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="09453-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="09453-191">Automazione interfaccia utente fornisce informazioni alle applicazioni client tramite gli eventi.</span><span class="sxs-lookup"><span data-stu-id="09453-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="09453-192">A differenza di WinEvents, gli eventi di automazione interfaccia utente non sono basati su un meccanismo di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="09453-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="09453-193">I client di automazione interfaccia utente si registrano per le notifiche di eventi specifici e possono richiedere che le proprietà specifiche e le informazioni sui pattern di controllo vengano passate ai gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="09453-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="09453-194">Inoltre, un evento di automazione interfaccia utente contiene un riferimento all'elemento che lo ha generato.</span><span class="sxs-lookup"><span data-stu-id="09453-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="09453-195">I provider possono migliorare le prestazioni generando eventi in modo selettivo, a seconda dei client in ascolto.</span><span class="sxs-lookup"><span data-stu-id="09453-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="09453-196">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="09453-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09453-197">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09453-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="09453-198">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="09453-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="09453-199">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="09453-200">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="09453-201">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="09453-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





