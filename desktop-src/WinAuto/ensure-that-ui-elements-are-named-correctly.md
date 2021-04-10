---
title: Verifica della corretta denominazione degli elementi dell'interfaccia utente
description: In questo argomento viene descritto il modo corretto per specificare i nomi degli elementi dell'interfaccia utente nelle applicazioni Microsoft Win32 in modo che Microsoft Active Accessibility possa esporre accuratamente i nomi alle applicazioni client tramite IAccessible \ 32; Proprietà Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963143"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="4a0b8-103">Verifica della corretta denominazione degli elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4a0b8-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="4a0b8-104">In questo argomento viene descritto il modo corretto per specificare i nomi degli elementi dell'interfaccia utente nelle applicazioni Microsoft Win32 in modo che Microsoft Active Accessibility possa esporre accuratamente i nomi alle applicazioni client tramite la [proprietà nome](name-property.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="4a0b8-105">Le informazioni contenute in questa sezione si applicano solo a Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="4a0b8-106">Non si applica alle applicazioni che utilizzano l'automazione interfaccia utente Microsoft o a quelle basate su linguaggi di markup, ad esempio HTML, DHTML (Dynamic HTML) o XML.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="4a0b8-107">Overview</span><span class="sxs-lookup"><span data-stu-id="4a0b8-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="4a0b8-108">Come la denominazione non corretta causa problemi</span><span class="sxs-lookup"><span data-stu-id="4a0b8-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="4a0b8-109">Come MSAA ottiene la proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="4a0b8-110">Come individuare e correggere i problemi di denominazione</span><span class="sxs-lookup"><span data-stu-id="4a0b8-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="4a0b8-111">Come assegnare un nome corretto a un TrackBar</span><span class="sxs-lookup"><span data-stu-id="4a0b8-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="4a0b8-112">Come usare le etichette invisibili per denominare i controlli</span><span class="sxs-lookup"><span data-stu-id="4a0b8-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="4a0b8-113">Come usare l'annotazione diretta per specificare la proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="4a0b8-114">Passaggi per l'annotazione della proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="4a0b8-115">Esempio di annotazione della proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="4a0b8-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a0b8-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="4a0b8-117">Panoramica</span><span class="sxs-lookup"><span data-stu-id="4a0b8-117">Overview</span></span>

<span data-ttu-id="4a0b8-118">In Microsoft Active Accessibility ogni elemento dell'interfaccia utente in un'applicazione è rappresentato da un oggetto che espone l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="4a0b8-119">Le applicazioni client utilizzano le proprietà e i metodi dell'interfaccia **IAccessible** per interagire con l'elemento dell'interfaccia utente e per recuperare informazioni su di esso.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="4a0b8-120">Una delle proprietà più importanti esposte dall'interfaccia **IAccessible** è la [proprietà Name](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="4a0b8-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="4a0b8-121">Le applicazioni client si basano sulla proprietà Name per trovare, identificare o annunciare un elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="4a0b8-122">Se Microsoft Active Accessibility non è in grado di esporre correttamente la proprietà Name di un particolare elemento dell'interfaccia utente, le applicazioni client non saranno in grado di presentare l'elemento dell'interfaccia utente e l'elemento dell'interfaccia utente sarà inaccessibile agli utenti con particolari esigenze.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="4a0b8-123">Come la denominazione non corretta causa problemi</span><span class="sxs-lookup"><span data-stu-id="4a0b8-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="4a0b8-124">Per illustrare i problemi causati dalla denominazione non corretta degli elementi dell'interfaccia utente, prendere in considerazione il formato della voce di nome illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![illustrazione di un modulo semplice per l'immissione del nome e del cognome](images/incorrect-form.png)

<span data-ttu-id="4a0b8-126">Anche se gli elementi dell'interfaccia utente nel form hanno un aspetto corretto, l'implementazione a livello di codice non è corretta.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="4a0b8-127">A un client di Microsoft Active Accessibility, ad esempio un'Reader per la lettura dello schermo, la [proprietà Name](name-property.md) del controllo top Edit è "Last Name:" e la proprietà Name del controllo Bottom Edit è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="4a0b8-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="4a0b8-128">Il controllo di modifica superiore verrà letto dal lettore dello schermo come "cognome", sebbene l'utente debba digitare il nome.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="4a0b8-129">Il secondo controllo di modifica viene letto come "nessun nome", pertanto l'utente non avrà idea di cosa digitare nel secondo controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="4a0b8-130">L'utente non è in grado di supportare l'immissione di dati in questo semplice modulo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="4a0b8-131">Un altro problema con il modulo è che nessun tasto di scelta rapida viene assegnato a uno dei controlli di modifica.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="4a0b8-132">L'utente è forzato a eseguire una tabulazione sui controlli o usare il mouse.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="4a0b8-133">Le sezioni seguenti illustrano l'origine di questi problemi e forniscono linee guida per correggerli.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="4a0b8-134">Come MSAA ottiene la proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="4a0b8-135">Microsoft Active Accessibility ottiene la stringa della [proprietà Name](name-property.md) da percorsi diversi a seconda del tipo di elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="4a0b8-136">Per la maggior parte degli elementi dell'interfaccia utente a cui è associato il testo della finestra, Microsoft Active Accessibility usa il testo della finestra come stringa della proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="4a0b8-137">Esempi di questo tipo di elemento dell'interfaccia utente includono controlli quali pulsanti, voci di menu e descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="4a0b8-138">Per i seguenti controlli, Microsoft Active Accessibility ignora il testo della finestra e cerca invece un'etichetta di testo statico (o etichetta casella di gruppo) immediatamente prima del controllo nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="4a0b8-139">Caselle combinate</span><span class="sxs-lookup"><span data-stu-id="4a0b8-139">Combo Boxes</span></span>
-   <span data-ttu-id="4a0b8-140">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="4a0b8-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="4a0b8-141">Modifica e controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="4a0b8-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="4a0b8-142">Controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="4a0b8-142">IP Address controls</span></span>
-   <span data-ttu-id="4a0b8-143">Caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="4a0b8-143">List Boxes</span></span>
-   <span data-ttu-id="4a0b8-144">Visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="4a0b8-144">List Views</span></span>
-   <span data-ttu-id="4a0b8-145">Indicatori di stato</span><span class="sxs-lookup"><span data-stu-id="4a0b8-145">Progress Bars</span></span>
-   <span data-ttu-id="4a0b8-146">Barre</span><span class="sxs-lookup"><span data-stu-id="4a0b8-146">Scrollbars</span></span>
-   <span data-ttu-id="4a0b8-147">Controlli statici con \_ icona SS o \_ stile bitmap SS</span><span class="sxs-lookup"><span data-stu-id="4a0b8-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="4a0b8-148">TrackBar</span><span class="sxs-lookup"><span data-stu-id="4a0b8-148">Trackbars</span></span>
-   <span data-ttu-id="4a0b8-149">Visualizzazioni ad albero</span><span class="sxs-lookup"><span data-stu-id="4a0b8-149">Tree Views</span></span>

<span data-ttu-id="4a0b8-150">Se i controlli precedenti non sono accompagnati da etichette di testo statiche o se le etichette non sono implementate correttamente, Microsoft Active Accessibility non è in grado di fornire la [proprietà nome](name-property.md) corretta alle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="4a0b8-151">Alla maggior parte dei controlli precedenti è effettivamente associato il testo della finestra.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="4a0b8-152">L'editor risorse genera automaticamente il testo della finestra, costituito da una stringa generica, ad esempio "Edit1" o "listbox3".</span><span class="sxs-lookup"><span data-stu-id="4a0b8-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="4a0b8-153">Sebbene gli sviluppatori possano sostituire il testo della finestra generata con testo più significativo, la maggior parte mai.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="4a0b8-154">Poiché il testo della finestra generata non ha significato per l'utente, Microsoft Active Accessibility lo ignora e usa invece l'etichetta di testo statico associata.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="4a0b8-155">Come individuare e correggere i problemi di denominazione</span><span class="sxs-lookup"><span data-stu-id="4a0b8-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="4a0b8-156">Nel modulo di immissione del nome illustrato in che modo la denominazione errata causa problemi, la causa dei problemi è che l'ordine di tabulazione dei controlli non è corretto.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="4a0b8-157">Esaminando l'interfaccia utente con uno strumento di test come [ispeziona](inspect-objects.md) , si riveleranno i problemi della gerarchia di oggetti.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="4a0b8-158">Lo screenshot seguente mostra la gerarchia di oggetti interrotta del modulo di immissione del nome come appare in ispeziona.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![screenshot dello strumento di controllo che mostra una gerarchia di oggetti non corretta del modulo di immissione del nome](images/incorrect-object-hierarchy.png)

<span data-ttu-id="4a0b8-160">Nello screenshot precedente si noti che la gerarchia di oggetti non corrisponde alla struttura dei controlli così come appaiono nell'interfaccia utente del modulo di immissione del nome.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="4a0b8-161">Si noti inoltre che l' [ispezione](inspect-objects.md) ha assegnato il nome errato all'elemento successivo all'ultimo (si tratta del controllo di modifica per l'immissione del nome e deve essere un nome denominato "First Name:".</span><span class="sxs-lookup"><span data-stu-id="4a0b8-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="4a0b8-162">Infine, si noti che ispezionare non è stato in grado di trovare un nome per l'ultimo elemento. si tratta del controllo di modifica per l'immissione del cognome e deve avere il nome "Cognome:".</span><span class="sxs-lookup"><span data-stu-id="4a0b8-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="4a0b8-163">Nell'esempio seguente viene illustrato il contenuto del file di risorse per il form di immissione del nome.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="4a0b8-164">Si noti che l'ordine di tabulazione non è coerente con la struttura logica dei controlli così come appaiono nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="4a0b8-165">Si noti inoltre che non viene specificato alcun tasto di scelta rapida per i due controlli di modifica.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="4a0b8-166">Per correggere i problemi con il modulo di immissione del nome, è necessario modificare il file di risorse (RC) per specificare i tasti di scelta rapida e i controlli devono essere inseriti nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="4a0b8-167">Etichetta di testo statico "&First Name:".</span><span class="sxs-lookup"><span data-stu-id="4a0b8-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="4a0b8-168">Controllo di modifica per l'immissione del nome (IDC \_ EDIT1).</span><span class="sxs-lookup"><span data-stu-id="4a0b8-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="4a0b8-169">Etichetta di testo statico "&Last Name:".</span><span class="sxs-lookup"><span data-stu-id="4a0b8-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="4a0b8-170">Controllo di modifica per l'immissione del cognome (IDC \_ Edit2).</span><span class="sxs-lookup"><span data-stu-id="4a0b8-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="4a0b8-171">Pulsante di push predefinito "OK".</span><span class="sxs-lookup"><span data-stu-id="4a0b8-171">The "OK" default push button.</span></span>

<span data-ttu-id="4a0b8-172">Nell'esempio seguente viene illustrato il file di risorse corretto per il form di immissione del nome:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="4a0b8-173">Per apportare correzioni a un file di risorse, è possibile modificare direttamente il file oppure utilizzare lo strumento di ordine di tabulazione in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="4a0b8-174">Per accedere allo strumento per l'ordine di tabulazione in Visual Studio, è possibile premere CTRL + D oppure selezionare **Tab Order** dal menu **formato** .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="4a0b8-175">Dopo la correzione e la ricompilazione dell'applicazione, l'interfaccia utente del form di immissione dei nomi sarà analoga a quella precedente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="4a0b8-176">Tuttavia, in Microsoft Active Accessibility verranno ora fornite le proprietà nome corrette per le applicazioni client e lo stato attivo verrà impostato correttamente quando l'utente preme i tasti di scelta rapida ALT + F o ALT + L.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="4a0b8-177">Inoltre, il [controllo](inspect-objects.md) visualizzerà la gerarchia di oggetti corretta, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![screenshot dello strumento di esplorazione accessibile che mostra una gerarchia di oggetti corretta del modulo di immissione del nome](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="4a0b8-179">Come assegnare un nome corretto a un TrackBar</span><span class="sxs-lookup"><span data-stu-id="4a0b8-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="4a0b8-180">Quando si definisce un TrackBar (o un dispositivo di scorrimento), assicurarsi che l'etichetta di testo statico principale per il controllo TrackBar venga visualizzata prima del TrackBar e che le etichette di testo statiche per gli intervalli minimo e massimo vengano visualizzate dopo il controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="4a0b8-181">Tenere presente che Microsoft Active Accessibility usa l'etichetta di testo statico che precede immediatamente un controllo come [proprietà Name](name-property.md) per il controllo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="4a0b8-182">Inserendo l'etichetta di testo statico principale immediatamente prima del TrackBar e le altre etichette dopo di essa, garantisce che Microsoft Active Accessibility fornisca la proprietà Name corretta a un client.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="4a0b8-183">Nella figura seguente viene illustrato un TrackBar tipico con un'etichetta di testo statico principale denominata "Speed" e le etichette di testo statico per gli intervalli minimo ("min") e Maximum ("Max").</span><span class="sxs-lookup"><span data-stu-id="4a0b8-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![illustrazione di un controllo TrackBar con un'etichetta principale ed etichette per gli intervalli minimo e massimo](images/speed-trackbar.png)

<span data-ttu-id="4a0b8-185">Nell'esempio seguente viene illustrato il modo corretto per definire un TrackBar e le relative etichette di testo statiche nel file di risorse:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="4a0b8-186">Come usare le etichette invisibili per denominare i controlli</span><span class="sxs-lookup"><span data-stu-id="4a0b8-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="4a0b8-187">Non è sempre possibile o auspicabile avere un'etichetta visibile per ogni controllo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="4a0b8-188">Talvolta, ad esempio, l'aggiunta di etichette può causare modifiche indesiderate nell'aspetto dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="4a0b8-189">In questo caso, è possibile usare le etichette invisibili.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="4a0b8-190">Microsoft Active Accessibility rileverà comunque il testo associato a un'etichetta invisibile, ma l'etichetta non verrà visualizzata o interferirà con l'interfaccia utente visiva.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="4a0b8-191">Come per le etichette visibili, un'etichetta invisibile deve precedere immediatamente il controllo nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="4a0b8-192">Per rendere invisibile un'etichetta in un file di risorse (RC), aggiungere `NOT WS_VISIBLE` o `|~WS_VISIBLE` alla parte di stile del controllo testo statico.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="4a0b8-193">Se si usa l'editor di risorse in Visual Studio, è possibile impostare la proprietà Visible su false.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="4a0b8-194">Come usare l'annotazione diretta per specificare la proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="4a0b8-195">I proxy predefiniti inclusi nel componente runtime di Microsoft Active Accessibility, Oleacc.dll, forniscono automaticamente un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per tutti i controlli Windows standard.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="4a0b8-196">Se si personalizza un controllo Windows standard, i proxy predefiniti eseguono le operazioni migliori per fornire in modo accurato tutte le proprietà **IAccessible** per il controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="4a0b8-197">È necessario testare accuratamente un controllo personalizzato per assicurarsi che i proxy predefiniti forniscano valori di proprietà accurati e completi.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="4a0b8-198">Se il test rivela valori di proprietà non accurati o incompleti, potrebbe essere possibile utilizzare la tecnica di annotazione dinamica denominata annotazione diretta per fornire valori di proprietà corretti e aggiungere quelli mancanti.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="4a0b8-199">Si noti che l'annotazione dinamica non è solo per i controlli supportati dai proxy di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="4a0b8-200">È anche possibile usarlo per modificare o fornire proprietà per qualsiasi controllo che fornisce la propria implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="4a0b8-201">Questa sezione è incentrata sull'uso dell'annotazione diretta per fornire un valore corretto per la [proprietà Name](name-property.md) dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="4a0b8-202">È possibile utilizzare l'annotazione diretta per fornire anche altri valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="4a0b8-203">Sono inoltre disponibili altre tecniche di annotazione dinamica accanto all'annotazione diretta e le funzionalità e le funzionalità dell'API di annotazione dinamica si estendono oltre quanto descritto in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="4a0b8-204">Per altre informazioni sull'annotazione dinamica, vedere [API di annotazione dinamica](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="4a0b8-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="4a0b8-205">Passaggi per l'annotazione della proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="4a0b8-206">L'uso dell'annotazione diretta per modificare la [proprietà Name](name-property.md) di un controllo prevede i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="4a0b8-207">Includere i file di intestazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-207">Include the following header files:</span></span>
    -   <span data-ttu-id="4a0b8-208">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="4a0b8-208">Initguid.h</span></span>
    -   <span data-ttu-id="4a0b8-209">Oleacc. h</span><span class="sxs-lookup"><span data-stu-id="4a0b8-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="4a0b8-210">Per definire i GUID, è necessario includere Initguid. h prima di oleacc. h nello stesso file.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="4a0b8-211">Inizializzare la libreria Component Object Model (COM) chiamando la funzione [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , in genere durante il processo di inizializzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="4a0b8-212">Subito dopo la creazione del controllo di destinazione (in genere durante il messaggio [WM \_ INITDIALOG](../dlgbox/wm-initdialog.md) ), creare un'istanza di gestione annotazioni e ottenere un puntatore al relativo puntatore [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="4a0b8-213">Annotare la [proprietà Name](name-property.md) del controllo di destinazione usando il metodo [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="4a0b8-214">Rilasciare il puntatore [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="4a0b8-215">Prima che il controllo di destinazione venga eliminato definitivamente (in genere durante la gestione del messaggio [WM \_ Destroy](../winmsg/wm-destroy.md) ), creare un'istanza di gestione annotazioni e ottenere un puntatore alla relativa interfaccia [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="4a0b8-216">Usare il metodo [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) per cancellare le annotazioni della [proprietà Name](name-property.md) dal controllo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="4a0b8-217">Rilasciare il puntatore [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="4a0b8-218">Prima di uscire dall'applicazione (in genere durante l'elaborazione del messaggio [WM \_ Destroy](../winmsg/wm-destroy.md) ), rilasciare la libreria COM chiamando la funzione [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="4a0b8-219">La funzione [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) accetta cinque parametri.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="4a0b8-220">I primi tre, ovvero *HWND*, *idObject* e *idChild*, vengono combinati per identificare il controllo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="4a0b8-221">Il quarto parametro, *idProp*, specifica l'identificatore della proprietà da modificare.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="4a0b8-222">Per modificare la [proprietà Name](name-property.md), impostare *idProp* su **propid \_ ACC \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="4a0b8-223">Per un elenco di altre proprietà che è possibile impostare tramite l'annotazione diretta, vedere [uso dell'annotazione diretta](using-direct-annotation.md). L'ultimo parametro di **SetHwndPropStr**, *Str*, è la nuova stringa da usare come proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="4a0b8-224">Esempio di annotazione della proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="4a0b8-225">Nell'esempio di codice seguente viene illustrato come utilizzare l'annotazione diretta per modificare la [proprietà Name](name-property.md) dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="4a0b8-226">Per semplificare le operazioni, nell'esempio viene utilizzata una stringa hardcoded ("nuovo nome controllo") per impostare la proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="4a0b8-227">Le stringhe hardcoded non devono essere usate nella versione finale dell'applicazione perché non possono essere localizzate.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="4a0b8-228">Al contrario, caricare sempre le stringhe dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="4a0b8-229">Inoltre, nell'esempio non vengono visualizzate le chiamate alle funzioni [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4a0b8-230">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a0b8-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4a0b8-231">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4a0b8-232">API di annotazione dinamica</span><span class="sxs-lookup"><span data-stu-id="4a0b8-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="4a0b8-233">Specifica della proprietà Name</span><span class="sxs-lookup"><span data-stu-id="4a0b8-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="4a0b8-234">Strumenti di test</span><span class="sxs-lookup"><span data-stu-id="4a0b8-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 