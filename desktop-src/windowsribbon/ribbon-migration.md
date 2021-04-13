---
title: Migrazione al framework della barra multifunzione di Windows
description: È possibile eseguire la migrazione di un'applicazione che si basa su menu tradizionali, barre degli strumenti e finestre di dialogo nell'interfaccia utente avanzata, dinamica e basata sul contesto del sistema di comandi della barra multifunzione di Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Barra multifunzione di Windows, migrazione a
- Barra multifunzione, migrazione a
- migrazione alla barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473595"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="c9824-106">Migrazione al framework della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="c9824-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="c9824-107">È possibile eseguire la migrazione di un'applicazione che si basa su menu tradizionali, barre degli strumenti e finestre di dialogo nell'interfaccia utente avanzata, dinamica e basata sul contesto del sistema di comandi della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="c9824-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="c9824-108">Si tratta di un modo semplice ed efficace per modernizzare e rivitalizzare l'applicazione, migliorando al tempo stesso l'accessibilità, l'usabilità e l'individuabilità delle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c9824-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="c9824-109">Introduzione</span><span class="sxs-lookup"><span data-stu-id="c9824-109">Introduction</span></span>

<span data-ttu-id="c9824-110">In generale, la migrazione di un'applicazione esistente al framework della barra multifunzione prevede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c9824-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="c9824-111">Progettazione di un'organizzazione di controllo e layout della barra multifunzione che espone la funzionalità dell'applicazione esistente ed è sufficientemente flessibile per supportare nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c9824-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="c9824-112">Adattamento del codice dell'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c9824-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="c9824-113">Migrazione delle risorse dell'applicazione esistenti (stringhe e immagini) al framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="c9824-114">Le [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx) devono essere esaminate per determinare se l'applicazione è un candidato adatto per un'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="c9824-115">Progettare il layout della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="c9824-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="c9824-116">È possibile identificare le possibili progettazioni dell'interfaccia utente della barra multifunzione e i layout dei controlli eseguendo questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="c9824-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="c9824-117">Esecuzione dell'inventario di tutte le funzionalità esistenti.</span><span class="sxs-lookup"><span data-stu-id="c9824-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="c9824-118">Conversione di questa funzionalità in comandi della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="c9824-119">Organizzare i comandi in gruppi logici.</span><span class="sxs-lookup"><span data-stu-id="c9824-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="c9824-120">Eseguire l'inventario</span><span class="sxs-lookup"><span data-stu-id="c9824-120">Take Inventory</span></span>

