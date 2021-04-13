---
description: Questo programma illustra come copiare e incollare input penna in un'altra applicazione. Consente inoltre all'utente di copiare una selezione di tratti e incollare il risultato nell'oggetto Ink esistente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Esempio di appunti Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525969"
---
# <a name="ink-clipboard-sample"></a><span data-ttu-id="f8549-104">Esempio di appunti Ink</span><span class="sxs-lookup"><span data-stu-id="f8549-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="f8549-105">Questo programma illustra come copiare e incollare input penna in un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8549-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="f8549-106">Consente inoltre all'utente di copiare una selezione di tratti e incollare il risultato nell'oggetto Ink esistente.</span><span class="sxs-lookup"><span data-stu-id="f8549-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="f8549-107">Sono disponibili le modalità degli Appunti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8549-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="f8549-108">Formato ISF (Ink Serialized Format)</span><span class="sxs-lookup"><span data-stu-id="f8549-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="f8549-109">Metafile</span><span class="sxs-lookup"><span data-stu-id="f8549-109">Metafile</span></span>
-   <span data-ttu-id="f8549-110">Enhanced Metafile (EMF)</span><span class="sxs-lookup"><span data-stu-id="f8549-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="f8549-111">Bitmap</span><span class="sxs-lookup"><span data-stu-id="f8549-111">Bitmap</span></span>
-   <span data-ttu-id="f8549-112">Input penna</span><span class="sxs-lookup"><span data-stu-id="f8549-112">Text Ink</span></span>
-   <span data-ttu-id="f8549-113">Disegna input penna</span><span class="sxs-lookup"><span data-stu-id="f8549-113">Sketch Ink</span></span>

<span data-ttu-id="f8549-114">Input penna e sketch input penna sono due tipi di controlli input penna utilizzati rispettivamente come testo o come disegno.</span><span class="sxs-lookup"><span data-stu-id="f8549-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="f8549-115">È possibile incollare ISF, input penna e sketch Ink nell'input penna esistente.</span><span class="sxs-lookup"><span data-stu-id="f8549-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="f8549-116">Oltre agli Appunti, questo esempio illustra anche come selezionare i tratti con lo strumento lazo.</span><span class="sxs-lookup"><span data-stu-id="f8549-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="f8549-117">L'utente può spostare i tratti selezionati e modificarne gli attributi di disegno.</span><span class="sxs-lookup"><span data-stu-id="f8549-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="f8549-118">Questa funzionalità è un subset della funzionalità di selezione già fornita dal controllo overlay dell'input penna. viene implementato qui a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="f8549-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="f8549-119">In questo esempio vengono usate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8549-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="f8549-120">Oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="f8549-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="f8549-121">Supporto degli Appunti di input penna.</span><span class="sxs-lookup"><span data-stu-id="f8549-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="f8549-122">Uso del lazo con il metodo [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .</span><span class="sxs-lookup"><span data-stu-id="f8549-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="f8549-123">In questo esempio viene illustrato come eseguire il rendering dell'input penna, copiare l'input penna e quindi incollare l'input penna in un'altra applicazione, ad esempio Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="f8549-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="f8549-124">Raccolta di input penna e configurazione del modulo</span><span class="sxs-lookup"><span data-stu-id="f8549-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="f8549-125">Per prima cosa, fare riferimento alle interfacce di automazione di Tablet PC, installate con Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f8549-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="f8549-126">Successivamente, il form dichiara alcune costanti e i campi che sono indicati più avanti in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="f8549-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



<span data-ttu-id="f8549-127">Infine, nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form, il form viene inizializzato, viene creato un oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per il form e l'agente di raccolta input penna è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f8549-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="f8549-128">Gestione degli eventi di menu</span><span class="sxs-lookup"><span data-stu-id="f8549-128">Handling Menu Events</span></span>

<span data-ttu-id="f8549-129">I gestori eventi delle voci di menu aggiornano principalmente lo stato del modulo.</span><span class="sxs-lookup"><span data-stu-id="f8549-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="f8549-130">Il comando Clear rimuove il rettangolo di selezione ed Elimina i tratti dall'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) dell'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="f8549-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="f8549-131">Il comando Exit Disabilita l'agente di raccolta input penna prima di uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8549-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="f8549-132">Il menu modifica Abilita i comandi taglia e copia in base allo stato di selezione del form e Abilita il comando Incolla in base al contenuto degli Appunti, determinato tramite il metodo [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="f8549-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="f8549-133">I comandi taglia e copia usano entrambi un metodo helper per copiare l'input penna negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f8549-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="f8549-134">Il comando Taglia USA un metodo helper per eliminare i tratti selezionati.</span><span class="sxs-lookup"><span data-stu-id="f8549-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="f8549-135">Il comando Incolla controlla prima di tutto il metodo [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per verificare se l'oggetto negli Appunti può essere incollato.</span><span class="sxs-lookup"><span data-stu-id="f8549-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="f8549-136">Il comando Incolla quindi calcola l'angolo superiore sinistro per l'area di Incolla, converte le coordinate da pixel a spazio di input penna e incolla i tratti dagli Appunti nell'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="f8549-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="f8549-137">Infine, viene aggiornata la casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="f8549-137">Finally, the selection box is updated.</span></span>


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



