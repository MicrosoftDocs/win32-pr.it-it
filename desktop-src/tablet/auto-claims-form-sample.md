---
description: L'esempio auto Claims risolve uno scenario ipotetico per un valutatore di assicurazioni.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Esempio di modulo Claims automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346891"
---
# <a name="auto-claims-form-sample"></a><span data-ttu-id="0329a-103">Esempio di modulo Claims automatico</span><span class="sxs-lookup"><span data-stu-id="0329a-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="0329a-104">L'esempio auto Claims risolve uno scenario ipotetico per un valutatore di assicurazioni.</span><span class="sxs-lookup"><span data-stu-id="0329a-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="0329a-105">Il lavoro del valutatore richiede che l'it visiti i client presso la propria abitazione o l'azienda e per immettere le informazioni di attestazione in un modulo.</span><span class="sxs-lookup"><span data-stu-id="0329a-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="0329a-106">Per aumentare la produttività del valutatore, il reparto IT sviluppa un'applicazione tablet che consente di immettere in modo rapido e preciso le informazioni sulle attestazioni tramite due controlli input penna, ovvero i controlli [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="0329a-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="0329a-107">In questo esempio viene usato un controllo [InkEdit](/previous-versions/ms835842(v=msdn.10)) per ogni campo di input di testo.</span><span class="sxs-lookup"><span data-stu-id="0329a-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="0329a-108">Un utente immette le informazioni rilevanti su un criterio e un veicolo assicurativo in questi campi con una penna.</span><span class="sxs-lookup"><span data-stu-id="0329a-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="0329a-109">Il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) viene usato per aggiungere input penna su un'immagine dell'automobile per evidenziare le aree danneggiate dell'automobile.</span><span class="sxs-lookup"><span data-stu-id="0329a-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="0329a-110">L'esempio auto Claims è disponibile per C \# e Microsoft Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="0329a-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="0329a-111">In questo argomento viene descritto il Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="0329a-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="0329a-112">La classe autoclaims viene definita come una sottoclasse di [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e viene definita una classe annidata per la creazione e la gestione di livelli di input penna per diversi tipi di danno.</span><span class="sxs-lookup"><span data-stu-id="0329a-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="0329a-113">Per eseguire le attività seguenti sono definiti quattro gestori eventi:</span><span class="sxs-lookup"><span data-stu-id="0329a-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="0329a-114">Inizializzazione del form e dei livelli di input penna.</span><span class="sxs-lookup"><span data-stu-id="0329a-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="0329a-115">Ridisegno del controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="0329a-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="0329a-116">Selezione di un livello input penna nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="0329a-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="0329a-117">Modifica della visibilità di un livello di input penna.</span><span class="sxs-lookup"><span data-stu-id="0329a-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="0329a-118">Le versioni di questo esempio sono disponibili in C \# e Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="0329a-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="0329a-119">La versione illustrata in questa sezione è Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="0329a-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="0329a-120">I concetti sono gli stessi tra le versioni.</span><span class="sxs-lookup"><span data-stu-id="0329a-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="0329a-121">Definizione del modulo e dei livelli di input penna</span><span class="sxs-lookup"><span data-stu-id="0329a-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="0329a-122">È necessario importare lo spazio dei nomi [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="0329a-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="0329a-123">Quindi, nella classe autoclaims viene definita una classe annidata `InkLayer` e `InkLayer` viene dichiarata una matrice di quattro oggetti.</span><span class="sxs-lookup"><span data-stu-id="0329a-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="0329a-124">(InkLayer contiene un oggetto [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) per archiviare i valori di input penna e [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) e **Boolean** per archiviare il colore e lo stato nascosto del livello). Un quinto oggetto Ink viene dichiarato per gestire l'input penna per il [InkPicture](/previous-versions/ms583740(v=vs.100)) quando tutti i livelli di input penna sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="0329a-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



<span data-ttu-id="0329a-125">Ogni livello dispone di un proprio oggetto [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="0329a-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="0329a-126">Nel modulo di attestazione sono presenti quattro aree discrete, ovvero Body, Windows, Tires e fari, quindi vengono usati quattro oggetti InkLayer.</span><span class="sxs-lookup"><span data-stu-id="0329a-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="0329a-127">Un utente può visualizzare qualsiasi combinazione di livelli in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="0329a-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="0329a-128">Inizializzazione del form e dei livelli di input penna</span><span class="sxs-lookup"><span data-stu-id="0329a-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="0329a-129">Il `Load` gestore dell'evento Inizializza l'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) e i quattro `InkLayer` oggetti.</span><span class="sxs-lookup"><span data-stu-id="0329a-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