<span data-ttu-id="c9824-121">Nel framework della barra multifunzione, la funzionalità esposta da un'applicazione che modifica lo stato o la visualizzazione di un'area di lavoro o di un documento è considerata un comando.</span><span class="sxs-lookup"><span data-stu-id="c9824-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="c9824-122">Ciò che costituisce un comando può variare e dipende dalla natura e dal dominio dell'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c9824-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="c9824-123">La tabella seguente elenca un set di comandi di base per un'applicazione di modifica del testo ipotetica:</span><span class="sxs-lookup"><span data-stu-id="c9824-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="c9824-124">Simbolo</span><span class="sxs-lookup"><span data-stu-id="c9824-124">Symbol</span></span>           | <span data-ttu-id="c9824-125">ID</span><span class="sxs-lookup"><span data-stu-id="c9824-125">ID</span></span>     | <span data-ttu-id="c9824-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9824-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="c9824-127">\_nuovo file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="c9824-128">0xE100</span><span class="sxs-lookup"><span data-stu-id="c9824-128">0xE100</span></span> | <span data-ttu-id="c9824-129">Nuovo documento</span><span class="sxs-lookup"><span data-stu-id="c9824-129">New document</span></span>              |
| <span data-ttu-id="c9824-130">\_Salva file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="c9824-131">0xE103</span><span class="sxs-lookup"><span data-stu-id="c9824-131">0xE103</span></span> | <span data-ttu-id="c9824-132">Salva documento</span><span class="sxs-lookup"><span data-stu-id="c9824-132">Save document</span></span>             |
| <span data-ttu-id="c9824-133">\_SaveAs file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="c9824-134">0xE104</span><span class="sxs-lookup"><span data-stu-id="c9824-134">0xE104</span></span> | <span data-ttu-id="c9824-135">Salva con nome... dialogo</span><span class="sxs-lookup"><span data-stu-id="c9824-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="c9824-136">ID \_ file \_ aperto</span><span class="sxs-lookup"><span data-stu-id="c9824-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="c9824-137">0xE101</span><span class="sxs-lookup"><span data-stu-id="c9824-137">0xE101</span></span> | <span data-ttu-id="c9824-138">Apri... dialogo</span><span class="sxs-lookup"><span data-stu-id="c9824-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="c9824-139">\_uscita file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="c9824-140">0xE102</span><span class="sxs-lookup"><span data-stu-id="c9824-140">0xE102</span></span> | <span data-ttu-id="c9824-141">Uscire dall'applicazione</span><span class="sxs-lookup"><span data-stu-id="c9824-141">Exit the application</span></span>      |
| <span data-ttu-id="c9824-142">\_Annulla modifica \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="c9824-143">0xE12B</span><span class="sxs-lookup"><span data-stu-id="c9824-143">0xE12B</span></span> | <span data-ttu-id="c9824-144">Annulla</span><span class="sxs-lookup"><span data-stu-id="c9824-144">Undo</span></span>                      |
| <span data-ttu-id="c9824-145">\_taglia ID modifica \_</span><span class="sxs-lookup"><span data-stu-id="c9824-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="c9824-146">0xE123</span><span class="sxs-lookup"><span data-stu-id="c9824-146">0xE123</span></span> | <span data-ttu-id="c9824-147">Taglia il testo selezionato</span><span class="sxs-lookup"><span data-stu-id="c9824-147">Cut selected text</span></span>         |
| <span data-ttu-id="c9824-148">\_Copia ID modifica \_</span><span class="sxs-lookup"><span data-stu-id="c9824-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="c9824-149">0xE122</span><span class="sxs-lookup"><span data-stu-id="c9824-149">0xE122</span></span> | <span data-ttu-id="c9824-150">Copia testo selezionato</span><span class="sxs-lookup"><span data-stu-id="c9824-150">Copy selected text</span></span>        |
| <span data-ttu-id="c9824-151">\_modifica ID \_ Incolla</span><span class="sxs-lookup"><span data-stu-id="c9824-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="c9824-152">0xE125</span><span class="sxs-lookup"><span data-stu-id="c9824-152">0xE125</span></span> | <span data-ttu-id="c9824-153">Incolla testo dagli Appunti</span><span class="sxs-lookup"><span data-stu-id="c9824-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="c9824-154">\_modifica ID \_ Cancella</span><span class="sxs-lookup"><span data-stu-id="c9824-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="c9824-155">0xE120</span><span class="sxs-lookup"><span data-stu-id="c9824-155">0xE120</span></span> | <span data-ttu-id="c9824-156">Elimina testo selezionato</span><span class="sxs-lookup"><span data-stu-id="c9824-156">Delete selected text</span></span>      |
| <span data-ttu-id="c9824-157">\_Zoom visualizzazione \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="c9824-158">1242</span><span class="sxs-lookup"><span data-stu-id="c9824-158">1242</span></span>   | <span data-ttu-id="c9824-159">Ingrandisci... dialogo</span><span class="sxs-lookup"><span data-stu-id="c9824-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="c9824-160">Per la compilazione di un inventario dei comandi, vedere oltre i menu e le barre degli strumenti esistenti.</span><span class="sxs-lookup"><span data-stu-id="c9824-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="c9824-161">Prendere in considerazione tutti i modi in cui un utente può interagire con l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9824-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="c9824-162">Anche se non tutti i comandi sono idonei per l'inclusione nella barra multifunzione, questo esercizio può esporre in modo molto efficace i comandi precedentemente nascosti dai livelli dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c9824-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="c9824-163">Traduci</span><span class="sxs-lookup"><span data-stu-id="c9824-163">Translate</span></span>

