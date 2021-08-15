---
description: Questa applicazione è basata sull'oggetto InkCollector e illustra la raccolta di input penna.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Esempio di raccolta ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5f568abf38abfa31d9374a7a1874f9f73481a799a740c402f3e8f168963c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718260"
---
# <a name="ink-collection-sample"></a>Esempio di raccolta ink

Questa applicazione è basata [sull'oggetto InkCollector](/previous-versions/ms836493(v=msdn.10)) e illustra la raccolta di input penna. L'applicazione crea una finestra, allega un oggetto InkCollector e fornisce all'utente opzioni di menu che possono essere usate per modificare il colore dell'input penna, la larghezza dell'input penna e abilitare e disabilitare la raccolta di input penna.

> [!Note]  
> La versione descritta in questa sezione è Visual Basic .NET. I concetti sono gli stessi tra le altre versioni del linguaggio nella libreria di esempi.

 

## <a name="declaring-the-inkcollector"></a>Dichiarazione di InkCollector

L'applicazione importa prima di tutto lo [spazio dei nomi Microsoft.Ink.](/previous-versions/ms826516(v=msdn.10)) L'applicazione dichiara quindi `myInkCollector` , che contiene [l'oggetto InkCollector](/previous-versions/ms836493(v=msdn.10)) per il form.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Configurazione di elementi

Il metodo del `InkCollection_Load` form gestisce l'evento [Load del](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) form. Crea un [oggetto InkCollector](/previous-versions/ms836493(v=msdn.10)) assegnato al form modifica la proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto InkCollector e abilita l'oggetto InkCollector.


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



[InkCollector](/previous-versions/ms836493(v=msdn.10)) viene assegnato alla finestra del form assegnando l'handle della finestra del form alla proprietà [Handle](/previous-versions/ms836504(v=msdn.10)) dell'oggetto InkCollector. La raccolta input penna viene attivata impostando la proprietà [Enabled](/previous-versions/ms836503(v=msdn.10)) dell'oggetto InkCollector su **TRUE.**

La proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) imposta gli attributi predefiniti assegnati a un nuovo cursore. Per impostare attributi diversi in un nuovo cursore, usare la [proprietà DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) dell'oggetto [Cursor.](/previous-versions/ms839521(v=msdn.10)) Per modificare gli attributi di disegno di un singolo tratto, usa la [proprietà DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) dell'oggetto [Stroke.](/previous-versions/ms827842(v=msdn.10))

## <a name="changing-the-properties"></a>Modifica delle proprietà

Il resto di questa semplice applicazione è costituito da gestori per le varie selezioni di menu che l'utente può effettuare. Ad esempio, quando l'utente sceglie di modificare il colore dell'input penna in rosso scegliendo Rosso dal menu Input penna, il colore viene modificato usando la proprietà [Color](/previous-versions/ms837933(v=msdn.10)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) nel gestore eventi per il menu.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Chiusura del modulo

Il metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form elimina l'oggetto [InkCollector,](/previous-versions/ms836493(v=msdn.10)) `myInkCollector` .

 

 
