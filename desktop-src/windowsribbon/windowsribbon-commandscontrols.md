---
title: Informazioni sui comandi e sui controlli
description: La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi di Windows Ribbon Framework \ 8212; un sistema basato su uno schema progettuale in cui funzionalità e comportamento sono implementate indipendentemente dai controlli che espongono questa funzionalità.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Barra multifunzione di Windows, Panoramica comandi
- Barra multifunzione, Panoramica comandi
- Barra multifunzione di Windows, Cenni preliminari sui controlli
- Barra multifunzione, Cenni preliminari sui controlli
- sistema di comando per la barra multifunzione di Windows
- controlli per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566031"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="8a7ef-109">Informazioni sui comandi e sui controlli</span><span class="sxs-lookup"><span data-stu-id="8a7ef-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="8a7ef-110">La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi del Framework della barra multifunzione di Windows, un sistema basato su uno schema progettuale in cui funzionalità e comportamento sono implementate indipendentemente dai controlli che espongono questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="8a7ef-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="8a7ef-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8a7ef-112">Sistema di comandi della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="8a7ef-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="8a7ef-113">Controlli</span><span class="sxs-lookup"><span data-stu-id="8a7ef-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="8a7ef-114">Comandi</span><span class="sxs-lookup"><span data-stu-id="8a7ef-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="8a7ef-115">Esperienza del comando in azione</span><span class="sxs-lookup"><span data-stu-id="8a7ef-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="8a7ef-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a7ef-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="8a7ef-117">Introduzione</span><span class="sxs-lookup"><span data-stu-id="8a7ef-117">Introduction</span></span>

<span data-ttu-id="8a7ef-118">Questo articolo illustra la progettazione del sistema di comandi del Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="8a7ef-119">Vengono descritti i concetti di comandi e controlli ed è possibile esplorare il modo in cui interagiscono per offrire un'esperienza di comando avanzata con un host di nuove funzionalità dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="8a7ef-120">Sistema di comandi della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="8a7ef-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="8a7ef-121">Nel framework della barra multifunzione, i comandi e i controlli sono entità indipendenti.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="8a7ef-122">Un comando è una struttura astratta, senza vincoli di presentazione, che rappresenta un'attività o una classe di funzionalità specifica.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="8a7ef-123">Un controllo, d'altra parte, è un oggetto concreto che espone la funzionalità del comando tramite l'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="8a7ef-124">Questa distinzione consente di definire i comandi che sono privi di dettagli dell'interfaccia utente e possono essere eseguiti allo scopo di un'azione senza la necessità di gestire il modo in cui l'azione è stata richiamata.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="8a7ef-125">Controlli</span><span class="sxs-lookup"><span data-stu-id="8a7ef-125">Controls</span></span>

