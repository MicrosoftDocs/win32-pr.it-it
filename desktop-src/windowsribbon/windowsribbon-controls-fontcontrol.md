---
title: Controllo carattere
description: Per semplificare l'integrazione e la configurazione del supporto per i tipi di carattere nelle applicazioni che richiedono l'elaborazione di testi e le funzionalità di modifica del testo, il Framework della barra multifunzione di Windows fornisce un controllo del tipo di carattere specializzato che espone un'ampia gamma di proprietà dei tipi di carattere, ad esempio il nome tipografico, lo stile
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399283"
---
# <a name="font-control"></a><span data-ttu-id="d5ae3-103">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-103">Font Control</span></span>

<span data-ttu-id="d5ae3-104">Per semplificare l'integrazione e la configurazione del supporto per i tipi di carattere nelle applicazioni che richiedono l'elaborazione di testi e le funzionalità di modifica del testo, il Framework della barra multifunzione di Windows fornisce un controllo del tipo di carattere specializzato che espone un'ampia gamma di proprietà dei tipi di carattere, ad esempio il nome tipografico, lo stile</span><span class="sxs-lookup"><span data-stu-id="d5ae3-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="d5ae3-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d5ae3-106">Esperienza coerente</span><span class="sxs-lookup"><span data-stu-id="d5ae3-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="d5ae3-107">Facile integrazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="d5ae3-108">Allineamento con strutture di testo GDI comuni</span><span class="sxs-lookup"><span data-stu-id="d5ae3-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="d5ae3-109">Aggiungere un FontControl</span><span class="sxs-lookup"><span data-stu-id="d5ae3-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="d5ae3-110">Dichiarazione di un FontControl nel markup</span><span class="sxs-lookup"><span data-stu-id="d5ae3-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="d5ae3-111">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="d5ae3-112">Definire un gestore di comandi FontControl</span><span class="sxs-lookup"><span data-stu-id="d5ae3-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="d5ae3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5ae3-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d5ae3-114">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-114">Introduction</span></span>

<span data-ttu-id="d5ae3-115">Il controllo del tipo di carattere è un controllo composto costituito da pulsanti, pulsanti di attivazione, caselle di riepilogo a discesa e caselle combinate, tutti usati per specificare una particolare proprietà del tipo di carattere o un'opzione di formattazione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="d5ae3-116">Lo screenshot seguente mostra il controllo del tipo di carattere della barra multifunzione in WordPad per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="d5ae3-118">Esperienza coerente</span><span class="sxs-lookup"><span data-stu-id="d5ae3-118">A Consistent Experience</span></span>

<span data-ttu-id="d5ae3-119">Come controllo della barra multifunzione incorporato, il controllo del tipo di carattere migliora le funzionalità generali di gestione dei caratteri, selezione e formattazione e offre un'esperienza utente avanzata e coerente in tutte le applicazioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="d5ae3-120">Questa esperienza coerente include</span><span class="sxs-lookup"><span data-stu-id="d5ae3-120">This consistent experience includes</span></span>

