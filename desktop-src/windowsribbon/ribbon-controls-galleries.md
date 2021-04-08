---
title: Uso delle raccolte
description: Il Framework della barra multifunzione di Windows offre agli sviluppatori un modello affidabile e coerente per la gestione di contenuto dinamico in diversi controlli basati su raccolte.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Barra multifunzione di Windows, raccolte
- Barra multifunzione, raccolte
- Barra multifunzione di Windows, controllo DropDownGallery
- Barra multifunzione, controllo DropDownGallery
- Barra multifunzione di Windows, controllo SplitButtonGallery
- Barra multifunzione, controllo SplitButtonGallery
- Controllo DropDownGallery
- Controllo SplitButtonGallery
- raccolte per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729231"
---
# <a name="working-with-galleries"></a><span data-ttu-id="f0dc3-112">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="f0dc3-112">Working with Galleries</span></span>

<span data-ttu-id="f0dc3-113">Il Framework della barra multifunzione di Windows offre agli sviluppatori un modello affidabile e coerente per la gestione di contenuto dinamico in diversi controlli basati su raccolte.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="f0dc3-114">Grazie all'adattamento e alla riconfigurazione dell'interfaccia utente della barra multifunzione, questi controlli dinamici consentono al Framework di rispondere all'interazione dell'utente sia nell'applicazione host che nella barra multifunzione e offrono la flessibilità necessaria per gestire diversi ambienti di Runtime.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="f0dc3-115">Introduzione</span><span class="sxs-lookup"><span data-stu-id="f0dc3-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f0dc3-116">Raccolte</span><span class="sxs-lookup"><span data-stu-id="f0dc3-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="f0dc3-117">Raccolte di elementi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="f0dc3-118">Raccolte comandi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="f0dc3-119">Controlli della raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="f0dc3-120">Come implementare una raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="f0dc3-121">Componenti di base</span><span class="sxs-lookup"><span data-stu-id="f0dc3-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="f0dc3-122">Dichiarare i controlli nel markup</span><span class="sxs-lookup"><span data-stu-id="f0dc3-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="f0dc3-123">Creazione di un gestore di comandi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="f0dc3-124">Associare il gestore di comandi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="f0dc3-125">Inizializzare una raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="f0dc3-126">Gestisci eventi raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="f0dc3-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0dc3-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f0dc3-128">Introduzione</span><span class="sxs-lookup"><span data-stu-id="f0dc3-128">Introduction</span></span>

<span data-ttu-id="f0dc3-129">Questa capacità del Framework della barra multifunzione di adattarsi dinamicamente alle condizioni di runtime, ai requisiti delle applicazioni e all'input dell'utente finale evidenzia le funzionalità avanzate dell'interfaccia utente del Framework e offre agli sviluppatori la flessibilità necessaria per soddisfare un'ampia gamma di esigenze dei clienti.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="f0dc3-130">Questa guida descrive i controlli della raccolta dinamica supportati dal Framework, ne spiega le differenze, discute quando e dove possono essere usati meglio e illustra come possono essere incorporati in un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="f0dc3-131">Raccolte</span><span class="sxs-lookup"><span data-stu-id="f0dc3-131">Galleries</span></span>

<span data-ttu-id="f0dc3-132">Le raccolte sono controlli casella di riepilogo funzionalmente e graficamente avanzati.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="f0dc3-133">La raccolta di elementi di una raccolta può essere organizzata in base a categorie, visualizzate in layout flessibili basati su righe e colonne, rappresentate con immagini e testo e a seconda del tipo di raccolta, supporta l'anteprima in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="f0dc3-134">Le raccolte sono separate dal punto di vista funzionale da altri controlli della barra multifunzione dinamici per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0dc3-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="f0dc3-135">Le raccolte implementano l'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) che definisce i vari metodi per la modifica delle raccolte di elementi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="f0dc3-136">Le raccolte possono essere aggiornate in fase di esecuzione, in base alle attività che si verificano direttamente nella barra multifunzione, ad esempio quando un utente aggiunge un comando alla barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="f0dc3-137">Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica indirettamente dall'ambiente di runtime, ad esempio quando un driver della stampante supporta solo layout di pagine verticale.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="f0dc3-138">Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica indirettamente nell'applicazione host, ad esempio quando un utente seleziona un elemento in un documento.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="f0dc3-139">Il Framework della barra multifunzione espone due tipi di raccolte: raccolte di elementi e raccolte di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="f0dc3-140">Raccolte di elementi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-140">Item Galleries</span></span>