<span data-ttu-id="8a7ef-126">I controlli sono gli oggetti dell'interfaccia utente necessari per la presentazione del comando.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="8a7ef-127">Viene eseguito il rendering e la gestione in fase di esecuzione dal Framework in base all'interazione dell'utente e a un set di proprietà e comportamenti intrinseci.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="8a7ef-128">Noto come layout adattivo, la flessibilità gestita dal framework dell'interfaccia utente è uno degli ottimi punti di forza della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="8a7ef-129">I controlli della barra multifunzione possono essere riconfigurati automaticamente tramite modelli di layout dipendenti dal Framework o definiti dallo sviluppatore che sono in grado di rispondere a diversi requisiti del runtime, il tutto senza scrivere una singola riga di codice di presentazione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="8a7ef-130">Per ulteriori informazioni, vedere [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="8a7ef-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="8a7ef-131">Oltre ai vantaggi del layout adattivo, molti controlli della barra multifunzione complessi forniscono soluzioni autosufficienti per spazi di problemi specifici dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="8a7ef-132">Grazie a un modello di interazione sofisticato, i controlli della barra multifunzione, ad esempio FontControl o ColorPicker, consentono di modificare i dati in termini più astratti tramite i contenitori di proprietà degli attributi dei tipi di carattere o dei colori effettivi anziché tramite vari controlli secondari, enumerazioni e valori di indice dei controlli Windows standard.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="8a7ef-133">Comandi</span><span class="sxs-lookup"><span data-stu-id="8a7ef-133">Commands</span></span>

<span data-ttu-id="8a7ef-134">A regime di controllo libero ai controlli della barra multifunzione che espongono la loro funzionalità, le implementazioni dei comandi sono il dominio dell'applicazione host e hanno il formato di listener di eventi, gestori di comandi e varie proprietà del comando.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="8a7ef-135">I comandi sono dichiarati nel markup della barra multifunzione con un ID univoco o assegnano un ID generato dal compilatore di markup durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="8a7ef-136">I comandi sono associati ai controlli tramite un nome di comando ma, a differenza dei controlli, la relativa funzionalità effettiva viene definita nel codice in cui sono associati a gestori di comandi specifici tramite l'ID di comando.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="8a7ef-137">In fase di compilazione, questo ID viene archiviato in un file di intestazione della definizione di ID che espone i comandi ai gestori di comandi corrispondenti nell'applicazione host della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="8a7ef-138">Ogni comando ha un tipo di comando sottostante nell'enumerazione [**\_ COMMANDTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .</span><span class="sxs-lookup"><span data-stu-id="8a7ef-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="8a7ef-139">Esperienza del comando in azione</span><span class="sxs-lookup"><span data-stu-id="8a7ef-139">The Command Experience In Action</span></span>

<span data-ttu-id="8a7ef-140">Le funzionalità di questo modello di comando sono illustrate dalla barra di accesso rapido della barra multifunzione (QAT).</span><span class="sxs-lookup"><span data-stu-id="8a7ef-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="8a7ef-141">Il QAT offre agli utenti finali un modo per definire facilmente i propri collegamenti per qualsiasi controllo nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="8a7ef-142">Un collegamento viene aggiunto dinamicamente a QAT in fase di esecuzione quando l'utente fa clic con il pulsante destro del mouse su un controllo Ribbon e seleziona **Aggiungi alla barra di accesso rapido** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="8a7ef-143">Nell'immagine seguente vengono illustrati i comandi **Incolla** e **Incolla da** , rappresentati da un controllo [**SplitButton**](windowsribbon-element-splitbutton.md) , nella barra multifunzione di Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![immagine del SplitButton incolla nella barra multifunzione di Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="8a7ef-145">Nell'immagine seguente vengono mostrati gli stessi comandi **Incolla** e **Incolla** dei comandi, ancora rappresentati da un controllo [**SplitButton**](windowsribbon-element-splitbutton.md) , nella barra multifunzione qat di Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![immagine del SplitButton incolla in Microsoft Paint qat.](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="8a7ef-147">Quando un controllo è ospitato da QAT, la nuova istanza del controllo mantiene tutte le funzionalità del controllo originale senza la necessità di altri listener di eventi e gestori di comandi per supportarla.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="8a7ef-148">Entrambi i controlli sono associati allo stesso gestore di comandi della barra multifunzione tramite un identificatore di comando condiviso.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="8a7ef-149">In questo modo, il Framework considera entrambi i controlli come uno, indipendentemente dal fatto che venga richiamato.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="8a7ef-150">Gli stessi vantaggi vengono realizzati quando i comandi vengono incorporati in un [**ContextPopup**](windowsribbon-element-contextpopup.md) in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="8a7ef-151">In questo caso, è possibile usare i gestori dei comandi di Incolla se il controllo [**SplitButton**](windowsribbon-element-splitbutton.md) viene visualizzato nella barra multifunzione, qat o **ContextPopup**.</span><span class="sxs-lookup"><span data-stu-id="8a7ef-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a7ef-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a7ef-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a7ef-153">Introduzione al framework della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="8a7ef-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="8a7ef-154">Creazione di un'applicazione Ribbon</span><span class="sxs-lookup"><span data-stu-id="8a7ef-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="8a7ef-155">Dichiarazione di comandi e controlli con markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="8a7ef-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 