---
title: Alternative all'annotazione dinamica
description: Alternative all'annotazione dinamica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117994"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="72fd1-103">Alternative all'annotazione dinamica</span><span class="sxs-lookup"><span data-stu-id="72fd1-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="72fd1-104">Esistono altri modi per fornire supporto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personalizzato per gli elementi dell'interfaccia utente e in alcuni casi sono la soluzione corretta.</span><span class="sxs-lookup"><span data-stu-id="72fd1-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="72fd1-105">Prima dell'annotazione dinamica, queste tecniche alternative erano le uniche opzioni disponibili per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="72fd1-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="72fd1-106">Sono incluse l'implementazione di tutte le tecniche di interfaccia **IAccessible** e a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="72fd1-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="72fd1-107">Implementazione di tutta l'interfaccia IAccessible</span><span class="sxs-lookup"><span data-stu-id="72fd1-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="72fd1-108">Una tecnica alternativa consiste nell'implementare tutte le interfacce [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="72fd1-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="72fd1-109">Questo approccio è spesso necessario per i controlli personalizzati o per gli elementi dell'interfaccia utente radicalmente diversi. Tuttavia, i costi di sviluppo e test sono sufficientemente significativi da evitare, a meno che non sia effettivamente necessario.</span><span class="sxs-lookup"><span data-stu-id="72fd1-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="72fd1-110">Se l'obiettivo è modificare una singola proprietà, è difficile giustificare il costo.</span><span class="sxs-lookup"><span data-stu-id="72fd1-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="72fd1-111">Tecniche programmatiche</span><span class="sxs-lookup"><span data-stu-id="72fd1-111">Programmatic Techniques</span></span>

<span data-ttu-id="72fd1-112">Un'altra opzione consiste nell'usare le tecniche di sottoclasse e di wrapping per modificare le informazioni esposte per una proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="72fd1-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="72fd1-113">Questa è la tecnica che l'annotazione dinamica deve sostituire.</span><span class="sxs-lookup"><span data-stu-id="72fd1-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="72fd1-114">Per eseguire l'override di una singola proprietà usando la sottoclasse e il wrapping, lo sviluppatore deve eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="72fd1-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="72fd1-115">Sottoclasse HWND dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="72fd1-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="72fd1-116">Intercettare il messaggio [**WM \_ GetObject**](wm-getobject.md) per il valore IParam/ObjID corretto.</span><span class="sxs-lookup"><span data-stu-id="72fd1-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="72fd1-117">Inviare il messaggio [**WM \_ GetObject**](wm-getobject.md) alla classe di base usando la funzione [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="72fd1-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="72fd1-118">Se viene restituito zero, chiamare [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); in caso contrario, chiamare [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) sul valore restituito per ottenere il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa del controllo.</span><span class="sxs-lookup"><span data-stu-id="72fd1-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="72fd1-119">Creare una classe wrapper che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ed esegue il wrapping del puntatore all'interfaccia **IAccessible** restituito dal passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="72fd1-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="72fd1-120">Questa classe wrapper Invia tutti i metodi e le proprietà al puntatore all'interfaccia **IAccessible** originale, ad eccezione di quelli che devono essere sottoposti a override.</span><span class="sxs-lookup"><span data-stu-id="72fd1-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="72fd1-121">Questa operazione comporta la scrittura di codice di invio per tutte le proprietà e i metodi dell'interfaccia **IAccessible** , indipendentemente dal numero di cui viene effettivamente eseguito l'override.</span><span class="sxs-lookup"><span data-stu-id="72fd1-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="72fd1-122">Inoltre, gli sviluppatori devono verificare le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="72fd1-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="72fd1-123">Il metodo o la proprietà sottoposta a override deve gestire solo gli ID figlio richiesti e trasmettere tutti gli altri al puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale.</span><span class="sxs-lookup"><span data-stu-id="72fd1-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="72fd1-124">Il wrapping deve anche trasmettere le interfacce [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) e [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) solo se l'oggetto originale lo supporta.</span><span class="sxs-lookup"><span data-stu-id="72fd1-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="72fd1-125">Il conteggio dei riferimenti deve essere gestito correttamente, soprattutto se sono supportate altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="72fd1-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="72fd1-126">I valori restituiti [**IDispatch**](idispatch-interface.md) devono essere gestiti correttamente, in particolare con il metodo [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , che deve essere chiamato con un puntatore di interfaccia all'interfaccia wrapper, non un puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale.</span><span class="sxs-lookup"><span data-stu-id="72fd1-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="72fd1-127">Queste tecniche richiedono una notevole quantità di lavoro, anche se è necessario eseguire l'override di una o due proprietà.</span><span class="sxs-lookup"><span data-stu-id="72fd1-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="72fd1-128">La maggior parte del codice risultante riguarda la creazione di sottoclassi e il wrapping e solo una piccola frazione fornisce effettivamente le informazioni sottoposte a override.</span><span class="sxs-lookup"><span data-stu-id="72fd1-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="72fd1-129">Tuttavia, esistono scenari in cui sono necessarie queste tecniche.</span><span class="sxs-lookup"><span data-stu-id="72fd1-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="72fd1-130">Se ad esempio si apportano modifiche strutturali per creare un elemento dell'interfaccia utente segnaposto, è consigliabile usare queste tecniche anziché l'annotazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="72fd1-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="72fd1-131">Correzione dei nomi derivati dalle etichette</span><span class="sxs-lookup"><span data-stu-id="72fd1-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="72fd1-132">Alcuni controlli comuni di Microsoft Win32, ad esempio il controllo casella di modifica, vengono quasi sempre usati con un'etichetta (una voce LTEXT nel file di risorse) o una casella di gruppo (GROUPBOX nel file di risorse).</span><span class="sxs-lookup"><span data-stu-id="72fd1-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="72fd1-133">Microsoft Active Accessibility deriva automaticamente dalla relativa etichetta la proprietà Name del controllo.</span><span class="sxs-lookup"><span data-stu-id="72fd1-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="72fd1-134">Per tali controlli, il testo della finestra (visualizzato in Microsoft Visual Studio come nome o proprietà ID) viene ignorato, perché in genere è generato automaticamente e raramente molto descrittivo; ad esempio, "IDC \_ EDIT1".</span><span class="sxs-lookup"><span data-stu-id="72fd1-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="72fd1-135">Se l'interfaccia utente dell'applicazione non è progettata correttamente, Microsoft Active Accessibility potrebbe non essere in grado di impostare correttamente il nome.</span><span class="sxs-lookup"><span data-stu-id="72fd1-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="72fd1-136">Per essere associato a un controllo, la casella etichetta o gruppo deve essere posizionata immediatamente prima del controllo dinamico nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="72fd1-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="72fd1-137">È possibile modificare l'ordine di tabulazione usando lo strumento in Visual Studio (dal menu **formato** quando l'editor risorse è aperto) o modificando direttamente il file di risorse.</span><span class="sxs-lookup"><span data-stu-id="72fd1-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="72fd1-138">Nell'esempio seguente viene illustrata la descrizione di un file di risorse di una finestra di dialogo contenente due caselle di modifica con etichetta.</span><span class="sxs-lookup"><span data-stu-id="72fd1-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