<span data-ttu-id="f8549-138">I comandi SELECT e Ink aggiornano la modalità dell'applicazione e gli attributi di disegno predefiniti, cancellano la selezione corrente, aggiornano lo stato del menu e aggiornano il modulo.</span><span class="sxs-lookup"><span data-stu-id="f8549-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="f8549-139">Gli altri gestori si basano sullo stato dell'applicazione per eseguire la funzione corretta, ovvero il lazo o la disinstallazione dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="f8549-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="f8549-140">Inoltre, il comando SELECT aggiunge i gestori eventi [NewPackets](/previous-versions/ms567621(v=vs.100)) e [Stroke](/previous-versions/ms567622(v=vs.100)) all'agente di raccolta input penna e il comando Ink rimuove i gestori eventi dall'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="f8549-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="f8549-141">I formati disponibili negli Appunti quando vengono copiati i tratti sono elencati nel menu formato e l'utente seleziona il formato per la copia dell'input penna da questo elenco.</span><span class="sxs-lookup"><span data-stu-id="f8549-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="f8549-142">I tipi di formati disponibili includono il formato ISF (Ink Serialized Format), metafile, Enhanced Metafile e bitmap.</span><span class="sxs-lookup"><span data-stu-id="f8549-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="f8549-143">I formati di sketch Ink e Text Ink si escludono a vicenda e si basano sull'input penna copiato negli Appunti come oggetto OLE.</span><span class="sxs-lookup"><span data-stu-id="f8549-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="f8549-144">Il menu stile consente all'utente di modificare le proprietà relative al colore e alla larghezza della penna e dei tratti selezionati.</span><span class="sxs-lookup"><span data-stu-id="f8549-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="f8549-145">Ad esempio, il comando rosso imposta la proprietà [color](/previous-versions/ms582103(v=vs.100)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) dell'agente di raccolta input penna sul colore rosso.</span><span class="sxs-lookup"><span data-stu-id="f8549-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="f8549-146">Poiché la proprietà [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) dell'oggetto [cursore](/previous-versions/ms552104(v=vs.100)) non è stata impostata, qualsiasi nuovo input penna creato nell'agente di raccolta input penna eredita il colore predefinito del disegno.</span><span class="sxs-lookup"><span data-stu-id="f8549-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="f8549-147">Inoltre, se sono attualmente selezionati tratti, viene aggiornata anche la proprietà Color degli attributi di disegno di ciascun tratto.</span><span class="sxs-lookup"><span data-stu-id="f8549-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a><span data-ttu-id="f8549-148">Gestione degli eventi del mouse</span><span class="sxs-lookup"><span data-stu-id="f8549-148">Handling Mouse Events</span></span>

<span data-ttu-id="f8549-149">Il gestore dell'evento [MouseMove](/previous-versions/ms567617(v=vs.100)) controlla la modalità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8549-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="f8549-150">Se la modalità è MoveInk e un pulsante del mouse è inattivo, il gestore sposta i tratti usando il metodo Move della raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) e aggiorna la casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="f8549-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="f8549-151">In caso contrario, il gestore verifica per determinare se il rettangolo di selezione contiene il cursore, Abilita la raccolta di input penna di conseguenza e imposta di conseguenza il cursore.</span><span class="sxs-lookup"><span data-stu-id="f8549-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="f8549-152">Il gestore eventi [MouseDown](/previous-versions/ms567616(v=vs.100)) controlla l'impostazione del cursore.</span><span class="sxs-lookup"><span data-stu-id="f8549-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="f8549-153">Se il cursore è impostato su [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), il gestore imposta la modalità dell'applicazione su MoveInk e registra la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="f8549-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="f8549-154">In caso contrario, se è presente una selezione corrente, deselezionarla.</span><span class="sxs-lookup"><span data-stu-id="f8549-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="f8549-155">Il gestore dell'evento [MouseUp](/previous-versions/ms567618(v=vs.100)) controlla la modalità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8549-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="f8549-156">Se la modalità è MoveInk, il gestore imposta la modalità dell'applicazione in base allo stato selezionato del comando SELECT.</span><span class="sxs-lookup"><span data-stu-id="f8549-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="f8549-157">L'evento [NewPackets](/previous-versions/ms567621(v=vs.100)) viene generato in modalità di selezione quando l'agente di raccolta input penna riceve nuovi dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f8549-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="f8549-158">Se l'applicazione è in modalità di selezione, è necessario intercettare i nuovi pacchetti e usarli per creare il lazo di selezione.</span><span class="sxs-lookup"><span data-stu-id="f8549-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="f8549-159">La coordinata di ogni pacchetto viene convertita in pixel, vincolata all'area di disegno e aggiunta alla raccolta di punti del lazo.</span><span class="sxs-lookup"><span data-stu-id="f8549-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="f8549-160">Viene quindi chiamato un metodo helper per creare il lazo sul form.</span><span class="sxs-lookup"><span data-stu-id="f8549-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="f8549-161">Gestione di un nuovo tratto</span><span class="sxs-lookup"><span data-stu-id="f8549-161">Handling a New Stroke</span></span>

