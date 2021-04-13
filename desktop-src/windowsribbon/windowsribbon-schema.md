---
title: Dichiarazione di comandi e controlli con markup della barra multifunzione
description: Il Framework della barra multifunzione di Windows usa un linguaggio di markup basato su Extensible Application Markup Language (XAML) per implementare in modo dichiarativo l'aspetto di un'applicazione Ribbon.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Barra multifunzione di Windows, struttura markup
- Barra multifunzione, struttura markup
- Barra multifunzione di Windows, separazione della presentazione dalla logica dei comandi
- Barra multifunzione, separazione della presentazione dalla logica del comando
- Barra multifunzione di Windows, componenti
- Barra multifunzione, componenti
- sistema di comando per la barra multifunzione di Windows
- controlli per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399447"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="0bc36-111">Dichiarazione di comandi e controlli con markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0bc36-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="0bc36-112">Il Framework della barra multifunzione di Windows usa un linguaggio di markup basato su Extensible Application Markup Language (XAML) per implementare in modo dichiarativo l'aspetto di un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="0bc36-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="0bc36-113">Separazione della presentazione dalla logica del comando</span><span class="sxs-lookup"><span data-stu-id="0bc36-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="0bc36-114">Struttura di markup</span><span class="sxs-lookup"><span data-stu-id="0bc36-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="0bc36-115">Componenti della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0bc36-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="0bc36-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0bc36-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="0bc36-117">Separazione della presentazione dalla logica del comando</span><span class="sxs-lookup"><span data-stu-id="0bc36-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="0bc36-118">La separazione degli attributi di presentazione e visualizzazione dalla logica dei comandi nel framework della barra multifunzione viene eseguita tramite due piattaforme di sviluppo distinte, ma dipendenti.</span><span class="sxs-lookup"><span data-stu-id="0bc36-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="0bc36-119">I layout di controllo, i comportamenti di ridimensionamento, le dichiarazioni di comando e le specifiche delle risorse sono il dominio della fase di progettazione di una sintassi di markup dichiarativa basata sulla specifica [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) .</span><span class="sxs-lookup"><span data-stu-id="0bc36-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="0bc36-120">Funzionalità di basso livello, hook dell'applicazione e gestori di comandi sono definiti nelle implementazioni di interfaccia basate su Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="0bc36-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="0bc36-121">Questa separazione di presentazione e logica offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0bc36-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="0bc36-122">Un ciclo di sviluppo di applicazioni più efficiente che consente agli sviluppatori e ai progettisti dell'interfaccia utente di implementare l'interfaccia utente grafica dell'applicazione Ribbon indipendentemente dalla funzionalità di base dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0bc36-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="0bc36-123">Questa funzionalità di base può essere lasciata agli sviluppatori di software dedicati.</span><span class="sxs-lookup"><span data-stu-id="0bc36-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="0bc36-124">Manutenzione meno costosa poiché le modifiche all'interfaccia utente grafica sono possibili senza modifiche alle funzionalità principali (e viceversa).</span><span class="sxs-lookup"><span data-stu-id="0bc36-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="0bc36-125">Specifica semplice delle risorse stringa e immagine tramite markup.</span><span class="sxs-lookup"><span data-stu-id="0bc36-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="0bc36-126">Semplicità di prototipo.</span><span class="sxs-lookup"><span data-stu-id="0bc36-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="0bc36-127">Struttura di markup</span><span class="sxs-lookup"><span data-stu-id="0bc36-127">Markup Structure</span></span>

