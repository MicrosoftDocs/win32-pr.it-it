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
# <a name="ink-collection-sample"></a><span data-ttu-id="51131-103">Esempio di raccolta Ink</span><span class="sxs-lookup"><span data-stu-id="51131-103">Ink Collection Sample</span></span>

<span data-ttu-id="51131-104">Questa applicazione è basata sull'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) e Mostra la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="51131-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="51131-105">L'applicazione crea una finestra, vi associa un oggetto InkCollector e fornisce all'utente le opzioni di menu che è possibile usare per modificare il colore dell'input penna, la larghezza dell'input penna e abilitare e disabilitare la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="51131-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="51131-106">La versione illustrata in questa sezione è Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="51131-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="51131-107">I concetti sono gli stessi tra le versioni di altre lingue nella libreria degli esempi.</span><span class="sxs-lookup"><span data-stu-id="51131-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="51131-108">Dichiarazione dell'oggetto InkCollector</span><span class="sxs-lookup"><span data-stu-id="51131-108">Declaring the InkCollector</span></span>

<span data-ttu-id="51131-109">L'applicazione importa prima di tutto lo spazio dei nomi [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="51131-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="51131-110">Quindi, l'applicazione dichiara `myInkCollector` , che include l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) per il form.</span><span class="sxs-lookup"><span data-stu-id="51131-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="51131-111">Impostazione di elementi</span><span class="sxs-lookup"><span data-stu-id="51131-111">Setting Things Up</span></span>

<span data-ttu-id="51131-112">Il metodo del modulo `InkCollection_Load` gestisce l'evento di [caricamento](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del modulo.</span><span class="sxs-lookup"><span data-stu-id="51131-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="51131-113">Viene creato un oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) assegnato al form che modifica la proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto InkCollector e Abilita l'oggetto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="51131-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


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



<span data-ttu-id="51131-114">L'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) viene assegnato alla finestra del form assegnando l'handle della finestra del form alla proprietà [handle](/previous-versions/ms836504(v=msdn.10)) dell'oggetto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="51131-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="51131-115">La raccolta di input penna è attivata impostando la proprietà [Enabled](/previous-versions/ms836503(v=msdn.10)) dell'oggetto InkCollector su **true**.</span><span class="sxs-lookup"><span data-stu-id="51131-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="51131-116">La proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) imposta gli attributi predefiniti assegnati a un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="51131-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="51131-117">Per impostare attributi diversi in un nuovo cursore, utilizzare la proprietà [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) dell'oggetto [cursore](/previous-versions/ms839521(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="51131-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="51131-118">Per modificare gli attributi di disegno di un tratto singolo, utilizzare la proprietà [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) dell'oggetto [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="51131-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="51131-119">Modifica delle proprietà</span><span class="sxs-lookup"><span data-stu-id="51131-119">Changing the Properties</span></span>

<span data-ttu-id="51131-120">Il resto di questa semplice applicazione è costituito da gestori per le varie selezioni di menu che l'utente può eseguire.</span><span class="sxs-lookup"><span data-stu-id="51131-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="51131-121">Ad esempio, quando l'utente sceglie di modificare il colore dell'input penna in rosso selezionando rosso dal menu input penna, il colore viene modificato usando la proprietà [color](/previous-versions/ms837933(v=msdn.10)) della proprietà [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) dell'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) nel gestore eventi per il menu.</span><span class="sxs-lookup"><span data-stu-id="51131-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="51131-122">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="51131-122">Closing the Form</span></span>

<span data-ttu-id="51131-123">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="51131-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
