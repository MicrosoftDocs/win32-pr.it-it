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
# <a name="ink-recognition-sample"></a><span data-ttu-id="d2b5b-103">Esempio di riconoscimento dell'input penna</span><span class="sxs-lookup"><span data-stu-id="d2b5b-103">Ink Recognition Sample</span></span>

<span data-ttu-id="d2b5b-104">Questa applicazione illustra come è possibile compilare un'applicazione di riconoscimento della grafia. Windows Vista SDK fornisce anche le versioni di questo esempio in C \# e Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="d2b5b-104">This application demonstrates how you can build a handwriting recognition application.The Windows Vista SDK provides versions of this sample in C\# and Visual Basic .NET, as well.</span></span> <span data-ttu-id="d2b5b-105">Questo argomento si riferisce all'esempio Visual Basic .NET, ma i concetti sono gli stessi tra le versioni.</span><span class="sxs-lookup"><span data-stu-id="d2b5b-105">This topic refers to the Visual Basic .NET sample, but the concepts are the same between versions.</span></span>

## <a name="access-the-tablet-pc-interfaces"></a><span data-ttu-id="d2b5b-106">Accedere alle interfacce di Tablet PC</span><span class="sxs-lookup"><span data-stu-id="d2b5b-106">Access the Tablet PC Interfaces</span></span>

<span data-ttu-id="d2b5b-107">Per prima cosa, fare riferimento all'API Tablet PC, che viene installata con l'SDK.</span><span class="sxs-lookup"><span data-stu-id="d2b5b-107">First, reference the Tablet PC API, which are installed with the SDK.</span></span>


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a><span data-ttu-id="d2b5b-108">Inizializzare l'oggetto InkCollector</span><span class="sxs-lookup"><span data-stu-id="d2b5b-108">Initialize the InkCollector</span></span>

<span data-ttu-id="d2b5b-109">Nell'esempio viene aggiunto il codice al gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form che consente di associare l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)), InkCollector, alla finestra di gruppo e di abilitare l'oggetto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="d2b5b-109">The sample adds code to the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler that serves to associate the [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, with the group box window and enable the InkCollector.</span></span>


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



## <a name="recognize-the-strokes"></a><span data-ttu-id="d2b5b-110">Riconoscere i tratti</span><span class="sxs-lookup"><span data-stu-id="d2b5b-110">Recognize the Strokes</span></span>

<span data-ttu-id="d2b5b-111">Il gestore dell'evento [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) dell'oggetto [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) verifica che l'utente disponga di almeno un riconoscimento installato esaminando la proprietà [count](/previous-versions/ms828521(v=msdn.10)) della raccolta [Recognizers](/previous-versions/ms828520(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d2b5b-111">The [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) object's [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event handler checks to ensure that the user has at least one recognizer installed by examining the [Count](/previous-versions/ms828521(v=msdn.10)) property of the [Recognizers](/previous-versions/ms828520(v=msdn.10)) collection.</span></span>

<span data-ttu-id="d2b5b-112">La proprietà [SelectedText](/previous-versions/windows/) della casella di testo è impostata sulla corrispondenza migliore per i tratti usando il metodo [ToString](/previous-versions/ms827836(v=msdn.10)) nella raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d2b5b-112">The [SelectedText](/previous-versions/windows/) property of the text box is set to the best match for the strokes using the [ToString](/previous-versions/ms827836(v=msdn.10)) method on the [Strokes](/previous-versions/ms552701(v=vs.100)) collection.</span></span> <span data-ttu-id="d2b5b-113">Dopo essere stati riconosciuti, i tratti vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="d2b5b-113">After the strokes have been recognized, they are deleted.</span></span> <span data-ttu-id="d2b5b-114">Infine, il codice forza il ridisegno dell'area di disegno, deselezionando il codice per un ulteriore utilizzo di input penna.</span><span class="sxs-lookup"><span data-stu-id="d2b5b-114">Finally, the code forces drawing area repaint, clearing it for further ink use.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="d2b5b-115">Chiusura del modulo</span><span class="sxs-lookup"><span data-stu-id="d2b5b-115">Closing the Form</span></span>

<span data-ttu-id="d2b5b-116">Il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo Elimina l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d2b5b-116">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