<span data-ttu-id="f0dc3-141">Le raccolte di elementi contengono una raccolta basata su indici di elementi correlati in cui ogni elemento è rappresentato da un'immagine, da una stringa o da entrambi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="f0dc3-142">Il controllo è associato a un singolo gestore di comando che si basa sul valore di indice identificato dalla proprietà [ \_ \_ SelectedItem pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-selecteditem.md) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="f0dc3-143">Le raccolte di elementi supportano l'anteprima in tempo reale, ovvero la visualizzazione del risultato di un comando, in base al passaggio del mouse o allo stato attivo, senza eseguire il commit o richiamare effettivamente il comando.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0dc3-144">Il Framework non supporta l'hosting di raccolte di elementi nel menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="f0dc3-145">Raccolte comandi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-145">Command Galleries</span></span>

<span data-ttu-id="f0dc3-146">Le raccolte di comandi contengono una raccolta di elementi distinti e non indicizzati.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="f0dc3-147">Ogni elemento è rappresentato da un singolo controllo associato a un gestore di comandi tramite un ID di comando.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="f0dc3-148">Analogamente ai controlli autonomi, ogni elemento in una raccolta di comandi indirizza gli eventi di input a un gestore di comandi associato: la raccolta di comandi non è in ascolto degli eventi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="f0dc3-149">Le raccolte comandi non supportano l'anteprima in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="f0dc3-150">Controlli della raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-150">Gallery Controls</span></span>

<span data-ttu-id="f0dc3-151">Sono disponibili quattro controlli della raccolta nel framework della barra multifunzione: [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md)e [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="f0dc3-152">All eccetto **ComboBox** può essere implementato come raccolta di elementi o come raccolta di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="f0dc3-153">DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="f0dc3-153">DropDownGallery</span></span>

<span data-ttu-id="f0dc3-154">Un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) è un pulsante che visualizza un elenco a discesa che contiene una raccolta di elementi o comandi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="f0dc3-155">Lo screenshot seguente illustra il controllo raccolta a [discesa](windowsribbon-controls-dropdowngallery.md) della barra multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo raccolta a discesa in Microsoft Paint per Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="f0dc3-157">SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="f0dc3-157">SplitButtonGallery</span></span>

<span data-ttu-id="f0dc3-158">Un [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) è un controllo composito che espone un singolo elemento o comando predefinito dalla raccolta in un pulsante principale e visualizza altri elementi o comandi in un elenco a discesa che viene escluso a vicenda quando si fa clic su un pulsante secondario.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="f0dc3-159">Lo screenshot seguente illustra il controllo raccolta dei [pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md) della barra multifunzione in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo raccolta di pulsanti di suddivisione in Microsoft Paint per Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="f0dc3-161">Inribbongallery</span><span class="sxs-lookup"><span data-stu-id="f0dc3-161">InRibbonGallery</span></span>

<span data-ttu-id="f0dc3-162">Un [**inribbongallery**](windowsribbon-element-inribbongallery.md) è una raccolta che visualizza una raccolta di elementi o comandi correlati nella barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="f0dc3-163">Se la raccolta contiene troppi elementi, viene fornita una freccia di espansione per visualizzare il resto della raccolta in un riquadro espanso.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="f0dc3-164">Lo screenshot seguente illustra il controllo della raccolta della barra [multifunzione](windowsribbon-controls-inribbongallery.md) in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot di un controllo della raccolta nella barra multifunzione nella barra multifunzione di Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="f0dc3-166">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f0dc3-166">ComboBox</span></span>

<span data-ttu-id="f0dc3-167">[**ComboBox**](windowsribbon-element-combobox.md) è una casella di riepilogo a colonna singola che contiene una raccolta di elementi con un controllo statico o un controllo di modifica e una freccia a discesa.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="f0dc3-168">La parte della casella di riepilogo del controllo viene visualizzata quando l'utente fa clic sulla freccia a discesa.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="f0dc3-169">Lo screenshot seguente illustra un controllo [casella combinata](windowsribbon-controls-combobox.md) della barra multifunzione di Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![Screenshot di un controllo ComboBox sulla barra multifunzione di Microsoft Paint.](images/controls/combobox.png)

<span data-ttu-id="f0dc3-171">Poiché [**ComboBox**](windowsribbon-element-combobox.md) è esclusivamente una raccolta di elementi, non supporta gli elementi di comando.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="f0dc3-172">È anche l'unico controllo raccolta che non supporta uno spazio dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="f0dc3-173">Uno spazio di comando è una raccolta di comandi dichiarati nel markup ed elencati nella parte inferiore di una raccolta di elementi o di una raccolta di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="f0dc3-174">Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare uno spazio dei comandi a tre pulsanti in un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="f0dc3-175">Lo screenshot seguente illustra lo spazio dei comandi a tre pulsanti dell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![Screenshot di uno spazio dei comandi a tre pulsanti in un dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="f0dc3-177">Come implementare una raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-177">How to Implement a Gallery</span></span>

