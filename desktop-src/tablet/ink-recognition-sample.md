---
description: Questa applicazione illustra come creare un'applicazione di riconoscimento della grafia. L Windows Vista SDK fornisce anche le versioni di questo esempio in C \# e Visual Basic .NET.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Esempio di riconoscimento input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151c92c9f407461c34ecffb015af179e57b5c9ed4735b36f70c9a4d26c78088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935121"
---
# <a name="ink-recognition-sample"></a>Esempio di riconoscimento input penna

Questa applicazione illustra come creare un'applicazione di riconoscimento della grafia. L Windows Vista SDK fornisce anche le versioni di questo esempio in C \# e Visual Basic .NET. In questo argomento si fa riferimento Visual Basic'esempio .NET, ma i concetti sono gli stessi tra le versioni.

## <a name="access-the-tablet-pc-interfaces"></a>Accedere alle interfacce tablet PC

Per prima cosa, fare riferimento all'API Tablet PC, che viene installata con l'SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Inizializzare InkCollector

L'esempio aggiunge codice al gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form che consente di [associare InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, alla finestra della casella di gruppo e abilitare InkCollector.


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

Il [gestore](/dotnet/api/system.windows.forms.button?view=netcore-3.1) dell'evento Click dell'oggetto [Button](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) verifica che l'utente abbia installato almeno un sistema di riconoscimento esaminando la [proprietà Count](/previous-versions/ms828521(v=msdn.10)) della raccolta [Recognizers.](/previous-versions/ms828520(v=msdn.10))

La [proprietà SelectedText](/previous-versions/windows/) della casella di testo viene impostata sulla corrispondenza migliore per i tratti usando il [metodo ToString](/previous-versions/ms827836(v=msdn.10)) nella [raccolta Strokes.](/previous-versions/ms552701(v=vs.100)) Dopo che i tratti sono stati riconosciuti, vengono eliminati. Infine, il codice forza il ridisegno dell'area di disegno, cancellando l'area per un ulteriore uso dell'input penna.


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

Il metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form elimina l'oggetto [InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