<span data-ttu-id="c9824-164">Non tutti i comandi devono essere rappresentati nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="c9824-165">Ad esempio, l'immissione di testo, la modifica di una selezione, lo scorrimento o lo spostamento del punto di inserimento con il mouse vengono tutti qualificati come comandi nell'editor di testo ipotetico, tuttavia, questi non sono idonei per esporre in una barra dei comandi perché ognuno implica un'interazione diretta con l'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9824-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="c9824-166">Viceversa, alcune funzionalità potrebbero non essere considerate come un comando nel senso tradizionale.</span><span class="sxs-lookup"><span data-stu-id="c9824-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="c9824-167">Ad esempio, anziché essere seppelliti in una finestra di dialogo, le regolazioni dei margini della pagina della stampante possono essere rappresentate nella barra multifunzione come un gruppo di controlli casella di selezione in una scheda contestuale o in una [modalità di applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="c9824-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="c9824-168">Prendere nota dell'ID numerico che può essere assegnato a ogni comando.</span><span class="sxs-lookup"><span data-stu-id="c9824-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="c9824-169">Alcuni framework dell'interfaccia utente, ad esempio Microsoft Foundation Classes (MFC), definiscono gli ID per i comandi come il menu file e modifica (da 0xE100 a 0xE200).</span><span class="sxs-lookup"><span data-stu-id="c9824-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="c9824-170">Organizzazione</span><span class="sxs-lookup"><span data-stu-id="c9824-170">Organize</span></span>

