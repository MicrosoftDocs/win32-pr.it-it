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
# <a name="auto-claims-form-sample"></a>Esempio di modulo Claims automatico

L'esempio auto Claims risolve uno scenario ipotetico per un valutatore di assicurazioni. Il lavoro del valutatore richiede che l'it visiti i client presso la propria abitazione o l'azienda e per immettere le informazioni di attestazione in un modulo. Per aumentare la produttività del valutatore, il reparto IT sviluppa un'applicazione tablet che consente di immettere in modo rapido e preciso le informazioni sulle attestazioni tramite due controlli input penna, ovvero i controlli [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) .

In questo esempio viene usato un controllo [InkEdit](/previous-versions/ms835842(v=msdn.10)) per ogni campo di input di testo. Un utente immette le informazioni rilevanti su un criterio e un veicolo assicurativo in questi campi con una penna. Il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) viene usato per aggiungere input penna su un'immagine dell'automobile per evidenziare le aree danneggiate dell'automobile. L'esempio auto Claims è disponibile per C \# e Microsoft Visual Basic .NET. In questo argomento viene descritto il Visual Basic .NET.

La classe autoclaims viene definita come una sottoclasse di [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e viene definita una classe annidata per la creazione e la gestione di livelli di input penna per diversi tipi di danno. Per eseguire le attività seguenti sono definiti quattro gestori eventi:

-   Inizializzazione del form e dei livelli di input penna.
-   Ridisegno del controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) .
-   Selezione di un livello input penna nella casella di riepilogo.
-   Modifica della visibilità di un livello di input penna.

> [!Note]  
> Le versioni di questo esempio sono disponibili in C \# e Visual Basic .NET. La versione illustrata in questa sezione è Visual Basic .NET. I concetti sono gli stessi tra le versioni.

 

## <a name="defining-the-form-and-ink-layers"></a>Definizione del modulo e dei livelli di input penna

È necessario importare lo spazio dei nomi [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Quindi, nella classe autoclaims viene definita una classe annidata `InkLayer` e `InkLayer` viene dichiarata una matrice di quattro oggetti. (InkLayer contiene un oggetto [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) per archiviare i valori di input penna e [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) e **Boolean** per archiviare il colore e lo stato nascosto del livello). Un quinto oggetto Ink viene dichiarato per gestire l'input penna per il [InkPicture](/previous-versions/ms583740(v=vs.100)) quando tutti i livelli di input penna sono nascosti.


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



Ogni livello dispone di un proprio oggetto [Ink](/previous-versions/ms583670(v=vs.100)) . Nel modulo di attestazione sono presenti quattro aree discrete, ovvero Body, Windows, Tires e fari, quindi vengono usati quattro oggetti InkLayer. Un utente può visualizzare qualsiasi combinazione di livelli in una sola volta.

## <a name="initializing-the-form-and-ink-layers"></a>Inizializzazione del form e dei livelli di input penna

Il `Load` gestore dell'evento Inizializza l'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) e i quattro `InkLayer` oggetti.


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



Selezionare quindi la prima voce (Body) nella casella di riepilogo.


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



Infine, impostare il colore dell'input penna per il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) sulla voce della casella di riepilogo attualmente selezionata.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Ridisegno del controllo InkPicture

Nel gestore dell'evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) ereditato del controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) , i livelli di input penna vengono controllati per determinare quali sono nascosti. Se un livello non è nascosto, viene visualizzato dalla routine evento utilizzando il metodo di [richiamo](/previous-versions/ms828488(v=msdn.10)) della proprietà [renderer](/previous-versions/ms582196(v=vs.100)) . Se si osserva la Visualizzatore oggetti, si noterà che la proprietà Microsoft. Ink. InkPicture. Renderer è definita come oggetto [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Selezione di un livello input penna nella casella di riepilogo

Quando l'utente seleziona un elemento nella casella di riepilogo, il gestore eventi [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) verifica innanzitutto che la selezione sia stata modificata e che il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) non stia attualmente raccogliendo input penna. Imposta quindi il colore dell'input penna del controllo InkPicture sul colore appropriato per il livello di input penna selezionato. Aggiorna inoltre la casella di controllo Nascondi livello in modo da riflettere lo stato nascosto del livello di input penna selezionato. Infine, il metodo di [aggiornamento](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) ereditato del controllo InkPicture viene utilizzato per visualizzare solo i livelli desiderati all'interno del controllo.


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>Modifica della visibilità di un livello di input penna

Il `CheckedChanged` gestore eventi verifica innanzitutto che la selezione sia stata modificata e che il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) non stia attualmente raccogliendo input penna. Aggiorna quindi lo stato nascosto del livello di input penna selezionato, imposta il InkEnabled del controllo InkPicture su **false**,.

Quindi, la proprietà InkEnabled del controllo InkPicture è impostata su **false** prima di aggiornare la relativa proprietà Ink.

Infine, il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) viene abilitato o disabilitato per la parte specifica del veicolo a seconda che sia selezionata la casella di controllo Nascondi livello e che il metodo di [aggiornamento](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del controllo InkPicture venga utilizzato per visualizzare solo i livelli desiderati all'interno del controllo.


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



## <a name="closing-the-form"></a>Chiusura del modulo

Nel codice generato da Progettazione Windows Form, i controlli [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) vengono aggiunti all'elenco dei componenti del form quando il modulo viene inizializzato. Quando il form viene chiuso, i controlli InkEdit e InkPicture vengono eliminati, così come gli altri componenti del form, dal metodo [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) del modulo. Il metodo Dispose del modulo Elimina inoltre gli oggetti [Ink](/previous-versions/ms583670(v=vs.100)) creati per il form.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[Controllo InkPicture](inkpicture-control.md)
</dt> <dt>

[Controllo InkEdit](inkedit-control.md)
</dt> </dl>

 

 
