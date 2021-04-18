---
title: Libreria di controlli Windows Ribbon Framework
description: Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione di Windows. I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espone la funzionalità del comando.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300236"
---
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="6b5c6-104">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="6b5c6-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="6b5c6-105">Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="6b5c6-106">I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espone la funzionalità del comando.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="6b5c6-107">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6b5c6-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="6b5c6-108">Controlli</span><span class="sxs-lookup"><span data-stu-id="6b5c6-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="6b5c6-109">Controlli di base</span><span class="sxs-lookup"><span data-stu-id="6b5c6-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="6b5c6-110">Controlli contenitore</span><span class="sxs-lookup"><span data-stu-id="6b5c6-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="6b5c6-111">Controlli specializzati</span><span class="sxs-lookup"><span data-stu-id="6b5c6-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="6b5c6-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b5c6-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="6b5c6-113">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6b5c6-113">Introduction</span></span>

<span data-ttu-id="6b5c6-114">Il Framework della barra multifunzione è costituito da componenti come [schede](windowsribbon-controls-tab.md) e dalla [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md), che interagiscono per offrire un'interfaccia utente avanzata.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="6b5c6-115">Singolarmente, questi componenti espongono tipi diversi di comandi per offrire ai clienti un'esperienza organizzata e prevedibile per tutte le applicazioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="6b5c6-116">Ogni scheda, ad esempio, espone i comandi correlati alla creazione e all'esecuzione di parti specifiche del contenuto all'interno dell'area di lavoro dell'applicazione, mentre il [menu applicazione](windowsribbon-controls-applicationmenu.md) espone funzionalità correlate a un progetto completo, ad esempio un intero documento, immagine o film.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="6b5c6-117">In questo argomento viene fornito un elenco completo dei controlli della barra multifunzione e viene inclusa una breve descrizione di ogni controllo, con collegamenti a una documentazione più dettagliata, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="6b5c6-118">Controlli</span><span class="sxs-lookup"><span data-stu-id="6b5c6-118">The Controls</span></span>

<span data-ttu-id="6b5c6-119">Il Framework della barra multifunzione è costituito da due [visualizzazioni](windowsribbon-reference-elements-view.md): la visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) e la visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="6b5c6-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="6b5c6-120">Ogni vista può ospitare diversi componenti che fungono da contenitori di presentazione per tutti i controlli sottoposti a rendering e gestiti dal Framework.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="6b5c6-121">La visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) ospita l'elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , l'elemento [**QuickAccessToolBar**](windowsribbon-element-quickaccesstoolbar.md) e la barra dei comandi della barra multifunzione mentre la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) ospita un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) o entrambi.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="6b5c6-122">Ogni controllo Framework è distinto dalla funzionalità associata al relativo [**tipo di comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span><span class="sxs-lookup"><span data-stu-id="6b5c6-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="6b5c6-123">Controlli di base</span><span class="sxs-lookup"><span data-stu-id="6b5c6-123">Basic Controls</span></span>

<span data-ttu-id="6b5c6-124">I controlli di base sono costituiti da uno o più pulsanti che possono essere richiamati con un solo clic del mouse per eseguire un'azione semplice.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="6b5c6-125">La [**casella**](windowsribbon-element-spinner.md) di selezione è un'eccezione perché contiene un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="6b5c6-126">Nella tabella seguente sono elencati i controlli di base del Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="6b5c6-127">Control</span><span class="sxs-lookup"><span data-stu-id="6b5c6-127">Control</span></span>                                                  | <span data-ttu-id="6b5c6-128">Elemento markup</span><span class="sxs-lookup"><span data-stu-id="6b5c6-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="6b5c6-129">Button</span><span class="sxs-lookup"><span data-stu-id="6b5c6-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="6b5c6-130">**Pulsante**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="6b5c6-131">Casella di controllo</span><span class="sxs-lookup"><span data-stu-id="6b5c6-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="6b5c6-132">**Casella**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="6b5c6-133">Pulsante della Guida</span><span class="sxs-lookup"><span data-stu-id="6b5c6-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="6b5c6-134">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="6b5c6-135">Spinner</span><span class="sxs-lookup"><span data-stu-id="6b5c6-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="6b5c6-136">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="6b5c6-137">Interruttore</span><span class="sxs-lookup"><span data-stu-id="6b5c6-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="6b5c6-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="6b5c6-139">Controlli contenitore</span><span class="sxs-lookup"><span data-stu-id="6b5c6-139">Container Controls</span></span>

<span data-ttu-id="6b5c6-140">I controlli contenitore sono costituiti da gruppi di controlli, menu, elenchi o raccolte di elementi e comandi.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="6b5c6-141">Il Framework distingue tra due tipi di contenitori, statici e dinamici.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="6b5c6-142">Contenitori statici</span><span class="sxs-lookup"><span data-stu-id="6b5c6-142">Static Containers</span></span>