<span data-ttu-id="0bc36-128">All'interno della struttura del markup del Framework Ribbon sono presenti due rami distinti.</span><span class="sxs-lookup"><span data-stu-id="0bc36-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="0bc36-129">Il primo ramo contiene un manifesto di dichiarazioni di comando e di risorse (stringhe e immagini).</span><span class="sxs-lookup"><span data-stu-id="0bc36-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="0bc36-130">Ogni voce di comando viene utilizzata dal Framework per associare un controllo Ribbon, tramite un ID di comando, a un gestore di comandi definito nel codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0bc36-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="0bc36-131">Il secondo ramo contiene le dichiarazioni di controllo effettive.</span><span class="sxs-lookup"><span data-stu-id="0bc36-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="0bc36-132">Ogni controllo è associato a un comando tramite un attributo *CommandName* che esegue il mapping a un attributo *Name* specificato in ogni dichiarazione di comando.</span><span class="sxs-lookup"><span data-stu-id="0bc36-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="0bc36-133">Componenti della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0bc36-133">Ribbon Components</span></span>

<span data-ttu-id="0bc36-134">La funzionalità dell'interfaccia utente del Framework Ribbon è esposta tramite [viste](windowsribbon-reference-elements-view.md).</span><span class="sxs-lookup"><span data-stu-id="0bc36-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="0bc36-135">Una vista è essenzialmente un contenitore, ad esempio la [**barra multifunzione**](windowsribbon-element-ribbon.md) e [**ContextPopup**](windowsribbon-element-contextpopup.md), usato per presentare i controlli del Framework e i comandi a cui sono associati.</span><span class="sxs-lookup"><span data-stu-id="0bc36-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="0bc36-136">La visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) è costituita da diversi componenti che includono un [menu applicazione](windowsribbon-controls-applicationmenu.md), la [barra di accesso rapido (QAT)](windowsribbon-controls-quickaccesstoolbar.md) per la visualizzazione dei comandi di uso comune dall'interfaccia utente della barra multifunzione, le [schede](windowsribbon-controls-tab.md) core e contestuali che contengono [gruppi](windowsribbon-controls-group.md) di controlli e il sistema di menu di scelta rapida completo del [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="0bc36-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="0bc36-137">Tutti i componenti della barra multifunzione sono dichiarati in un file di markup autonomo:</span><span class="sxs-lookup"><span data-stu-id="0bc36-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="0bc36-138">Specifica le proprietà di base per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="0bc36-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="0bc36-139">Mostra chiaramente le relazioni gerarchiche.</span><span class="sxs-lookup"><span data-stu-id="0bc36-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="0bc36-140">Fornisce le preferenze di layout e gli hint di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="0bc36-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="0bc36-141">Per ulteriori informazioni sui modelli di layout del Framework della barra multifunzione, vedere [personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di scalabilità](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0bc36-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="0bc36-142">Fornisce un modo per definire risorse quali immagini ed etichette.</span><span class="sxs-lookup"><span data-stu-id="0bc36-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="0bc36-143">Per altre informazioni sulle risorse di immagine, vedere [specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md).</span><span class="sxs-lookup"><span data-stu-id="0bc36-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="0bc36-144">I due esempi di markup della barra multifunzione seguenti illustrano come un set di voci di menu dell'applicazione Ribbon è associato a un nome di comando e a un ID.</span><span class="sxs-lookup"><span data-stu-id="0bc36-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="0bc36-145">In questa sezione vengono illustrate le dichiarazioni di comando necessarie per un menu dell'applicazione con comandi di base, ad esempio nuovo, Apri e Salva.</span><span class="sxs-lookup"><span data-stu-id="0bc36-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="0bc36-146">In questa sezione vengono illustrate le dichiarazioni di controllo associate.</span><span class="sxs-lookup"><span data-stu-id="0bc36-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="0bc36-147">Quando il markup viene compilato con lo strumento del compilatore di comandi dell'interfaccia utente (UICC), i nomi e gli ID del comando vengono inseriti in un file di intestazione utilizzato dall'applicazione host della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0bc36-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="0bc36-148">Di seguito è riportato un esempio di un file di intestazione generato da UICC.</span><span class="sxs-lookup"><span data-stu-id="0bc36-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="0bc36-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0bc36-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc36-150">Extensible Application Markup Language (XAML)</span><span class="sxs-lookup"><span data-stu-id="0bc36-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="0bc36-151">Compilazione del markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0bc36-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 