<span data-ttu-id="72fd1-139">In questo esempio le etichette e i controlli non sono elencati nell'ordine di tabulazione corretto.</span><span class="sxs-lookup"><span data-stu-id="72fd1-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="72fd1-140">Di conseguenza, Microsoft Active Accessibility assegna il nome "cognome" alla casella di modifica First-Name e nessun nome alla casella di modifica Last-Name.</span><span class="sxs-lookup"><span data-stu-id="72fd1-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="72fd1-141">Nell'esempio seguente viene illustrato l'elenco di risorse corretto.</span><span class="sxs-lookup"><span data-stu-id="72fd1-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="72fd1-142">Si noti anche che i tasti di scelta rapida sono stati designati nelle etichette.</span><span class="sxs-lookup"><span data-stu-id="72fd1-142">Note also that shortcut keys have been designated in the labels.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



<span data-ttu-id="72fd1-143">Quando i controlli hanno etichette supplementari, ad esempio per i valori minimo e massimo in un TrackBar, queste etichette devono essere posizionate dopo il controllo nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="72fd1-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="72fd1-144">L'etichetta principale del controllo deve apparire immediatamente prima del controllo stesso.</span><span class="sxs-lookup"><span data-stu-id="72fd1-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="72fd1-145">Denominazione dei controlli senza etichette</span><span class="sxs-lookup"><span data-stu-id="72fd1-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="72fd1-146">Non è sempre possibile o auspicabile avere un'etichetta visibile per ogni controllo.</span><span class="sxs-lookup"><span data-stu-id="72fd1-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="72fd1-147">Tuttavia, è comunque possibile specificare un nome per il controllo aggiungendo un'etichetta invisibile.</span><span class="sxs-lookup"><span data-stu-id="72fd1-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="72fd1-148">Come sempre, l'etichetta invisibile deve precedere immediatamente il controllo nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="72fd1-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="72fd1-149">Se si usa l'editor di risorse in Microsoft Visual Studio .NET, è possibile impostare la proprietà Visible su false.</span><span class="sxs-lookup"><span data-stu-id="72fd1-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="72fd1-150">Per rendere invisibile l'etichetta quando si modifica il file di risorse (RC), aggiungere NOT WS \_ Visible o alla parte Style del controllo Label, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="72fd1-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="72fd1-151">Si noti che qualsiasi tasto di scelta rapida designato funziona anche se l'etichetta è invisibile.</span><span class="sxs-lookup"><span data-stu-id="72fd1-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 