<span data-ttu-id="0329a-130">Selezionare quindi la prima voce (Body) nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="0329a-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="0329a-131">Infine, impostare il colore dell'input penna per il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) sulla voce della casella di riepilogo attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="0329a-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="0329a-132">Ridisegno del controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="0329a-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="0329a-133">Nel gestore dell'evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) ereditato del controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) , i livelli di input penna vengono controllati per determinare quali sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="0329a-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="0329a-134">Se un livello non è nascosto, viene visualizzato dalla routine evento utilizzando il metodo di [richiamo](/previous-versions/ms828488(v=msdn.10)) della proprietà [renderer](/previous-versions/ms582196(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="0329a-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="0329a-135">Se si osserva la Visualizzatore oggetti, si noterà che la proprietà Microsoft. Ink. InkPicture. Renderer è definita come oggetto [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="0329a-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="0329a-136">Selezione di un livello input penna nella casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="0329a-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="0329a-137">Quando l'utente seleziona un elemento nella casella di riepilogo, il gestore eventi [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) verifica innanzitutto che la selezione sia stata modificata e che il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) non stia attualmente raccogliendo input penna.</span><span class="sxs-lookup"><span data-stu-id="0329a-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="0329a-138">Imposta quindi il colore dell'input penna del controllo InkPicture sul colore appropriato per il livello di input penna selezionato.</span><span class="sxs-lookup"><span data-stu-id="0329a-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="0329a-139">Aggiorna inoltre la casella di controllo Nascondi livello in modo da riflettere lo stato nascosto del livello di input penna selezionato.</span><span class="sxs-lookup"><span data-stu-id="0329a-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="0329a-140">Infine, il metodo di [aggiornamento](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) ereditato del controllo InkPicture viene utilizzato per visualizzare solo i livelli desiderati all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="0329a-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="0329a-141">Modifica della visibilità di un livello di input penna</span><span class="sxs-lookup"><span data-stu-id="0329a-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="0329a-142">Il `CheckedChanged` gestore eventi verifica innanzitutto che la selezione sia stata modificata e che il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) non stia attualmente raccogliendo input penna.</span><span class="sxs-lookup"><span data-stu-id="0329a-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="0329a-143">Aggiorna quindi lo stato nascosto del livello di input penna selezionato, imposta il InkEnabled del controllo InkPicture su **false**,.</span><span class="sxs-lookup"><span data-stu-id="0329a-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="0329a-144">Quindi, la proprietà InkEnabled del controllo InkPicture è impostata su **false** prima di aggiornare la relativa proprietà Ink.</span><span class="sxs-lookup"><span data-stu-id="0329a-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="0329a-145">Infine, il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) viene abilitato o disabilitato per la parte specifica del veicolo a seconda che sia selezionata la casella di controllo Nascondi livello e che il metodo di [aggiornamento](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del controllo InkPicture venga utilizzato per visualizzare solo i livelli desiderati all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="0329a-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a><span data-ttu-id="0329a-146">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="0329a-146">Closing the Form</span></span>

<span data-ttu-id="0329a-147">Nel codice generato da Progettazione Windows Form, i controlli [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) vengono aggiunti all'elenco dei componenti del form quando il modulo viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="0329a-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="0329a-148">Quando il form viene chiuso, i controlli InkEdit e InkPicture vengono eliminati, così come gli altri componenti del form, dal metodo [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) del modulo.</span><span class="sxs-lookup"><span data-stu-id="0329a-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="0329a-149">Il metodo Dispose del modulo Elimina inoltre gli oggetti [Ink](/previous-versions/ms583670(v=vs.100)) creati per il form.</span><span class="sxs-lookup"><span data-stu-id="0329a-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0329a-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0329a-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0329a-151">[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="0329a-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="0329a-152">Controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="0329a-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="0329a-153">Controllo InkEdit</span><span class="sxs-lookup"><span data-stu-id="0329a-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 
