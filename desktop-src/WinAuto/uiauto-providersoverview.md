---
title: Cenni preliminari sui provider di automazione interfaccia utente
description: Questo argomento fornisce una panoramica del modo in cui gli sviluppatori di controlli implementano i provider di automazione interfaccia utente.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automazione interfaccia utente, panoramica provider
- Automazione interfaccia utente, tipi di provider
- Automazione interfaccia utente, concetti relativi ai provider
- provider, informazioni
- provider, tipi
- provider, concetti
- provider, elementi
- provider, navigazione
- provider, viste
- provider, Framework
- provider, frammenti
- provider, host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955353"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="ede99-115">Cenni preliminari sui provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ede99-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="ede99-116">Un provider di automazione interfaccia utente Microsoft è un oggetto software che espone un elemento dell'interfaccia utente di un'applicazione in modo che le applicazioni client di accessibilità possano recuperare le informazioni sull'elemento e richiamarne la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ede99-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="ede99-117">In generale, ogni controllo o un altro elemento distinto in un'interfaccia utente dispone di un provider.</span><span class="sxs-lookup"><span data-stu-id="ede99-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="ede99-118">Microsoft include un provider per ognuno dei controlli standard forniti con Microsoft Win32, Windows Form e Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="ede99-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="ede99-119">Ciò significa che i controlli standard vengono esposti automaticamente ai client di automazione interfaccia utente; non è necessario implementare interfacce di accessibilità per i controlli standard.</span><span class="sxs-lookup"><span data-stu-id="ede99-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="ede99-120">Se l'applicazione include controlli personalizzati, è necessario implementare i provider di automazione interfaccia utente per tali controlli per renderli accessibili alle applicazioni client di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="ede99-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="ede99-121">È anche necessario implementare i provider per tutti i controlli di terze parti che non includono un provider.</span><span class="sxs-lookup"><span data-stu-id="ede99-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="ede99-122">È possibile implementare un provider implementando interfacce del provider di automazione interfaccia utente e interfacce del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="ede99-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="ede99-123">Questo argomento fornisce una panoramica del modo in cui gli sviluppatori di controlli implementano i provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ede99-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="ede99-124">Include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ede99-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="ede99-125">Tipi di provider</span><span class="sxs-lookup"><span data-stu-id="ede99-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="ede99-126">Concetti relativi al provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ede99-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   [<span data-ttu-id="ede99-127">Elementi</span><span class="sxs-lookup"><span data-stu-id="ede99-127">Elements</span></span>](#elements)
    -   [<span data-ttu-id="ede99-128">Framework</span><span class="sxs-lookup"><span data-stu-id="ede99-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="ede99-129">Frammenti</span><span class="sxs-lookup"><span data-stu-id="ede99-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="ede99-130">Host</span><span class="sxs-lookup"><span data-stu-id="ede99-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="ede99-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ede99-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="ede99-132">Tipi di provider</span><span class="sxs-lookup"><span data-stu-id="ede99-132">Types of Providers</span></span>

<span data-ttu-id="ede99-133">I provider di automazione interfaccia utente rientrano in due categorie: provider lato server e provider lato client (o *proxy*).</span><span class="sxs-lookup"><span data-stu-id="ede99-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="ede99-134">Un provider lato server è un oggetto, ad esempio un controllo personalizzato, che contiene la propria implementazione nativa delle interfacce del provider di automazione interfaccia utente pertinenti.</span><span class="sxs-lookup"><span data-stu-id="ede99-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="ede99-135">Un provider lato server comunica con le applicazioni client attraverso il limite di processo esponendo l'implementazione delle interfacce del provider al nucleo di automazione interfaccia utente, che consente di soddisfare le richieste dei client.</span><span class="sxs-lookup"><span data-stu-id="ede99-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="ede99-136">Per ulteriori informazioni sui provider lato server, vedere [implementazione di un provider di automazione interfaccia utente di Server-Side](uiauto-serversideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="ede99-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="ede99-137">Un provider lato client, o un proxy, è un oggetto che implementa le interfacce del provider di automazione interfaccia utente per conto di un controllo non include un'implementazione del provider completa autonomamente.</span><span class="sxs-lookup"><span data-stu-id="ede99-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="ede99-138">Senza un proxy, questo controllo è in gran parte opaco per l'automazione dell'interfaccia utente, che può fornire solo le informazioni di base disponibili dall'handle di finestra (**HWND**), ad esempio la posizione del controllo.</span><span class="sxs-lookup"><span data-stu-id="ede99-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="ede99-139">In genere, i provider proxy comunicano con l'applicazione attraverso il limite di processo inviando e ricevendo messaggi di Windows.</span><span class="sxs-lookup"><span data-stu-id="ede99-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="ede99-140">Per ulteriori informazioni, vedere [implementazione di un provider di automazione interfaccia utente Client-Side (proxy)](uiauto-clientsideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="ede99-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="ede99-141">Concetti relativi al provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ede99-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="ede99-142">In questa sezione viene presentata una breve spiegazione di alcuni concetti chiave fondamentali per l'implementazione di provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ede99-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="ede99-143">Elementi</span><span class="sxs-lookup"><span data-stu-id="ede99-143">Elements</span></span>

<span data-ttu-id="ede99-144">Gli elementi di automazione interfaccia utente sono parti dell'interfaccia utente, in genere finestre o controlli, visibili ai client di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ede99-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="ede99-145">ad esempio finestre delle applicazioni, riquadri, pulsanti, descrizioni comandi, caselle di riepilogo e voci di elenco.</span><span class="sxs-lookup"><span data-stu-id="ede99-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="ede99-146">Gli elementi di automazione interfaccia utente vengono esposti ai client sotto forma di albero.</span><span class="sxs-lookup"><span data-stu-id="ede99-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="ede99-147">L'automazione interfaccia utente costruisce l'albero passando da un elemento a un altro.</span><span class="sxs-lookup"><span data-stu-id="ede99-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="ede99-148">Lo spostamento viene abilitato dal provider per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="ede99-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="ede99-149">Ogni elemento può puntare al proprio elemento padre, ai relativi elementi di pari livello e ai relativi primi e ultimi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="ede99-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="ede99-150">Un client può vedere l'albero di automazione interfaccia utente in tre visualizzazioni principali, come descritto nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="ede99-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="ede99-151">Visualizzazione</span><span class="sxs-lookup"><span data-stu-id="ede99-151">View</span></span>         | <span data-ttu-id="ede99-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ede99-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="ede99-153">Visualizzazione non elaborata</span><span class="sxs-lookup"><span data-stu-id="ede99-153">Raw view</span></span>     | <span data-ttu-id="ede99-154">Include tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="ede99-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="ede99-155">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="ede99-155">Control view</span></span> | <span data-ttu-id="ede99-156">Include gli elementi che sono controlli.</span><span class="sxs-lookup"><span data-stu-id="ede99-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="ede99-157">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="ede99-157">Content view</span></span> | <span data-ttu-id="ede99-158">Include gli elementi di controllo che trasmettono informazioni all'utente.</span><span class="sxs-lookup"><span data-stu-id="ede99-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="ede99-159">È responsabilità dell'implementazione del provider definire un elemento come elemento contenuto o elemento controllo.</span><span class="sxs-lookup"><span data-stu-id="ede99-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="ede99-160">Gli elementi controllo possono essere anche elementi contenuto, mentre tutti gli elementi contenuto sono elementi controllo.</span><span class="sxs-lookup"><span data-stu-id="ede99-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="ede99-161">Per ulteriori informazioni sulla visualizzazione client dell'albero di, vedere [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ede99-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="ede99-162">Framework</span><span class="sxs-lookup"><span data-stu-id="ede99-162">Frameworks</span></span>

<span data-ttu-id="ede99-163">Un framework è un componente che gestisce controlli figlio, hit testing e rendering in un'area dello schermo.</span><span class="sxs-lookup"><span data-stu-id="ede99-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="ede99-164">Ad esempio, una finestra Win32, spesso denominata **HWND**, può fungere da Framework che contiene più elementi di automazione interfaccia utente, ad esempio una barra dei menu, una barra di stato e pulsanti.</span><span class="sxs-lookup"><span data-stu-id="ede99-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="ede99-165">I controlli contenitore Win32, ad esempio caselle di riepilogo e controlli visualizzazione albero, sono considerati Framework perché contengono il proprio codice per il rendering degli elementi figlio e l'esecuzione di hit testing su di essi.</span><span class="sxs-lookup"><span data-stu-id="ede99-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="ede99-166">Al contrario, una casella di riepilogo WPF non è un Framework, perché il rendering e l'hit testing sono gestiti dalla finestra che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="ede99-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="ede99-167">L'interfaccia utente di un'applicazione può essere costituita da Framework diversi.</span><span class="sxs-lookup"><span data-stu-id="ede99-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="ede99-168">Ad esempio, un **HWND** in un'applicazione potrebbe contenere codice HTML dinamico (DHTML) che a sua volta può contenere un componente, ad esempio una casella combinata in un **HWND**.</span><span class="sxs-lookup"><span data-stu-id="ede99-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="ede99-169">Frammenti</span><span class="sxs-lookup"><span data-stu-id="ede99-169">Fragments</span></span>

<span data-ttu-id="ede99-170">Un sottoalbero completo di elementi di un particolare Framework è denominato frammento.</span><span class="sxs-lookup"><span data-stu-id="ede99-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="ede99-171">L'elemento in corrispondenza del nodo radice del sottoalbero è definito radice del frammento.</span><span class="sxs-lookup"><span data-stu-id="ede99-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="ede99-172">Una radice del frammento non ha un elemento padre, ma è ospitata in un altro Framework, in genere una finestra Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="ede99-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="ede99-173">Hosts</span><span class="sxs-lookup"><span data-stu-id="ede99-173">Hosts</span></span>

<span data-ttu-id="ede99-174">Il nodo radice di ogni frammento deve essere ospitato in un elemento, in genere una finestra Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="ede99-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="ede99-175">L'eccezione è rappresentata dal desktop, che non è ospitato in nessun altro elemento.</span><span class="sxs-lookup"><span data-stu-id="ede99-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="ede99-176">L'host di un controllo personalizzato è **HWND** del controllo stesso, non la finestra dell'applicazione o qualsiasi altra finestra che potrebbe contenere gruppi di controlli di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ede99-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="ede99-177">L'host di un frammento svolge un ruolo importante nella fornitura dei servizi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ede99-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="ede99-178">Consente lo spostamento alla radice del frammento e rende disponibili alcune proprietà predefinite in modo che il provider personalizzato debba implementarle.</span><span class="sxs-lookup"><span data-stu-id="ede99-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ede99-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ede99-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ede99-180">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ede99-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ede99-181">Implementazione di un provider di automazione interfaccia utente Client-Side</span><span class="sxs-lookup"><span data-stu-id="ede99-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="ede99-182">Implementazione di un provider di automazione interfaccia utente Server-Side</span><span class="sxs-lookup"><span data-stu-id="ede99-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="ede99-183">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ede99-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




