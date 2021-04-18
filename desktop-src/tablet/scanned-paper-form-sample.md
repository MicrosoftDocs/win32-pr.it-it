---
description: In questo esempio di C \# , un modulo cartaceo è stato analizzato come file di Portable Network Graphics (png) e specificato come immagine di sfondo in fase di esecuzione per un controllo InkPicture. Nell'esempio viene utilizzata una finestra di messaggio per visualizzare i risultati del riconoscimento della grafia.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Esempio di modulo cartaceo analizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314900"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="cd97e-104">Esempio di modulo cartaceo analizzato</span><span class="sxs-lookup"><span data-stu-id="cd97e-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="cd97e-105">In questo esempio di C \# , un modulo cartaceo è stato analizzato come file di Portable Network Graphics (png) e specificato come immagine di sfondo in fase di esecuzione per un controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="cd97e-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="cd97e-106">Nell'esempio viene utilizzata una finestra di messaggio per visualizzare i risultati del riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="cd97e-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="cd97e-107">Nell'esempio è incluso un file Extensible Markup Language (XML), Formdata.xml.</span><span class="sxs-lookup"><span data-stu-id="cd97e-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="cd97e-108">Il file XML contiene il nome del file PNG.</span><span class="sxs-lookup"><span data-stu-id="cd97e-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="cd97e-109">Contiene anche `FieldInfo` elementi che definiscono aree rettangolari sul form in cui un utente può immettere input penna.</span><span class="sxs-lookup"><span data-stu-id="cd97e-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="cd97e-110">Le informazioni nell' `FieldInfo` elemento sono illustrate nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="cd97e-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="cd97e-111">Gli elementi sinistro, superiore, destro e inferiore sono definizioni delle coordinate dei pixel per ogni campo.</span><span class="sxs-lookup"><span data-stu-id="cd97e-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="cd97e-112">L'esempio Inizializza un nuovo [set](/dotnet/api/system.data.dataset?view=netcore-3.1) di dati con i dati contenuti in Formdata.xml:</span><span class="sxs-lookup"><span data-stu-id="cd97e-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="cd97e-113">L'immagine del modulo specificata in Formdata.xml viene caricata come sfondo del controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="cd97e-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="cd97e-114">La raccolta di input penna viene quindi abilitata per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="cd97e-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="cd97e-115">Gestori eventi di menu</span><span class="sxs-lookup"><span data-stu-id="cd97e-115">Menu Event Handlers</span></span>

<span data-ttu-id="cd97e-116">L'applicazione include i gestori eventi Click per tutti i menu visualizzati nella parte superiore del form.</span><span class="sxs-lookup"><span data-stu-id="cd97e-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="cd97e-117">Voce di menu riconosci</span><span class="sxs-lookup"><span data-stu-id="cd97e-117">Recognize Menu Item</span></span>

<span data-ttu-id="cd97e-118">Il gestore dell'evento click del menu Recognize Disabilita la raccolta di input penna per il controllo e verifica la presenza di un riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="cd97e-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="cd97e-119">Se non è installato alcun riconoscimento, viene visualizzata una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="cd97e-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="cd97e-120">Un utente deve quindi fare clic sull'opzione di menu input penna o penna per riabilitare il controllo per input penna.</span><span class="sxs-lookup"><span data-stu-id="cd97e-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="cd97e-121">Se è installato un riconoscimento, la `Recognize` funzione recupera i dati XML che specificano le coordinate dei pixel per ogni campo del modulo.</span><span class="sxs-lookup"><span data-stu-id="cd97e-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="cd97e-122">Le coordinate vengono convertite in coordinate dello spazio di input penna e viene definito un rettangolo per ogni campo del modulo.</span><span class="sxs-lookup"><span data-stu-id="cd97e-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="cd97e-123">Dopo aver definito i rettangoli, la funzione trova i tratti che si intersecano e si trovano all'interno di ogni rettangolo.</span><span class="sxs-lookup"><span data-stu-id="cd97e-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="cd97e-124">Infine, esegue il riconoscimento sull'input penna e Visualizza i risultati in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="cd97e-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="cd97e-125">Voce di menu input penna</span><span class="sxs-lookup"><span data-stu-id="cd97e-125">Ink Menu Item</span></span>