<span data-ttu-id="c9824-171">Prima di provare a organizzare l'inventario dei comandi, è necessario esaminare le [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx) per le procedure consigliate per l'implementazione di un'interfaccia utente della barra</span><span class="sxs-lookup"><span data-stu-id="c9824-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="c9824-172">In generale, le regole seguenti possono essere applicate all'organizzazione dei comandi della barra multifunzione:</span><span class="sxs-lookup"><span data-stu-id="c9824-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="c9824-173">I comandi che operano sul file o sull'applicazione complessiva più probabilmente appartengono al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="c9824-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="c9824-174">I comandi usati di frequente, ad esempio taglia, copia e incolla, come nell'esempio di editor di testo, vengono in genere inseriti in una scheda Home predefinita. Nelle applicazioni più complesse possono essere duplicate altrove nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="c9824-175">I comandi importanti o di uso frequente possono garantire l'inclusione predefinita nella [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="c9824-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="c9824-176">Il Framework Ribbon fornisce anche controlli ContextMenu e MiniToolbar tramite la vista ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="c9824-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="c9824-177">Queste funzionalità non sono obbligatorie, ma se l'applicazione dispone di uno o più menu di scelta rapida esistenti, la migrazione dei comandi che contengono potrebbe consentire il riutilizzo della codebase esistente con binding automatico alle risorse esistenti.</span><span class="sxs-lookup"><span data-stu-id="c9824-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="c9824-178">Poiché ogni applicazione è diversa, leggere le linee guida e provare ad applicarle alla massima misura possibile.</span><span class="sxs-lookup"><span data-stu-id="c9824-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="c9824-179">Uno degli obiettivi del Framework della barra multifunzione è fornire un'esperienza utente familiare e coerente e questo obiettivo sarà più realizzabile se le soluzioni per le nuove applicazioni rispecchiano il più possibile le applicazioni Ribbon esistenti.</span><span class="sxs-lookup"><span data-stu-id="c9824-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="c9824-180">Adattare il codice</span><span class="sxs-lookup"><span data-stu-id="c9824-180">Adapt Your Code</span></span>

<span data-ttu-id="c9824-181">Una volta identificati e organizzati i comandi della barra multifunzione in raggruppamenti logici, il numero di passaggi necessari per incorporare il Framework della barra multifunzione nel codice dell'applicazione esistente dipende dalla complessità dell'applicazione originale.</span><span class="sxs-lookup"><span data-stu-id="c9824-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="c9824-182">In generale, sono disponibili tre passaggi di base:</span><span class="sxs-lookup"><span data-stu-id="c9824-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="c9824-183">Creare il markup della barra multifunzione in base all'organizzazione dei comandi e alla specifica del layout.</span><span class="sxs-lookup"><span data-stu-id="c9824-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="c9824-184">Sostituisci funzionalità di menu e barre degli strumenti legacy con funzionalità della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="c9824-185">Implementare una scheda IUICommandHandler.</span><span class="sxs-lookup"><span data-stu-id="c9824-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="c9824-186">Creare il markup</span><span class="sxs-lookup"><span data-stu-id="c9824-186">Create The Markup</span></span>

<span data-ttu-id="c9824-187">L'elenco di comandi, nonché l'organizzazione e il layout vengono dichiarati tramite il file di markup della barra multifunzione utilizzato dal [compilatore di markup della barra multifunzione](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="c9824-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="c9824-188">Molti dei passaggi necessari per adattare un'applicazione esistente sono simili a quelli necessari per avviare una nuova applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="c9824-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="c9824-189">Per ulteriori informazioni, vedere l'esercitazione relativa alla [creazione di un'applicazione barra multifunzione](windowsribbon-stepbystep.md) per una nuova applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="c9824-190">Il markup della barra multifunzione è suddiviso in due sezioni principali.</span><span class="sxs-lookup"><span data-stu-id="c9824-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="c9824-191">La prima sezione è un manifesto di comandi e delle risorse associate (stringhe e immagini).</span><span class="sxs-lookup"><span data-stu-id="c9824-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="c9824-192">La seconda sezione specifica la struttura e il posizionamento dei controlli sulla barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="c9824-193">Il markup per l'editor di testo semplice potrebbe avere un aspetto simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="c9824-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="c9824-194">Le risorse di immagine e stringa sono descritte più avanti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="c9824-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="c9824-195">Per evitare di ridefinire i simboli definiti da un Framework dell'interfaccia utente, ad esempio MFC, nell'esempio precedente vengono usati nomi di simboli leggermente diversi per ogni comando (ID \_ file \_ nuovo rispetto all'ID \_ cmd \_ nuovo).</span><span class="sxs-lookup"><span data-stu-id="c9824-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="c9824-196">Tuttavia, l'ID numerico assegnato a ogni comando deve rimanere invariato.</span><span class="sxs-lookup"><span data-stu-id="c9824-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="c9824-197">Per integrare il file di markup in un'applicazione, configurare un'istruzione di compilazione personalizzata per eseguire il compilatore di markup della barra multifunzione UICC.exe.</span><span class="sxs-lookup"><span data-stu-id="c9824-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="c9824-198">I file di intestazione e di risorse risultanti vengono quindi incorporati nel progetto esistente.</span><span class="sxs-lookup"><span data-stu-id="c9824-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="c9824-199">Se l'applicazione della barra multifunzione Editor di testo di esempio è denominata "RibbonPad", è necessaria una riga di comando di compilazione personalizzata simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="c9824-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="c9824-200">Il compilatore di markup crea un file binario, un file di intestazione (H) e un file di risorse (RC).</span><span class="sxs-lookup"><span data-stu-id="c9824-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="c9824-201">Poiché è probabile che l'applicazione esistente disponga di un file RC esistente, includere i file H e RC generati nel file RC, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="c9824-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="c9824-202">Sostituire i menu e le barre degli strumenti legacy</span><span class="sxs-lookup"><span data-stu-id="c9824-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="c9824-203">Per sostituire i menu e le barre degli strumenti standard con una barra multifunzione in un'applicazione legacy è necessario quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c9824-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="c9824-204">Rimuovere la barra degli strumenti e i riferimenti alle risorse di menu dal file di risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9824-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="c9824-205">Elimina tutti i codici di inizializzazione della barra degli strumenti e dei menu.</span><span class="sxs-lookup"><span data-stu-id="c9824-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="c9824-206">Eliminare qualsiasi codice utilizzato per aggiungere una barra degli strumenti o una barra dei menu alla finestra di primo livello dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9824-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="c9824-207">Creare un'istanza del Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="c9824-208">Alleghi la barra multifunzione alla finestra di primo livello dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9824-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="c9824-209">Caricare il markup compilato.</span><span class="sxs-lookup"><span data-stu-id="c9824-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9824-210">La barra di stato esistente e le tabelle dei tasti di scelta rapida devono essere mantenute perché il Framework della barra multifunzione non sostituisce queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c9824-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="c9824-211">Nell'esempio seguente viene illustrato come inizializzare il Framework utilizzando [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span><span class="sxs-lookup"><span data-stu-id="c9824-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="c9824-212">Nell'esempio seguente viene illustrato come utilizzare [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) per caricare il markup compilato:</span><span class="sxs-lookup"><span data-stu-id="c9824-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="c9824-213">La classe CApplication, a cui si fa riferimento, deve implementare una coppia di interfacce di Component Object Model (COM) definite dal framework della barra multifunzione: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) e [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span><span class="sxs-lookup"><span data-stu-id="c9824-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="c9824-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fornisce l'interfaccia di callback principale tra il Framework e l'applicazione (ad esempio, l'altezza della barra multifunzione viene comunicata tramite [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), mentre i callback per i singoli comandi vengono forniti in risposta a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span><span class="sxs-lookup"><span data-stu-id="c9824-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="c9824-215">**Suggerimento:** Alcuni framework applicazione, ad esempio MFC, richiedono che l'altezza della barra multifunzione venga presa in considerazione durante il rendering dello spazio del documento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9824-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="c9824-216">In questi casi, l'aggiunta di una finestra nascosta per sovrapporre la barra multifunzione e forzare lo spazio del documento sull'altezza desiderata è necessaria.</span><span class="sxs-lookup"><span data-stu-id="c9824-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="c9824-217">Per un esempio di questo approccio, in cui viene chiamata una funzione di layout basata sull'altezza della barra multifunzione restituita dal metodo [**IUIRibbon:: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , vedere l' [esempio HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="c9824-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="c9824-218">L'esempio di codice seguente illustra un'implementazione di [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :</span><span class="sxs-lookup"><span data-stu-id="c9824-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="c9824-219">Implementare un adattatore IUICommandHandler</span><span class="sxs-lookup"><span data-stu-id="c9824-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="c9824-220">A seconda della progettazione dell'applicazione originale, può risultare più semplice avere più implementazioni del gestore comandi o un singolo gestore dei comandi di bridging che richiama la logica del comando dell'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c9824-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="c9824-221">Molte applicazioni usano \_ i messaggi di comando WM a questo scopo, dove è sufficiente fornire un singolo gestore di comandi per tutti gli scopi che inoltri semplicemente \_ i messaggi di comando WM alla finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="c9824-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="c9824-222">Tuttavia, questo approccio richiede una gestione speciale per i comandi, ad esempio **Exit** o **Close**.</span><span class="sxs-lookup"><span data-stu-id="c9824-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="c9824-223">Poiché la barra multifunzione non può essere distrutta durante l'elaborazione di un messaggio di finestra, il \_ messaggio WM Close deve essere inviato al thread dell'interfaccia utente dell'applicazione e non deve essere elaborato in modo sincrono, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="c9824-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="c9824-224">Migrazione di risorse</span><span class="sxs-lookup"><span data-stu-id="c9824-224">Migrating Resources</span></span>

<span data-ttu-id="c9824-225">Quando è stato definito il manifesto dei comandi, la struttura della barra multifunzione è stata dichiarata e il codice dell'applicazione è stato adattato per ospitare il Framework della barra multifunzione, il passaggio finale è la specifica delle risorse stringa e immagine per ogni comando.</span><span class="sxs-lookup"><span data-stu-id="c9824-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="c9824-226">Le risorse stringa e immagine vengono in genere fornite nel file di markup.</span><span class="sxs-lookup"><span data-stu-id="c9824-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="c9824-227">Tuttavia, possono essere generati o sostituiti a livello di codice implementando il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c9824-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="c9824-228">Risorse di stringa</span><span class="sxs-lookup"><span data-stu-id="c9824-228">String Resources</span></span>

<span data-ttu-id="c9824-229">[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) è la proprietà di stringa più comune definita per un comando.</span><span class="sxs-lookup"><span data-stu-id="c9824-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="c9824-230">Il rendering viene eseguito come etichette di testo per schede, gruppi e singoli controlli.</span><span class="sxs-lookup"><span data-stu-id="c9824-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="c9824-231">Una stringa di etichetta da una voce di menu legacy può in genere essere riutilizzata per un **comando. LabelTitle** senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="c9824-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="c9824-232">Tuttavia, le convenzioni seguenti sono state modificate con l'avvento della barra multifunzione:</span><span class="sxs-lookup"><span data-stu-id="c9824-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="c9824-233">Il suffisso con i puntini di sospensione (...), utilizzato per indicare un comando di avvio della finestra di dialogo, non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="c9824-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="c9824-234">La e commerciale (&) può ancora essere usata per indicare un tasto di scelta rapida per un comando che viene visualizzato in un menu, ma la proprietà [**Command. suggerimentod**](windowsribbon-element-command-keytip.md) supportata dal Framework soddisfa uno scopo simile.</span><span class="sxs-lookup"><span data-stu-id="c9824-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="c9824-235">Facendo riferimento all'esempio di editor di testo, è possibile specificare le seguenti stringhe per LabelTitle e suggerimento tasto di risposta:</span><span class="sxs-lookup"><span data-stu-id="c9824-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="c9824-236">Simbolo</span><span class="sxs-lookup"><span data-stu-id="c9824-236">Symbol</span></span>           | <span data-ttu-id="c9824-237">Stringa originale</span><span class="sxs-lookup"><span data-stu-id="c9824-237">Original string</span></span> | <span data-ttu-id="c9824-238">Stringa LabelTitle</span><span class="sxs-lookup"><span data-stu-id="c9824-238">LabelTitle string</span></span> | <span data-ttu-id="c9824-239">Stringa suggerimento</span><span class="sxs-lookup"><span data-stu-id="c9824-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="c9824-240">\_nuovo file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="c9824-241">&nuovo</span><span class="sxs-lookup"><span data-stu-id="c9824-241">&New</span></span>            | <span data-ttu-id="c9824-242">&nuovo</span><span class="sxs-lookup"><span data-stu-id="c9824-242">&New</span></span>              | <span data-ttu-id="c9824-243">N</span><span class="sxs-lookup"><span data-stu-id="c9824-243">N</span></span>             |
| <span data-ttu-id="c9824-244">\_Salva file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="c9824-245">&Salva</span><span class="sxs-lookup"><span data-stu-id="c9824-245">&Save</span></span>           | <span data-ttu-id="c9824-246">&Salva</span><span class="sxs-lookup"><span data-stu-id="c9824-246">&Save</span></span>             | <span data-ttu-id="c9824-247">S</span><span class="sxs-lookup"><span data-stu-id="c9824-247">S</span></span>             |
| <span data-ttu-id="c9824-248">\_SaveAs file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="c9824-249">Salva &con nome...</span><span class="sxs-lookup"><span data-stu-id="c9824-249">Save &As…</span></span>       | <span data-ttu-id="c9824-250">Salva &</span><span class="sxs-lookup"><span data-stu-id="c9824-250">Save &as</span></span>          | <span data-ttu-id="c9824-251">A</span><span class="sxs-lookup"><span data-stu-id="c9824-251">A</span></span>             |
| <span data-ttu-id="c9824-252">ID \_ file \_ aperto</span><span class="sxs-lookup"><span data-stu-id="c9824-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="c9824-253">&Apri...</span><span class="sxs-lookup"><span data-stu-id="c9824-253">&Open…</span></span>          | <span data-ttu-id="c9824-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="c9824-254">&Open</span></span>             | <span data-ttu-id="c9824-255">O</span><span class="sxs-lookup"><span data-stu-id="c9824-255">O</span></span>             |
| <span data-ttu-id="c9824-256">\_uscita file \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="c9824-257">&Esci</span><span class="sxs-lookup"><span data-stu-id="c9824-257">E&xit</span></span>           | <span data-ttu-id="c9824-258">&Esci</span><span class="sxs-lookup"><span data-stu-id="c9824-258">E&xit</span></span>             | <span data-ttu-id="c9824-259">X</span><span class="sxs-lookup"><span data-stu-id="c9824-259">X</span></span>             |
| <span data-ttu-id="c9824-260">\_Annulla modifica \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="c9824-261">Annulla &</span><span class="sxs-lookup"><span data-stu-id="c9824-261">&Undo</span></span>           | <span data-ttu-id="c9824-262">Annulla</span><span class="sxs-lookup"><span data-stu-id="c9824-262">Undo</span></span>              | <span data-ttu-id="c9824-263">Z</span><span class="sxs-lookup"><span data-stu-id="c9824-263">Z</span></span>             |
| <span data-ttu-id="c9824-264">\_taglia ID modifica \_</span><span class="sxs-lookup"><span data-stu-id="c9824-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="c9824-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="c9824-265">Cu&t</span></span>            | <span data-ttu-id="c9824-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="c9824-266">Cu&t</span></span>              | <span data-ttu-id="c9824-267">X</span><span class="sxs-lookup"><span data-stu-id="c9824-267">X</span></span>             |
| <span data-ttu-id="c9824-268">\_Copia ID modifica \_</span><span class="sxs-lookup"><span data-stu-id="c9824-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="c9824-269">Copia &</span><span class="sxs-lookup"><span data-stu-id="c9824-269">&Copy</span></span>           | <span data-ttu-id="c9824-270">Copia &</span><span class="sxs-lookup"><span data-stu-id="c9824-270">&Copy</span></span>             | <span data-ttu-id="c9824-271">C</span><span class="sxs-lookup"><span data-stu-id="c9824-271">C</span></span>             |
| <span data-ttu-id="c9824-272">\_modifica ID \_ Incolla</span><span class="sxs-lookup"><span data-stu-id="c9824-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="c9824-273">Incolla &</span><span class="sxs-lookup"><span data-stu-id="c9824-273">&Paste</span></span>          | <span data-ttu-id="c9824-274">Incolla &</span><span class="sxs-lookup"><span data-stu-id="c9824-274">&Paste</span></span>            | <span data-ttu-id="c9824-275">V</span><span class="sxs-lookup"><span data-stu-id="c9824-275">V</span></span>             |
| <span data-ttu-id="c9824-276">\_modifica ID \_ Cancella</span><span class="sxs-lookup"><span data-stu-id="c9824-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="c9824-277">Eliminazione &</span><span class="sxs-lookup"><span data-stu-id="c9824-277">&Delete</span></span>         | <span data-ttu-id="c9824-278">Eliminazione &</span><span class="sxs-lookup"><span data-stu-id="c9824-278">&Delete</span></span>           | <span data-ttu-id="c9824-279">D</span><span class="sxs-lookup"><span data-stu-id="c9824-279">D</span></span>             |
| <span data-ttu-id="c9824-280">\_Zoom visualizzazione \_ ID</span><span class="sxs-lookup"><span data-stu-id="c9824-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="c9824-281">Zoom &...</span><span class="sxs-lookup"><span data-stu-id="c9824-281">&Zoom…</span></span>          | <span data-ttu-id="c9824-282">Zoom</span><span class="sxs-lookup"><span data-stu-id="c9824-282">Zoom</span></span>              | <span data-ttu-id="c9824-283">Z</span><span class="sxs-lookup"><span data-stu-id="c9824-283">Z</span></span>             |



 

<span data-ttu-id="c9824-284">Di seguito è riportato un elenco di altre proprietà di stringa che devono essere impostate nella maggior parte dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c9824-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="c9824-285">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="c9824-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="c9824-286">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="c9824-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="c9824-287">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="c9824-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="c9824-288">Le schede, i gruppi e altre funzionalità dell'interfaccia utente della barra multifunzione possono ora essere dichiarate con tutte le risorse stringa e immagine specificate.</span><span class="sxs-lookup"><span data-stu-id="c9824-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="c9824-289">Nell'esempio di markup della barra multifunzione seguente sono illustrate varie risorse di stringa:</span><span class="sxs-lookup"><span data-stu-id="c9824-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="c9824-290">Risorse immagine</span><span class="sxs-lookup"><span data-stu-id="c9824-290">Image Resources</span></span>

<span data-ttu-id="c9824-291">Il Framework della barra multifunzione supporta formati di immagini che forniscono un aspetto molto più completo rispetto ai formati di immagine supportati dai componenti dei menu e delle barre degli strumenti precedenti.</span><span class="sxs-lookup"><span data-stu-id="c9824-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="c9824-292">Per Windows 8 e versioni successive, il Framework della barra multifunzione supporta i formati grafici seguenti: file di bitmap (BMP) a 32 bit ARGB (BMP) e file Portable Network Graphics (PNG) con trasparenza.</span><span class="sxs-lookup"><span data-stu-id="c9824-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="c9824-293">Per Windows 7 e versioni precedenti, le risorse di immagine devono essere conformi al formato di grafica BMP standard usato in Windows.</span><span class="sxs-lookup"><span data-stu-id="c9824-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="c9824-294">I file di immagine esistenti possono essere convertiti in uno dei due formati.</span><span class="sxs-lookup"><span data-stu-id="c9824-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="c9824-295">Tuttavia, i risultati potrebbero essere meno soddisfacenti se i file di immagine non supportano l'anti-aliasing e la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="c9824-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="c9824-296">Non è possibile specificare una singola dimensione predefinita per le risorse immagine nel framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="c9824-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="c9824-297">Tuttavia, per supportare il [layout adattivo](windowsribbon-templates.md) dei controlli, le immagini possono essere specificate in due dimensioni (grandi e piccole).</span><span class="sxs-lookup"><span data-stu-id="c9824-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="c9824-298">Tutte le immagini nel framework della barra multifunzione vengono ridimensionate in base alla risoluzione dpi (punti per pollice) dello schermo con le dimensioni esatte che dipendono da questa impostazione dpi.</span><span class="sxs-lookup"><span data-stu-id="c9824-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="c9824-299">Per ulteriori informazioni, vedere [specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md) .</span><span class="sxs-lookup"><span data-stu-id="c9824-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="c9824-300">Nell'esempio seguente viene illustrato come viene fatto riferimento a un set di immagini specifiche di dpi nel markup:</span><span class="sxs-lookup"><span data-stu-id="c9824-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="c9824-301">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9824-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9824-302">Specifica delle risorse dell'immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="c9824-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 