<span data-ttu-id="f0dc3-178">In questa sezione vengono illustrati i dettagli di implementazione delle raccolte della barra multifunzione e viene illustrato come incorporarli in un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="f0dc3-179">Componenti di base</span><span class="sxs-lookup"><span data-stu-id="f0dc3-179">The Basic Components</span></span>

<span data-ttu-id="f0dc3-180">In questa sezione viene descritto il set di proprietà e metodi che costituiscono la struttura di contenuto dinamico nel framework della barra multifunzione e il supporto per l'aggiunta, l'eliminazione, l'aggiornamento e la modifica del contenuto e il layout visivo delle raccolte della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="f0dc3-181">IUICollection</span><span class="sxs-lookup"><span data-stu-id="f0dc3-181">IUICollection</span></span>

<span data-ttu-id="f0dc3-182">Le raccolte richiedono un set di base di metodi per accedere e modificare i singoli elementi nelle raccolte.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="f0dc3-183">L'interfaccia [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) definisce questi metodi e il Framework integra le funzionalità con metodi aggiuntivi definiti nell'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="f0dc3-184">**IUICollection** viene implementato dal Framework per ogni dichiarazione della raccolta nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="f0dc3-185">Se è necessaria una funzionalità aggiuntiva non fornita dall'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , è possibile sostituire un oggetto raccolta personalizzato implementato dall'applicazione host e derivato da [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) per la raccolta di Framework.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="f0dc3-186">IUICollectionChangedEvent</span><span class="sxs-lookup"><span data-stu-id="f0dc3-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="f0dc3-187">Affinché un'applicazione risponda alle modifiche in una raccolta di raccolta, deve implementare l'interfaccia [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="f0dc3-188">Le applicazioni possono sottoscrivere le notifiche da un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite il listener di eventi [**IUICollectionChangedEvent:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="f0dc3-189">Quando l'applicazione sostituisce la raccolta di raccolta fornita dal Framework con una raccolta personalizzata, l'applicazione deve implementare l'interfaccia [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="f0dc3-190">Se [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) non è implementato, l'applicazione non è in grado di notificare al Framework le modifiche apportate alla raccolta personalizzata che richiedono aggiornamenti dinamici per il controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="f0dc3-191">Nei casi in cui [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) non è implementato, il controllo raccolta può essere aggiornato solo tramite invalidazione tramite [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) e [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)oppure chiamando [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="f0dc3-192">IUISimplePropertySet</span><span class="sxs-lookup"><span data-stu-id="f0dc3-192">IUISimplePropertySet</span></span>