<span data-ttu-id="cd97e-126">Il gestore dell'evento clic del menu input penna Abilita il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="cd97e-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="cd97e-127">Voce di menu penna</span><span class="sxs-lookup"><span data-stu-id="cd97e-127">Pen Menu Item</span></span>

<span data-ttu-id="cd97e-128">Il gestore eventi click del menu penna esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd97e-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="cd97e-129">Disabilita la raccolta di input penna per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) (necessario prima di modificare la proprietà [EditingMode](/previous-versions/ms582189(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="cd97e-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="cd97e-130">Imposta la proprietà [EditingMode](/previous-versions/ms582189(v=vs.100)) per la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="cd97e-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="cd97e-131">Riabilita la raccolta di input penna per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) e attiva o disattiva i menu penna, seleziona e Cancella per indicare la modalità attiva.</span><span class="sxs-lookup"><span data-stu-id="cd97e-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="cd97e-132">Modifica voce di menu</span><span class="sxs-lookup"><span data-stu-id="cd97e-132">Edit Menu Item</span></span>

<span data-ttu-id="cd97e-133">Il gestore eventi click del menu modifica è simile al gestore dell'evento del menu Pen.</span><span class="sxs-lookup"><span data-stu-id="cd97e-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="cd97e-134">Esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd97e-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="cd97e-135">Disabilita la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="cd97e-135">Disables ink collection.</span></span>
-   <span data-ttu-id="cd97e-136">Imposta la proprietà [EditingMode](/previous-versions/ms582189(v=vs.100)) su **SELECT**, che consente all'utente di eseguire la selezione dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="cd97e-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="cd97e-137">Abilita nuovamente la raccolta di input penna e attiva o disattiva i menu di penna, modifica e gomma per indicare la modalità attiva.</span><span class="sxs-lookup"><span data-stu-id="cd97e-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="cd97e-138">Voce di menu gomma</span><span class="sxs-lookup"><span data-stu-id="cd97e-138">Eraser Menu Item</span></span>

<span data-ttu-id="cd97e-139">Il gestore eventi click del menu gomma imposta il [](/previous-versions/aa514604(v=msdn.10)) controllo InkPicture [EditingMode](/previous-versions/ms582189(v=vs.100)) su **Delete**, che consente a un utente di cancellare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="cd97e-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="cd97e-140">Consente inoltre di impostare le voci di menu penna, modifica e gomma.</span><span class="sxs-lookup"><span data-stu-id="cd97e-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="cd97e-141">Cancella voce di menu</span><span class="sxs-lookup"><span data-stu-id="cd97e-141">Clear Menu Item</span></span>

<span data-ttu-id="cd97e-142">Il gestore dell'evento click menu Clear elimina la raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) corrente per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) , cancellando così tutto l'input penna nel form.</span><span class="sxs-lookup"><span data-stu-id="cd97e-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="cd97e-143">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="cd97e-143">Closing the Form</span></span>

<span data-ttu-id="cd97e-144">Nel codice generato da Progettazione Windows Form, il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) viene aggiunto all'elenco dei componenti del form quando il modulo viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cd97e-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="cd97e-145">Quando il form viene chiuso, il controllo InkPicture viene eliminato, così come gli altri componenti del form, dal metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo.</span><span class="sxs-lookup"><span data-stu-id="cd97e-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd97e-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd97e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd97e-147">Controllo InkEdit</span><span class="sxs-lookup"><span data-stu-id="cd97e-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="cd97e-148">Controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="cd97e-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