<span data-ttu-id="6b5c6-143">I contenitori statici vengono dichiarati e popolati, insieme a tutte le risorse associate, nel file di markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="6b5c6-144">Questi controlli non possono essere modificati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="6b5c6-145">I vantaggi dei controlli statici includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b5c6-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="6b5c6-146">Prototipazione rapida.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-146">Rapid prototyping.</span></span> <span data-ttu-id="6b5c6-147">I controlli statici consentono di creare rapidamente una barra multifunzione che simula la creazione di una struttura della barra multifunzione finale che non richiede codice complesso.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="6b5c6-148">Modifiche semplici.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-148">Easy modifications.</span></span> <span data-ttu-id="6b5c6-149">La maggior parte degli elementi, degli attributi, delle risorse e dei layout dei controlli statici può essere modificata nel markup.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="6b5c6-150">Interfaccia utente coerente.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-150">Consistent UI.</span></span> <span data-ttu-id="6b5c6-151">Le applicazioni ben progettate forniscono un'interfaccia utente coerente e stabile che evita modifiche a menu ed elenchi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="6b5c6-152">La tabella seguente descrive i controlli contenitore statici nel framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="6b5c6-153">Control</span><span class="sxs-lookup"><span data-stu-id="6b5c6-153">Control</span></span>                                                        | <span data-ttu-id="6b5c6-154">Elemento markup</span><span class="sxs-lookup"><span data-stu-id="6b5c6-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="6b5c6-155">Menu applicazione</span><span class="sxs-lookup"><span data-stu-id="6b5c6-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="6b5c6-156">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="6b5c6-157">Popup contesto</span><span class="sxs-lookup"><span data-stu-id="6b5c6-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="6b5c6-158">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="6b5c6-159">Pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="6b5c6-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="6b5c6-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="6b5c6-161">Gruppo</span><span class="sxs-lookup"><span data-stu-id="6b5c6-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="6b5c6-162">**Group**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="6b5c6-163">Gruppo di menu</span><span class="sxs-lookup"><span data-stu-id="6b5c6-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="6b5c6-164">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="6b5c6-165">Pulsante di divisione</span><span class="sxs-lookup"><span data-stu-id="6b5c6-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="6b5c6-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="6b5c6-167">TAB</span><span class="sxs-lookup"><span data-stu-id="6b5c6-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="6b5c6-168">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="6b5c6-169">Gruppo di schede</span><span class="sxs-lookup"><span data-stu-id="6b5c6-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="6b5c6-170">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="6b5c6-171">Contenitori dinamici</span><span class="sxs-lookup"><span data-stu-id="6b5c6-171">Dynamic Containers</span></span>

<span data-ttu-id="6b5c6-172">I contenitori dinamici sono dichiarati nel file di markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="6b5c6-173">Presentano un gruppo di elementi o comandi creati o modificati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="6b5c6-174">Una sottoclasse di contenitori dinamici, detti raccolte, si distingue dalla relativa implementazione dell'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="6b5c6-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="6b5c6-175">Questa interfaccia consente a un controllo di esporre l'elenco di elementi o comandi come una raccolta e di supportare gli aggiornamenti in base all'interazione dell'utente e alle condizioni di run-time.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="6b5c6-176">Per ulteriori informazioni, vedere [utilizzo delle raccolte](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="6b5c6-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="6b5c6-177">Nella tabella seguente sono elencati i controlli contenitore dinamici nel framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="6b5c6-178">Control</span><span class="sxs-lookup"><span data-stu-id="6b5c6-178">Control</span></span>                                                               | <span data-ttu-id="6b5c6-179">Elemento markup</span><span class="sxs-lookup"><span data-stu-id="6b5c6-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="6b5c6-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="6b5c6-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="6b5c6-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="6b5c6-182">Raccolta a discesa</span><span class="sxs-lookup"><span data-stu-id="6b5c6-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="6b5c6-183">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="6b5c6-184">Raccolta della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="6b5c6-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="6b5c6-185">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="6b5c6-186">Barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="6b5c6-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="6b5c6-187">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="6b5c6-188">Elementi recenti</span><span class="sxs-lookup"><span data-stu-id="6b5c6-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="6b5c6-189">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="6b5c6-190">Raccolta di pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="6b5c6-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="6b5c6-191">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="6b5c6-192">Controlli specializzati</span><span class="sxs-lookup"><span data-stu-id="6b5c6-192">Specialized Controls</span></span>

<span data-ttu-id="6b5c6-193">Il Framework della barra multifunzione contiene una serie di controlli specializzati per funzionalità specifiche dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="6b5c6-194">Nella tabella seguente sono elencati i controlli specializzati del Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b5c6-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="6b5c6-195">Control</span><span class="sxs-lookup"><span data-stu-id="6b5c6-195">Control</span></span>                                                                  | <span data-ttu-id="6b5c6-196">Elemento markup</span><span class="sxs-lookup"><span data-stu-id="6b5c6-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="6b5c6-197">Selezione colori a discesa</span><span class="sxs-lookup"><span data-stu-id="6b5c6-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="6b5c6-198">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="6b5c6-199">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="6b5c6-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="6b5c6-200">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="6b5c6-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="6b5c6-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b5c6-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5c6-202">Informazioni sui comandi e sui controlli</span><span class="sxs-lookup"><span data-stu-id="6b5c6-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 