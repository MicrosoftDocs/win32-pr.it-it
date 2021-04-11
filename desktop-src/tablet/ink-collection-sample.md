---
description: Questa applicazione è basata sull'oggetto InkCollector e Mostra la raccolta di input penna.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Esempio di raccolta Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128995"
---
# <a name="ink-collection-sample"></a>Esempio di raccolta Ink

Questa applicazione è basata sull'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) e Mostra la raccolta di input penna. L'applicazione crea una finestra, vi associa un oggetto InkCollector e fornisce all'utente le opzioni di menu che è possibile usare per modificare il colore dell'input penna, la larghezza dell'input penna e abilitare e disabilitare la raccolta di input penna.

> [!Note]  
> La versione illustrata in questa sezione è Visual Basic .NET. I concetti sono gli stessi tra le versioni di altre lingue nella libreria degli esempi.

 

## <a name="declaring-the-inkcollector"></a>Dichiarazione dell'oggetto InkCollector

L'applicazione importa prima di tutto lo spazio dei nomi [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) . Quindi, l'applicazione dichiara `myInkCollector` , che include l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) per il form.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Impostazione di elementi

Il metodo del modulo `InkCollection_Load` gestisce l'evento di [caricamento](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del modulo. Viene creato un oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) assegnato al form che modifica la proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto InkCollector e Abilita l'oggetto InkCollector.


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



L'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) viene assegnato alla finestra del form assegnando l'handle della finestra del form alla proprietà [handle](/previous-versions/ms836504(v=msdn.10)) dell'oggetto InkCollector. La raccolta di input penna è attivata impostando la proprietà [Enabled](/previous-versions/ms836503(v=msdn.10)) dell'oggetto InkCollector su **true**.

La proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) imposta gli attributi predefiniti assegnati a un nuovo cursore. Per impostare attributi diversi in un nuovo cursore, utilizzare la proprietà [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) dell'oggetto [cursore](/previous-versions/ms839521(v=msdn.10)) . Per modificare gli attributi di disegno di un tratto singolo, utilizzare la proprietà [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) .

## <a name="changing-the-properties"></a>Modifica delle proprietà

Il resto di questa semplice applicazione è costituito da gestori per le varie selezioni di menu che l'utente può eseguire. Ad esempio, quando l'utente sceglie di modificare il colore dell'input penna in rosso selezionando rosso dal menu input penna, il colore viene modificato usando la proprietà [color](/previous-versions/ms837933(v=msdn.10)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) nel gestore eventi per il menu.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