-   <span data-ttu-id="d5ae3-121">Formattazione standardizzata e selezione di tipi di carattere nelle applicazioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="d5ae3-122">Rappresentazione dei tipi di carattere standardizzata nelle applicazioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="d5ae3-123">Automatica, in Windows 7, attivazione dei tipi di carattere basata sull'impostazione **Mostra** o **Nascondi** per ogni tipo di carattere nel pannello di controllo dei **tipi** di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="d5ae3-124">Il controllo font Visualizza solo i tipi di carattere impostati per la **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="d5ae3-125">In Windows Vista, il pannello di controllo dei **tipi di carattere** non offre la funzionalità **Mostra** o **Nascondi** , quindi tutti i tipi di carattere sono attivati.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="d5ae3-126">Gestione dei tipi di carattere disponibile direttamente dal controllo.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="d5ae3-127">Lo screenshot seguente mostra che è possibile accedere al pannello di controllo dei **tipi di carattere** direttamente dal controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![screenshot dell'elenco di famiglie di caratteri in WordPad per Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="d5ae3-129">Supporto per l'anteprima automatica.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="d5ae3-130">Esposizione dei tipi di carattere più rilevanti per un utente, ad esempio</span><span class="sxs-lookup"><span data-stu-id="d5ae3-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="d5ae3-131">Elenchi di tipi di carattere localizzati per gli utenti internazionali.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="d5ae3-132">Elenchi di tipi di carattere basati sul dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="d5ae3-133">Il supporto per questa funzionalità non è disponibile in nessuna piattaforma precedente a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="d5ae3-134">Facile integrazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="d5ae3-135">Grazie alla funzionalità standard, riutilizzabile e facilmente utilizzata, il controllo del tipo di carattere della barra multifunzione semplifica l'integrazione del supporto dei tipi di carattere in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="d5ae3-136">I dettagli della selezione e della formattazione dei tipi di carattere sono racchiusi in un elemento logico autonomo che</span><span class="sxs-lookup"><span data-stu-id="d5ae3-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="d5ae3-137">Elimina la gestione complessa delle interdipendenze del controllo tipiche delle implementazioni del controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="d5ae3-138">Richiede un singolo gestore di comando per tutte le funzionalità esposte dai controlli secondari del controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="d5ae3-139">Questo unico gestore comando consente al controllo del tipo di carattere di gestire internamente la funzionalità di vari controlli secondari; un sottocontrollo non interagisce mai direttamente con l'applicazione, indipendentemente dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="d5ae3-140">Altre funzionalità del controllo del tipo di carattere includono</span><span class="sxs-lookup"><span data-stu-id="d5ae3-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="d5ae3-141">Generazione automatica in grado di riconoscere DPI di un oggetto WYSIWYG (elementi visualizzati) rappresentazione bitmap per ogni tipo di carattere nel menu della **famiglia di caratteri** .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="d5ae3-142">Integrazione di [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="d5ae3-143">Bitmap e descrizioni comandi della famiglia di caratteri localizzati.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="d5ae3-144">Enumerazione del tipo di carattere, raggruppamento e metadati per la gestione e la presentazione di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="d5ae3-145">Il supporto per questa funzionalità non è disponibile in nessuna piattaforma precedente a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="d5ae3-146">Il colore del **testo** e i [selettori](windowsribbon-controls-dropdowncolorpicker.md) di colore dell' **evidenziazione del testo** che riflettono il comportamento della selezione colori a discesa della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="d5ae3-147">Supporto dell'anteprima automatica da parte di tutti i controlli secondari basati sulla raccolta di controlli del tipo di carattere: **famiglia di caratteri**, **dimensioni del carattere**, colore del **testo** e **colore di evidenziazione del testo**.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="d5ae3-148">Allineamento con strutture di testo GDI comuni</span><span class="sxs-lookup"><span data-stu-id="d5ae3-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="d5ae3-149">I componenti dello stack di testo di [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) vengono utilizzati per esporre la funzionalità di selezione e formattazione del tipo di carattere tramite il controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="d5ae3-150">Le varie funzionalità del tipo di carattere supportate dalla struttura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), dalla struttura [ChooseFont](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e dalla [struttura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) sono esposte tramite i controlli secondari inclusi nel controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="d5ae3-151">I controlli secondari visualizzati nel controllo del tipo di carattere dipendono dal modello *FontType* dichiarato nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="d5ae3-152">I modelli *FontType* , descritti in dettaglio nella sezione seguente, sono progettati per essere allineati alle strutture di testo comuni di [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="d5ae3-153">Aggiungere un FontControl</span><span class="sxs-lookup"><span data-stu-id="d5ae3-153">Add a FontControl</span></span>

<span data-ttu-id="d5ae3-154">In questa sezione vengono descritti i passaggi di base per l'aggiunta di un controllo del tipo di carattere a un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="d5ae3-155">Dichiarazione di un FontControl nel markup</span><span class="sxs-lookup"><span data-stu-id="d5ae3-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="d5ae3-156">Analogamente ad altri controlli della barra multifunzione, il controllo del tipo di carattere viene dichiarato nel markup con un elemento [**FontControl**](windowsribbon-element-fontcontrol.md) e associato a una dichiarazione di comando tramite un ID di comando.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="d5ae3-157">Quando l'applicazione viene compilata, l'ID comando viene usato per associare il comando a un gestore di comando nell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="d5ae3-158">Se non viene dichiarato alcun ID di comando con [**FontControl**](windowsribbon-element-fontcontrol.md) nel markup, ne viene generato uno dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="d5ae3-159">Poiché i controlli secondari del controllo del tipo di carattere non sono esposti direttamente, la personalizzazione del controllo del tipo di carattere è limitata a tre modelli di layout *FontType* definiti dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="d5ae3-160">Una maggiore personalizzazione del controllo del tipo di carattere può essere eseguita combinando il modello di layout con attributi [**FontControl**](windowsribbon-element-fontcontrol.md) , ad esempio *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* e *IsUnderlineButtonVisible*.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="d5ae3-161">Le funzionalità dei tipi di carattere oltre a quelle esposte dagli attributi e dai modelli di controllo dei tipi di carattere standard richiedono un'implementazione del controllo del tipo di carattere personalizzata che esula dall'ambito di</span><span class="sxs-lookup"><span data-stu-id="d5ae3-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="d5ae3-162">Nella tabella seguente sono elencati i modelli di controllo dei tipi di carattere e il tipo di controllo di modifica a cui è allineato ogni modello.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="d5ae3-163">Modello</span><span class="sxs-lookup"><span data-stu-id="d5ae3-163">Template</span></span>      | <span data-ttu-id="d5ae3-164">Supporti</span><span class="sxs-lookup"><span data-stu-id="d5ae3-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d5ae3-165">FontOnly</span><span class="sxs-lookup"><span data-stu-id="d5ae3-165">FontOnly</span></span>      | [<span data-ttu-id="d5ae3-166">LOGFONT (struttura)</span><span class="sxs-lookup"><span data-stu-id="d5ae3-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="d5ae3-167">FontWithColor</span><span class="sxs-lookup"><span data-stu-id="d5ae3-167">FontWithColor</span></span> | [<span data-ttu-id="d5ae3-168">Struttura CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="d5ae3-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="d5ae3-169">RichFont</span><span class="sxs-lookup"><span data-stu-id="d5ae3-169">RichFont</span></span>      | [<span data-ttu-id="d5ae3-170">Struttura CHARFORMAT2</span><span class="sxs-lookup"><span data-stu-id="d5ae3-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="d5ae3-171">Nella tabella seguente sono elencati i controlli associati a ogni modello e vengono identificati i controlli facoltativi per un modello associato.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="d5ae3-172">Controlli</span><span class="sxs-lookup"><span data-stu-id="d5ae3-172">Controls</span></span>

<span data-ttu-id="d5ae3-173">Modelli</span><span class="sxs-lookup"><span data-stu-id="d5ae3-173">Templates</span></span>

<span data-ttu-id="d5ae3-174">**RichFont**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-174">**RichFont**</span></span>

<span data-ttu-id="d5ae3-175">**FontWithColor**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-175">**FontWithColor**</span></span>

<span data-ttu-id="d5ae3-176">**FontOnly**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-176">**FontOnly**</span></span>

<span data-ttu-id="d5ae3-177">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d5ae3-177">Default</span></span>

<span data-ttu-id="d5ae3-178">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="d5ae3-178">Optional</span></span>

<span data-ttu-id="d5ae3-179">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d5ae3-179">Default</span></span>

<span data-ttu-id="d5ae3-180">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="d5ae3-180">Optional</span></span>

<span data-ttu-id="d5ae3-181">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d5ae3-181">Default</span></span>

<span data-ttu-id="d5ae3-182">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="d5ae3-182">Optional</span></span>

<span data-ttu-id="d5ae3-183">Casella combinata **dimensione carattere**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-183">**Font size** combo box</span></span>

<span data-ttu-id="d5ae3-184">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-184">Yes</span></span>

<span data-ttu-id="d5ae3-185">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-185">No</span></span>

<span data-ttu-id="d5ae3-186">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-186">Yes</span></span>

<span data-ttu-id="d5ae3-187">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-187">No</span></span>

<span data-ttu-id="d5ae3-188">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-188">Yes</span></span>

<span data-ttu-id="d5ae3-189">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-189">No</span></span>

<span data-ttu-id="d5ae3-190">Casella combinata della **famiglia di caratteri**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-190">**Font family** combo box</span></span>

<span data-ttu-id="d5ae3-191">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-191">Yes</span></span>

<span data-ttu-id="d5ae3-192">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-192">No</span></span>

<span data-ttu-id="d5ae3-193">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-193">Yes</span></span>

<span data-ttu-id="d5ae3-194">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-194">No</span></span>

<span data-ttu-id="d5ae3-195">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-195">Yes</span></span>

<span data-ttu-id="d5ae3-196">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-196">No</span></span>

<span data-ttu-id="d5ae3-197">Pulsante **Grow font**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-197">**Grow font** button</span></span>

<span data-ttu-id="d5ae3-198">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-198">Yes</span></span>

<span data-ttu-id="d5ae3-199">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-199">Yes</span></span>

<span data-ttu-id="d5ae3-200">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-200">Yes</span></span>

<span data-ttu-id="d5ae3-201">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-201">Yes</span></span>

\-

\-

<span data-ttu-id="d5ae3-202">Pulsante **compatta carattere**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-202">**Shrink font** button</span></span>

<span data-ttu-id="d5ae3-203">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-203">Yes</span></span>

<span data-ttu-id="d5ae3-204">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-204">Yes</span></span>

<span data-ttu-id="d5ae3-205">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-205">Yes</span></span>

<span data-ttu-id="d5ae3-206">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-206">Yes</span></span>

\-

\-

<span data-ttu-id="d5ae3-207">Pulsante **grassetto**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-207">**Bold** button</span></span>

<span data-ttu-id="d5ae3-208">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-208">Yes</span></span>

<span data-ttu-id="d5ae3-209">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-209">No</span></span>

<span data-ttu-id="d5ae3-210">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-210">Yes</span></span>

<span data-ttu-id="d5ae3-211">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-211">No</span></span>

<span data-ttu-id="d5ae3-212">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-212">Yes</span></span>

<span data-ttu-id="d5ae3-213">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-213">No</span></span>

<span data-ttu-id="d5ae3-214">Pulsante **corsivo**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-214">**Italic** button</span></span>

<span data-ttu-id="d5ae3-215">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-215">Yes</span></span>

<span data-ttu-id="d5ae3-216">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-216">No</span></span>

<span data-ttu-id="d5ae3-217">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-217">Yes</span></span>

<span data-ttu-id="d5ae3-218">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-218">No</span></span>

<span data-ttu-id="d5ae3-219">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-219">Yes</span></span>

<span data-ttu-id="d5ae3-220">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-220">No</span></span>

<span data-ttu-id="d5ae3-221">Pulsante **sottolineato**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-221">**Underline** button</span></span>

<span data-ttu-id="d5ae3-222">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-222">Yes</span></span>

<span data-ttu-id="d5ae3-223">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-223">No</span></span>

<span data-ttu-id="d5ae3-224">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-224">Yes</span></span>

<span data-ttu-id="d5ae3-225">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-225">Yes</span></span>

<span data-ttu-id="d5ae3-226">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-226">Yes</span></span>

<span data-ttu-id="d5ae3-227">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-227">Yes</span></span>

<span data-ttu-id="d5ae3-228">Pulsante **barrato**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-228">**Strikethrough** button</span></span>

<span data-ttu-id="d5ae3-229">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-229">Yes</span></span>

<span data-ttu-id="d5ae3-230">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-230">No</span></span>

<span data-ttu-id="d5ae3-231">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-231">Yes</span></span>

<span data-ttu-id="d5ae3-232">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-232">Yes</span></span>

<span data-ttu-id="d5ae3-233">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-233">Yes</span></span>

<span data-ttu-id="d5ae3-234">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-234">Yes</span></span>

<span data-ttu-id="d5ae3-235">Pulsante **Indice**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-235">**Subscript** button</span></span>

<span data-ttu-id="d5ae3-236">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-236">Yes</span></span>

<span data-ttu-id="d5ae3-237">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="d5ae3-238">Pulsante **apice**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-238">**Superscript** button</span></span>

<span data-ttu-id="d5ae3-239">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-239">Yes</span></span>

<span data-ttu-id="d5ae3-240">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="d5ae3-241">Pulsante **colore evidenziazione testo**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-241">**Text highlight color** button</span></span>

<span data-ttu-id="d5ae3-242">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-242">Yes</span></span>

<span data-ttu-id="d5ae3-243">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-243">No</span></span>

<span data-ttu-id="d5ae3-244">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-244">Yes</span></span>

<span data-ttu-id="d5ae3-245">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-245">Yes</span></span>

\-

\-

<span data-ttu-id="d5ae3-246">Pulsante **colore testo**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-246">**Text color** button</span></span>

<span data-ttu-id="d5ae3-247">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-247">Yes</span></span>

<span data-ttu-id="d5ae3-248">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-248">No</span></span>

<span data-ttu-id="d5ae3-249">Sì</span><span class="sxs-lookup"><span data-stu-id="d5ae3-249">Yes</span></span>

<span data-ttu-id="d5ae3-250">No</span><span class="sxs-lookup"><span data-stu-id="d5ae3-250">No</span></span>

\-

\-



 

<span data-ttu-id="d5ae3-251">Quando viene dichiarato il comportamento del layout di un controllo del tipo di carattere, il Framework della barra multifunzione fornisce un modello di layout *SizeDefinition* facoltativo, `OneFontControl` , che definisce due configurazioni di sottocontrollo in base alla dimensione della barra multifunzione e allo spazio disponibile per il controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="d5ae3-252">Per ulteriori informazioni, vedere [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="d5ae3-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="d5ae3-253">Aggiunta di un FontControl a una barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="d5ae3-254">Gli esempi di codice seguenti illustrano i requisiti di markup di base per l'aggiunta di un controllo tipo di carattere a una barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="d5ae3-255">Questa sezione di codice mostra il markup della dichiarazione del comando [**FontControl**](windowsribbon-element-fontcontrol.md) , inclusi i comandi di [**tabulazione**](windowsribbon-element-tab.md) e [**gruppo**](windowsribbon-element-group.md) necessari per visualizzare un controllo nella [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="d5ae3-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="d5ae3-256">Questa sezione di codice mostra il markup necessario per dichiarare e associare un [**FontControl**](windowsribbon-element-fontcontrol.md) a un [**comando**](windowsribbon-element-command.md) tramite un ID di comando.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="d5ae3-257">Questo particolare esempio include le dichiarazioni di [**tabulazione**](windowsribbon-element-tab.md) e di [**gruppo**](windowsribbon-element-group.md) , con preferenze di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="d5ae3-258">Aggiunta di un FontControl a un ContextPopup</span><span class="sxs-lookup"><span data-stu-id="d5ae3-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="d5ae3-259">L'aggiunta di un controllo del tipo di carattere a un [popup del contesto](windowsribbon-controls-contextpopup.md) richiede una procedura simile a quella di aggiunta di un controllo tipo di carattere alla barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="d5ae3-260">Tuttavia, un controllo del tipo di carattere in un [**MiniToolbar**](windowsribbon-element-minitoolbar.md) è limitato al set di controlli secondari predefiniti comuni a tutti i modelli di controllo dei tipi di carattere: **famiglia di caratteri**, **dimensioni del carattere**, **grassetto** e **corsivo**.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="d5ae3-261">Gli esempi di codice seguenti illustrano i requisiti di markup di base per aggiungere un controllo del tipo di carattere a un [popup del contesto](windowsribbon-controls-contextpopup.md):</span><span class="sxs-lookup"><span data-stu-id="d5ae3-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="d5ae3-262">Questa sezione di codice mostra il markup della dichiarazione di comando [**FontControl**](windowsribbon-element-fontcontrol.md) necessario per visualizzare un **FontControl** in [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="d5ae3-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="d5ae3-263">Questa sezione di codice mostra il markup necessario per dichiarare e associare un [**FontControl**](windowsribbon-element-fontcontrol.md) a un comando tramite un ID di comando.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="d5ae3-264">Suggerimenti per i tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="d5ae3-264">Keytips</span></span>

<span data-ttu-id="d5ae3-265">Ogni sottocontrollo nel controllo del tipo di carattere della barra multifunzione è accessibile tramite un tasto di scelta rapida o un suggerimento tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="d5ae3-266">Questo suggerimento è predefinito e assegnato a ogni sottocontrollo dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="d5ae3-267">Se un valore dell'attributo del tasto di *Suggerimento* viene assegnato all'elemento [**FontControl**](windowsribbon-element-fontcontrol.md) nel markup, questo valore viene aggiunto come prefisso al suggerimento tasto di definizione definito dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="d5ae3-268">L'applicazione deve applicare una regola a carattere singolo per questo prefisso.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="d5ae3-269">Nella tabella seguente sono elencati i suggerimenti tasti definiti dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5ae3-270">Controllo secondario</span><span class="sxs-lookup"><span data-stu-id="d5ae3-270">Sub-control</span></span></th>
<th><span data-ttu-id="d5ae3-271">Suggerimento tasto</span><span class="sxs-lookup"><span data-stu-id="d5ae3-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5ae3-272">Famiglia di caratteri</span><span class="sxs-lookup"><span data-stu-id="d5ae3-272">Font family</span></span></td>
<td><span data-ttu-id="d5ae3-273">F</span><span class="sxs-lookup"><span data-stu-id="d5ae3-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5ae3-274">Stile carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-274">Font style</span></span></td>
<td><span data-ttu-id="d5ae3-275">T</span><span class="sxs-lookup"><span data-stu-id="d5ae3-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5ae3-276">Dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-276">Font size</span></span></td>
<td><span data-ttu-id="d5ae3-277">S</span><span class="sxs-lookup"><span data-stu-id="d5ae3-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5ae3-278">Espandi carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-278">Grow font</span></span></td>
<td><span data-ttu-id="d5ae3-279">G</span><span class="sxs-lookup"><span data-stu-id="d5ae3-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5ae3-280">Compatta carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-280">Shrink font</span></span></td>
<td><span data-ttu-id="d5ae3-281">K</span><span class="sxs-lookup"><span data-stu-id="d5ae3-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5ae3-282">Grassetto</span><span class="sxs-lookup"><span data-stu-id="d5ae3-282">Bold</span></span></td>
<td><span data-ttu-id="d5ae3-283">B</span><span class="sxs-lookup"><span data-stu-id="d5ae3-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5ae3-284">Corsivo</span><span class="sxs-lookup"><span data-stu-id="d5ae3-284">Italic</span></span></td>
<td><span data-ttu-id="d5ae3-285">I</span><span class="sxs-lookup"><span data-stu-id="d5ae3-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5ae3-286">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="d5ae3-286">Underline</span></span></td>
<td><span data-ttu-id="d5ae3-287">U</span><span class="sxs-lookup"><span data-stu-id="d5ae3-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5ae3-288">barrato</span><span class="sxs-lookup"><span data-stu-id="d5ae3-288">Strikethrough</span></span></td>
<td><span data-ttu-id="d5ae3-289">X</span><span class="sxs-lookup"><span data-stu-id="d5ae3-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5ae3-290">Apice</span><span class="sxs-lookup"><span data-stu-id="d5ae3-290">Superscript</span></span></td>
<td><span data-ttu-id="d5ae3-291">Y o Z</span><span class="sxs-lookup"><span data-stu-id="d5ae3-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d5ae3-292">Se l'attributo del <em>Suggerimento</em> tasto di opzione non è dichiarato nel markup, il suggerimento predefinito è Y; in caso contrario, il suggerimento tasto di opzione predefinito è il <em>Suggerimento</em> + Z.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5ae3-293">Pedice</span><span class="sxs-lookup"><span data-stu-id="d5ae3-293">Subscript</span></span></td>
<td><span data-ttu-id="d5ae3-294">A</span><span class="sxs-lookup"><span data-stu-id="d5ae3-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5ae3-295">Colore carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-295">Font color</span></span></td>
<td><span data-ttu-id="d5ae3-296">C</span><span class="sxs-lookup"><span data-stu-id="d5ae3-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5ae3-297">Evidenziazione carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-297">Font highlight</span></span></td>
<td><span data-ttu-id="d5ae3-298">H</span><span class="sxs-lookup"><span data-stu-id="d5ae3-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d5ae3-299">Il prefisso consigliato per una barra multifunzione di Multilingual User Interface (MUI) EN-US è' F ', come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="d5ae3-300">Lo screenshot seguente illustra i suggerimenti dei tasti di controllo del tipo di carattere così come sono definiti nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![screenshot dei suggerimenti per i tasti di fontcontrol in WordPad per Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="d5ae3-302">File di risorse della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d5ae3-302">The Ribbon Resource File</span></span>

<span data-ttu-id="d5ae3-303">Quando il file di markup viene compilato, viene generato un file di risorse che contiene tutti i riferimenti alle risorse per l'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="d5ae3-304">Esempio di un file di risorse semplice:</span><span class="sxs-lookup"><span data-stu-id="d5ae3-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="d5ae3-305">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-305">Font Control Properties</span></span>

<span data-ttu-id="d5ae3-306">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo del tipo di carattere e i relativi controlli secondari.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="d5ae3-307">In genere, una proprietà del controllo del tipo di carattere viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d5ae3-308">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d5ae3-309">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d5ae3-310">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d5ae3-311">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d5ae3-312">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="d5ae3-313">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="d5ae3-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="d5ae3-314">Note</span><span class="sxs-lookup"><span data-stu-id="d5ae3-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5ae3-315">Interfaccia utente \_ pkey \_ FontProperties</span><span class="sxs-lookup"><span data-stu-id="d5ae3-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="d5ae3-316">Espone, in aggregato come oggetto [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , tutte le proprietà del sottocontrollo del controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="d5ae3-317">Il Framework esegue una query su questa proprietà quando `UI_INVALIDATIONS_VALUE` viene passato come valore di *flag* nella chiamata a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="d5ae3-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="d5ae3-318">Interfaccia utente \_ pkey \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="d5ae3-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="d5ae3-319">Espone, in aggregato come oggetto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , solo le proprietà del controllo del sottocontrollo del tipo di carattere che sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="d5ae3-320">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="d5ae3-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="d5ae3-321">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d5ae3-322">Interfaccia utente \_ pkey \_ abilitata</span><span class="sxs-lookup"><span data-stu-id="d5ae3-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="d5ae3-323">Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="d5ae3-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="d5ae3-324">Oltre alle proprietà supportate dal controllo del tipo di carattere stesso, il Framework della barra multifunzione definisce anche una [chiave di proprietà](windowsribbon-reference-properties.md) per ogni controllo secondario del controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="d5ae3-325">Queste chiavi di proprietà e i relativi valori vengono esposte dal Framework tramite un'implementazione dell'interfaccia [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) che definisce i metodi per la gestione di una raccolta, denominata anche contenitore delle proprietà, di coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="d5ae3-326">L'applicazione converte le strutture dei tipi di carattere in proprietà accessibili tramite i metodi di interfaccia [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="d5ae3-327">Questo modello enfatizza la distinzione tra il controllo del tipo di carattere e i componenti dello stack di testo di Windows Graphics Device Interface (GDI) ([struttura LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [struttura ChooseFont](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e [struttura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) supportati dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="d5ae3-328">Nella tabella seguente sono elencati i singoli controlli e le relative chiavi di proprietà associate.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="d5ae3-329">Controlli</span><span class="sxs-lookup"><span data-stu-id="d5ae3-329">Controls</span></span>                 | <span data-ttu-id="d5ae3-330">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="d5ae3-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="d5ae3-331">Note</span><span class="sxs-lookup"><span data-stu-id="d5ae3-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ae3-332">**Dimensioni carattere**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-332">**Font size**</span></span>            | [<span data-ttu-id="d5ae3-333">\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_</span><span class="sxs-lookup"><span data-stu-id="d5ae3-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="d5ae3-334">Quando viene evidenziata un'esecuzione di testo di dimensioni eterogenee, il Framework della barra multifunzione imposta il controllo della **dimensione del carattere** su Blank e il valore di [UI \_ pkey \_ FontProperties \_ size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) su 0.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="d5ae3-335">Quando si fa clic sul pulsante **Grow font** o **Shrink font** , tutto il testo evidenziato viene ridimensionato, ma viene mantenuta la differenza relativa nelle dimensioni del testo.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d5ae3-336">**Famiglia di caratteri**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-336">**Font family**</span></span>          | [<span data-ttu-id="d5ae3-337">Interfaccia \_ utente \_ pkey \_ famiglia FontProperties</span><span class="sxs-lookup"><span data-stu-id="d5ae3-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="d5ae3-338">I nomi delle famiglie di caratteri GDI variano a seconda delle impostazioni locali del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="d5ae3-339">Di conseguenza, se il valore di [UI \_ pkey \_ FontProperties \_ Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) viene mantenuto nelle sessioni dell'applicazione, tale valore deve essere recuperato in ogni nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d5ae3-340">**Espandi carattere**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-340">**Grow font**</span></span>            | [<span data-ttu-id="d5ae3-341">\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_</span><span class="sxs-lookup"><span data-stu-id="d5ae3-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="d5ae3-342">Vedere **dimensioni carattere**.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d5ae3-343">**Compatta carattere**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-343">**Shrink font**</span></span>          | [<span data-ttu-id="d5ae3-344">\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_</span><span class="sxs-lookup"><span data-stu-id="d5ae3-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="d5ae3-345">Vedere **dimensioni carattere**.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d5ae3-346">**Grassetto**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-346">**Bold**</span></span>                 | [<span data-ttu-id="d5ae3-347">Interfaccia utente \_ pkey \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="d5ae3-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d5ae3-348">**Corsivo**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-348">**Italic**</span></span>               | [<span data-ttu-id="d5ae3-349">Interfaccia utente \_ pkey \_ FontProperties \_ corsivo</span><span class="sxs-lookup"><span data-stu-id="d5ae3-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d5ae3-350">**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-350">**Underline**</span></span>            | [<span data-ttu-id="d5ae3-351">\_ \_ Sottolineato FontProperties pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="d5ae3-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d5ae3-352">**barrato**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-352">**Strikethrough**</span></span>        | [<span data-ttu-id="d5ae3-353">Barra dell'interfaccia utente \_ pkey \_ FontProperties \_</span><span class="sxs-lookup"><span data-stu-id="d5ae3-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d5ae3-354">**Pedice**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-354">**Subscript**</span></span>            | [<span data-ttu-id="d5ae3-355">Interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="d5ae3-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="d5ae3-356">Se viene impostato il pulsante **pedice** , non è possibile impostare anche l' **apice** .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d5ae3-357">**Apice**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-357">**Superscript**</span></span>          | [<span data-ttu-id="d5ae3-358">Interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="d5ae3-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="d5ae3-359">Se il pulsante **apice** è impostato, non è possibile impostare anche il **pedice** .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d5ae3-360">**Colore di evidenziazione testo**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-360">**Text highlight color**</span></span> | <span data-ttu-id="d5ae3-361">[Interfaccia utente \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ pkey \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="d5ae3-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="d5ae3-362">Fornisce la stessa funzionalità del `HighlightColors` modello dell'elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="d5ae3-363">Si consiglia vivamente di impostare l'applicazione solo un valore di **colore di evidenziazione del testo** iniziale.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="d5ae3-364">L'ultimo valore selezionato deve essere mantenuto e non impostato quando il cursore viene riposizionato all'interno di un documento.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="d5ae3-365">In questo modo è possibile accedere rapidamente all'ultima selezione dell'utente e non è necessario riaprire la selezione colori.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="d5ae3-366">I campioni di colore non possono essere personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="d5ae3-367">**Colore del testo**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-367">**Text color**</span></span>           | <span data-ttu-id="d5ae3-368">[Interfaccia utente \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ pkey \_ FontProperties \_ ](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md) ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="d5ae3-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="d5ae3-369">Fornisce la stessa funzionalità del `StandardColors` modello dell'elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ae3-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="d5ae3-370">Si consiglia vivamente di impostare l'applicazione solo un valore di **colore del testo** iniziale.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="d5ae3-371">L'ultimo valore selezionato deve essere mantenuto e non impostato quando il cursore viene riposizionato all'interno di un documento.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="d5ae3-372">In questo modo è possibile accedere rapidamente all'ultima selezione dell'utente e non è necessario riaprire la selezione colori.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="d5ae3-373">I campioni di colore non possono essere personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="d5ae3-374">Definire un gestore di comandi FontControl</span><span class="sxs-lookup"><span data-stu-id="d5ae3-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="d5ae3-375">In questa sezione vengono descritti i passaggi necessari per associare un controllo del tipo di carattere a un gestore comando.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="d5ae3-376">Qualsiasi tentativo di selezionare un campione di colore dalla selezione colori di un controllo del tipo di carattere può causare una violazione di accesso se al controllo non è associato alcun gestore di comando.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="d5ae3-377">Nell'esempio di codice riportato di seguito viene illustrato come associare i comandi dichiarati nel markup a un gestore di comandi.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="d5ae3-378">Nell'esempio di codice seguente viene illustrato come implementare il metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) per un controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="d5ae3-379">Nell'esempio di codice seguente viene illustrato come implementare il metodo [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) per un controllo del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d5ae3-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d5ae3-380">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5ae3-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5ae3-381">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d5ae3-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d5ae3-382">**Elemento FontControl**</span><span class="sxs-lookup"><span data-stu-id="d5ae3-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d5ae3-383">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="d5ae3-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d5ae3-384">Esempio FontControl</span><span class="sxs-lookup"><span data-stu-id="d5ae3-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