<span data-ttu-id="f8549-162">Quando viene disegnato un nuovo tratto, l'evento [Stroke](/previous-versions/ms567622(v=vs.100)) viene generato in modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="f8549-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="f8549-163">Se l'applicazione è in modalità di selezione, questo tratto corrisponde al lazo ed è necessario aggiornare le informazioni sui tratti selezionati.</span><span class="sxs-lookup"><span data-stu-id="f8549-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="f8549-164">Il gestore Annulla l'evento [Stroke](/previous-versions/ms567622(v=vs.100)) , verifica la presenza di più di due punti lazo, copia la raccolta Points in una matrice di oggetti [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) e converte le coordinate dei punti della matrice da pixel a spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="f8549-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="f8549-165">Quindi, il gestore usa il metodo [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per ottenere i tratti selezionati dai punti di lazo e aggiorna lo stato di selezione del form.</span><span class="sxs-lookup"><span data-stu-id="f8549-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="f8549-166">Infine, il tratto che ha generato l'evento viene rimosso dalla raccolta dei tratti selezionati, la raccolta di punti lazo viene svuotata e un metodo helper disegna il rettangolo di selezione.</span><span class="sxs-lookup"><span data-stu-id="f8549-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="f8549-167">Copia dell'input penna negli Appunti</span><span class="sxs-lookup"><span data-stu-id="f8549-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="f8549-168">Il metodo helper CopyInkToClipboard crea un valore [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , controlla lo stato del menu formato per aggiornare i formati da inserire negli Appunti e usa il metodo [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) dell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) per copiare i tratti negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f8549-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a><span data-ttu-id="f8549-169">Aggiornamento di una selezione</span><span class="sxs-lookup"><span data-stu-id="f8549-169">Updating a Selection</span></span>

<span data-ttu-id="f8549-170">Il metodo helper seselectation aggiorna il selectedStrokes archiviato e, se la raccolta è **null** o **vuota**, il rettangolo di selezione viene impostato sul rettangolo vuoto.</span><span class="sxs-lookup"><span data-stu-id="f8549-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="f8549-171">Se la raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) selezionata non è vuota, il metodo di selezione esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8549-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="f8549-172">Determina il rettangolo di delimitazione usando il metodo [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) della raccolta Strokes</span><span class="sxs-lookup"><span data-stu-id="f8549-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="f8549-173">Converte le coordinate del rettangolo dallo spazio dell'input penna ai pixel</span><span class="sxs-lookup"><span data-stu-id="f8549-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="f8549-174">Ingrandisce il rettangolo per fornire uno spazio visivo tra l'oggetto e i tratti selezionati.</span><span class="sxs-lookup"><span data-stu-id="f8549-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="f8549-175">Crea gli handle di selezione per la casella di selezione corrente</span><span class="sxs-lookup"><span data-stu-id="f8549-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="f8549-176">Infine, il metodo seselectation imposta la visibilità degli handle di selezione e imposta la proprietà [AutoRedraw](/previous-versions/ms571706(v=vs.100)) dell'agente di raccolta input penna su **false**, se i tratti sono selezionati.</span><span class="sxs-lookup"><span data-stu-id="f8549-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a><span data-ttu-id="f8549-177">Disegno del lazo</span><span class="sxs-lookup"><span data-stu-id="f8549-177">Drawing the Lasso</span></span>

<span data-ttu-id="f8549-178">Il lazo viene disegnato come una serie di punti aperti che seguono il percorso del tratto del lazo e una linea del connettore tratteggiata tra le due estremità.</span><span class="sxs-lookup"><span data-stu-id="f8549-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="f8549-179">L'evento [NewPackets](/previous-versions/ms567621(v=vs.100)) viene generato durante il disegno del lazo e il gestore dell'evento passa le informazioni sul tratto al metodo DrawLasso.</span><span class="sxs-lookup"><span data-stu-id="f8549-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="f8549-180">Il metodo helper DrawLasso rimuove prima di tutto la vecchia riga del connettore e quindi scorre i punti del tratto.</span><span class="sxs-lookup"><span data-stu-id="f8549-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="f8549-181">Quindi, DrawLasso calcola dove posizionare i punti lungo il tratto e li disegna.</span><span class="sxs-lookup"><span data-stu-id="f8549-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="f8549-182">Infine, viene disegnata una nuova linea di connessione.</span><span class="sxs-lookup"><span data-stu-id="f8549-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="f8549-183">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="f8549-183">Closing the Form</span></span>

<span data-ttu-id="f8549-184">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) , ovvero InkCollector.</span><span class="sxs-lookup"><span data-stu-id="f8549-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 
