---
description: Questa applicazione illustra come è possibile compilare un'applicazione di riconoscimento della grafia. Windows Vista SDK fornisce anche le versioni di questo esempio in C \# e Visual Basic .NET.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Esempio di riconoscimento dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226050"
---
# <a name="ink-recognition-sample"></a>Esempio di riconoscimento dell'input penna

Questa applicazione illustra come è possibile compilare un'applicazione di riconoscimento della grafia. Windows Vista SDK fornisce anche le versioni di questo esempio in C \# e Visual Basic .NET. Questo argomento si riferisce all'esempio Visual Basic .NET, ma i concetti sono gli stessi tra le versioni.

## <a name="access-the-tablet-pc-interfaces"></a>Accedere alle interfacce di Tablet PC

Per prima cosa, fare riferimento all'API Tablet PC, che viene installata con l'SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Inizializzare l'oggetto InkCollector

Nell'esempio viene aggiunto il codice al gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form che consente di associare l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)), InkCollector, alla finestra di gruppo e di abilitare l'oggetto InkCollector.


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a>Riconoscere i tratti

Il gestore dell'evento [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) dell'oggetto [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) verifica che l'utente disponga di almeno un riconoscimento installato esaminando la proprietà [count](/previous-versions/ms828521(v=msdn.10)) della raccolta [Recognizers](/previous-versions/ms828520(v=msdn.10)) .

La proprietà [SelectedText](/previous-versions/windows/) della casella di testo è impostata sulla corrispondenza migliore per i tratti usando il metodo [ToString](/previous-versions/ms827836(v=msdn.10)) nella raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) . Dopo essere stati riconosciuti, i tratti vengono eliminati. Infine, il codice forza il ridisegno dell'area di disegno, deselezionando il codice per un ulteriore utilizzo di input penna.


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