<span data-ttu-id="f0dc3-193">Le applicazioni devono implementare IUISimplePropertySet per ogni elemento o comando in una raccolta di raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="f0dc3-194">Tuttavia, le proprietà che possono essere richieste con [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) variano.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="f0dc3-195">Gli elementi vengono definiti e associati a una raccolta tramite la chiave della proprietà [ \_ \_ ItemsSource dell'interfaccia utente pkey](windowsribbon-reference-properties-uipkey-itemssource.md) ed espongono le proprietà con un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="f0dc3-196">Nella tabella seguente sono descritte le proprietà valide per gli elementi nelle raccolte di elementi ([**\_ \_ raccolta COMMANDTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="f0dc3-197">Alcune proprietà dell'elemento, ad esempio l' [ \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md), possono essere definite nel markup.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="f0dc3-198">Per informazioni dettagliate, vedere la documentazione di riferimento per le [chiavi di proprietà](windowsribbon-reference-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="f0dc3-199">Control</span><span class="sxs-lookup"><span data-stu-id="f0dc3-199">Control</span></span>

<span data-ttu-id="f0dc3-200">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0dc3-200">Properties</span></span>

[<span data-ttu-id="f0dc3-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="f0dc3-202">[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="f0dc3-203">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="f0dc3-204">[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="f0dc3-205">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="f0dc3-206">[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="f0dc3-207">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="f0dc3-208">[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="f0dc3-209">[Interfaccia utente \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) è una proprietà della raccolta di elementi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="f0dc3-210">Nella tabella seguente sono descritte le proprietà degli elementi valide per le raccolte di comandi ([**UI \_ COMMANDTYPE \_ CommandCollection**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="f0dc3-211">Control</span><span class="sxs-lookup"><span data-stu-id="f0dc3-211">Control</span></span>                                                                | <span data-ttu-id="f0dc3-212">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0dc3-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0dc3-213">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="f0dc3-214">[Interfaccia utente \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="f0dc3-215">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="f0dc3-216">[Interfaccia utente \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="f0dc3-217">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="f0dc3-218">[Interfaccia utente \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="f0dc3-219">Le categorie vengono usate per organizzare gli elementi e i comandi nelle raccolte.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="f0dc3-220">Le categorie vengono definite e associate a una raccolta tramite la chiave della proprietà [ \_ \_ categorie pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-categories.md) ed espongono le proprietà con un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) specifico per la categoria.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="f0dc3-221">Le categorie non hanno un CommandType e non supportano l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="f0dc3-222">Le categorie, ad esempio, non possono diventare SelectedItem in una raccolta di elementi e non sono associate a un comando in una raccolta di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="f0dc3-223">Analogamente ad altre proprietà degli elementi della raccolta, è possibile recuperare le proprietà di categoria, ad esempio [UI \_ pkey \_ Label](windowsribbon-reference-properties-uipkey-label.md) e [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) , chiamando [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0dc3-224">[**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) deve restituire [**la \_ raccolta \_ di interfaccia utente INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) quando è richiesto l' [interfaccia utente \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) per un elemento a cui non è associata una categoria.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="f0dc3-225">Dichiarare i controlli nel markup</span><span class="sxs-lookup"><span data-stu-id="f0dc3-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="f0dc3-226">Le raccolte, come tutti i controlli della barra multifunzione, devono essere dichiarate nel markup.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="f0dc3-227">Una raccolta viene identificata nel markup come raccolta di elementi o raccolta di comandi e vengono dichiarati diversi dettagli di presentazione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="f0dc3-228">A differenza di altri controlli, le raccolte richiedono che il controllo di base o il contenitore della raccolta vengano dichiarati nel markup.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="f0dc3-229">Le raccolte effettive vengono popolate in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="f0dc3-230">Quando una raccolta viene dichiarata nel markup, l'attributo *Type* viene usato per specificare se la raccolta è una raccolta di elementi di una raccolta di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="f0dc3-231">Sono disponibili diversi attributi di layout facoltativi per ognuno dei controlli descritti qui.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="f0dc3-232">Questi attributi forniscono preferenze per gli sviluppatori per il Framework da seguire che influiscono direttamente sulla modalità di popolamento e visualizzazione di un controllo in una barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="f0dc3-233">Le preferenze applicabili al markup sono correlate ai modelli di visualizzazione e di layout e ai comportamenti descritti in [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="f0dc3-234">Se un particolare controllo non consente le preferenze di layout direttamente nel markup oppure le preferenze di layout non sono specificate, il Framework definisce le convenzioni di visualizzazione specifiche del controllo in base alla quantità di spazio disponibile sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="f0dc3-235">Gli esempi seguenti illustrano come incorporare un set di raccolte in una barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="f0dc3-236">Dichiarazioni di comando</span><span class="sxs-lookup"><span data-stu-id="f0dc3-236">Command Declarations</span></span>

<span data-ttu-id="f0dc3-237">I comandi devono essere dichiarati con un attributo *CommandName* usato per associare un controllo o un set di controlli con il comando.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="f0dc3-238">Qui è anche possibile specificare un attributo *CommandID* usato per associare un comando a un gestore di comandi quando il markup viene compilato.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="f0dc3-239">Se non viene fornito alcun ID, ne viene generato uno dal Framework.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="f0dc3-240">Dichiarazioni di controllo</span><span class="sxs-lookup"><span data-stu-id="f0dc3-240">Control Declarations</span></span>

<span data-ttu-id="f0dc3-241">Questa sezione contiene esempi che illustrano il markup di base del controllo necessario per i vari tipi di raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="f0dc3-242">Illustrano come dichiarare i controlli della raccolta e associarli a un comando tramite l'attributo *CommandName* .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="f0dc3-243">Nell'esempio seguente viene illustrata una dichiarazione di controllo per [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) in cui viene usato l'attributo *Type* per specificare che si tratta di una raccolta di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="f0dc3-244">Nell'esempio seguente viene illustrata una dichiarazione di controllo per [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="f0dc3-245">Nell'esempio seguente viene illustrata una dichiarazione di controllo per l'oggetto [**inribbongallery**](windowsribbon-element-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="f0dc3-246">Poiché l' [**inribbongallery**](windowsribbon-element-inribbongallery.md) è progettato per visualizzare un subset della relativa raccolta di elementi nella barra multifunzione senza attivare un menu a discesa, fornisce un numero di attributi facoltativi che ne regolano la dimensione e il layout dell'elemento nell'inizializzazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="f0dc3-247">Questi attributi sono univoci per gli **inribbongallery** e non sono disponibili dagli altri controlli dinamici.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



<span data-ttu-id="f0dc3-248">Nell'esempio seguente viene illustrata una dichiarazione di controllo per [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="f0dc3-249">Creazione di un gestore di comandi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-249">Create a Command Handler</span></span>

<span data-ttu-id="f0dc3-250">Per ogni comando, il Framework della barra multifunzione richiede un gestore di comando corrispondente nell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="f0dc3-251">I gestori di comandi sono implementati dall'applicazione host della barra multifunzione e derivano dall'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f0dc3-252">È possibile associare più comandi a un singolo gestore di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="f0dc3-253">Un gestore di comando svolge due finalità:</span><span class="sxs-lookup"><span data-stu-id="f0dc3-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="f0dc3-254">[**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) risponde alle richieste di aggiornamento delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="f0dc3-255">I valori delle proprietà del comando, ad esempio [interfaccia utente \_ pkey \_ abilitata](windowsribbon-reference-properties-uipkey-enabled.md) o [ \_ \_ etichetta pkey interfaccia utente](windowsribbon-reference-properties-uipkey-label.md), vengono impostati tramite chiamate a [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) o [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="f0dc3-256">[**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) risponde per eseguire gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="f0dc3-257">Questo metodo supporta i tre stati di esecuzione seguenti specificati dal parametro [**\_ EXECUTIONVERB dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .</span><span class="sxs-lookup"><span data-stu-id="f0dc3-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="f0dc3-258">Lo stato Execute esegue o esegue il commit in tutti i comandi a cui è associato il gestore.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="f0dc3-259">Lo stato di anteprima Visualizza in anteprima tutti i comandi a cui è associato il gestore.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="f0dc3-260">Questa operazione esegue essenzialmente i comandi senza commit nel risultato.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="f0dc3-261">Lo stato CancelPreview Annulla tutti i comandi visualizzati in anteprima.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="f0dc3-262">Questa operazione è necessaria per supportare l'attraversamento tramite un menu o un elenco ed eseguire l'anteprima sequenziale e annullare i risultati secondo le esigenze.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="f0dc3-263">Nell'esempio seguente viene illustrato un gestore di comandi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="f0dc3-264">Associare il gestore di comandi</span><span class="sxs-lookup"><span data-stu-id="f0dc3-264">Bind the Command Handler</span></span>

<span data-ttu-id="f0dc3-265">Dopo aver definito un gestore di comandi, il comando deve essere associato al gestore.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="f0dc3-266">Nell'esempio seguente viene illustrato come associare un comando della raccolta a un gestore di comandi specifico.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="f0dc3-267">In questo caso, entrambi i controlli [**ComboBox**](windowsribbon-element-combobox.md) e Gallery sono associati ai rispettivi gestori di comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="f0dc3-268">Inizializzare una raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-268">Initialize a Collection</span></span>

<span data-ttu-id="f0dc3-269">Nell'esempio seguente viene illustrata un'implementazione personalizzata di [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per le raccolte di elementi e comandi.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="f0dc3-270">La classe CItemProperties in questo esempio è derivata da [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span><span class="sxs-lookup"><span data-stu-id="f0dc3-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="f0dc3-271">Oltre al metodo [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)necessario, la classe CItemProperties implementa un set di funzioni di supporto per l'inizializzazione e il rilevamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="f0dc3-272">Gestisci eventi raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-272">Handle Collection Events</span></span>

<span data-ttu-id="f0dc3-273">Nell'esempio seguente viene illustrata un'implementazione di IUICollectionChangedEvent.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="f0dc3-274">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0dc3-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0dc3-275">Proprietà della raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="f0dc3-276">Creazione di un'applicazione Ribbon</span><span class="sxs-lookup"><span data-stu-id="f0dc3-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="f0dc3-277">Informazioni sui comandi e sui controlli</span><span class="sxs-lookup"><span data-stu-id="f0dc3-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="f0dc3-278">Linee guida sull'esperienza utente della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="f0dc3-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="f0dc3-279">Processo di progettazione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="f0dc3-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="f0dc3-280">Esempio di raccolta</span><span class="sxs-lookup"><span data-stu-id="f0dc3-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 