---
title: Incorporamento del controllo Media Player Windows in una soluzione Visual Basic .NET
description: Incorporamento del controllo Media Player Windows in una soluzione Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, Visual Basic .NET
- Modello a oggetti di Windows Media Player, Visual Basic .NET
- modello a oggetti, Visual Basic .NET
- Windows Media Player Mobile Visual Basic .NET
- Controllo ActiveX di Windows Media Player, Visual Basic .NET
- Controllo ActiveX Windows Media Player Mobile Visual Basic .NET
- Controllo ActiveX, Visual Basic .NET
- incorporamento, programmi Visual Basic .NET
- Incorporamento del programma Visual Basic .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332879"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="d074d-119">Incorporamento del controllo Media Player Windows in una soluzione Visual Basic .NET</span><span class="sxs-lookup"><span data-stu-id="d074d-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="d074d-120">Per usare la funzionalità di Windows Media Player 9 o versioni successive in un'applicazione Visual Basic .NET, aggiungere prima di tutto il componente a un modulo, come descritto in [uso del controllo windows media player con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="d074d-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="d074d-121">In questa sezione viene descritto come creare un'applicazione che riproduce video e con pulsanti di riproduzione e arresto personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d074d-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="d074d-122">Aggiungere la finestra video</span><span class="sxs-lookup"><span data-stu-id="d074d-122">Add the Video Window</span></span>

<span data-ttu-id="d074d-123">Aggiungere il controllo Media Player Windows a un modulo.</span><span class="sxs-lookup"><span data-stu-id="d074d-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="d074d-124">Ridimensionare il controllo e posizionarlo nel punto in cui si desidera visualizzare la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="d074d-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="d074d-125">Selezionare il controllo Media Player Windows, quindi impostare la proprietà **uiMode** su "None".</span><span class="sxs-lookup"><span data-stu-id="d074d-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="d074d-126">Questa impostazione nasconde i controlli dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d074d-126">This setting hides the UI controls.</span></span> <span data-ttu-id="d074d-127">Quando l'utente riproduce un video, viene visualizzato nella finestra.</span><span class="sxs-lookup"><span data-stu-id="d074d-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="d074d-128">Per il contenuto solo audio, viene visualizzata una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d074d-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="d074d-129">Aggiungere due pulsanti e modificare il modulo</span><span class="sxs-lookup"><span data-stu-id="d074d-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="d074d-130">Aggiungere ora due pulsanti al modulo.</span><span class="sxs-lookup"><span data-stu-id="d074d-130">Now add two buttons to the form.</span></span> <span data-ttu-id="d074d-131">Selezionare il primo pulsante e modificare la proprietà **Text** in "Play".</span><span class="sxs-lookup"><span data-stu-id="d074d-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="d074d-132">Selezionare il secondo pulsante e modificarne la proprietà **Text** in "Stop".</span><span class="sxs-lookup"><span data-stu-id="d074d-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="d074d-133">Aggiungere il codice di riproduzione</span><span class="sxs-lookup"><span data-stu-id="d074d-133">Add the Play Code</span></span>

<span data-ttu-id="d074d-134">Fare doppio clic sul pulsante **Riproduci** per visualizzare la finestra del codice.</span><span class="sxs-lookup"><span data-stu-id="d074d-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="d074d-135">Viene visualizzato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d074d-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="d074d-136">Aggiungere questa riga alla subroutine:</span><span class="sxs-lookup"><span data-stu-id="d074d-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="d074d-137">Nell'esempio di codice precedente, "axWindowsMediaPlayer1" è il nome predefinito del controllo Media Player di Windows e "c: \\ mediafile. wmv" è un segnaposto per il nome del file multimediale che si desidera riprodurre.</span><span class="sxs-lookup"><span data-stu-id="d074d-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="d074d-138">Se è stato aggiunto il contenuto multimediale digitale da Windows Media Player SDK alla libreria in Windows Media Player, è possibile usare questo codice:</span><span class="sxs-lookup"><span data-stu-id="d074d-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="d074d-139">Poiché la proprietà **autostart** è true per impostazione predefinita, Windows Media Player inizierà a essere riprodotto quando si imposta la proprietà **currentPlaylist** o **URL** .</span><span class="sxs-lookup"><span data-stu-id="d074d-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="d074d-140">Aggiungere il codice di arresto</span><span class="sxs-lookup"><span data-stu-id="d074d-140">Add the Stop Code</span></span>

<span data-ttu-id="d074d-141">Fare doppio clic sul pulsante **Arresta** per visualizzare la finestra del codice.</span><span class="sxs-lookup"><span data-stu-id="d074d-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="d074d-142">Viene visualizzato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d074d-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="d074d-143">Aggiungere questa riga alla subroutine:</span><span class="sxs-lookup"><span data-stu-id="d074d-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="d074d-144">Il wrapper di codice gestito per il controllo Media Player di Windows espone l'oggetto **Controls** come **Ctlcontrols** per evitare conflitti con la proprietà **Controls** ereditata da **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="d074d-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="d074d-145">Aggiungere la gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="d074d-145">Add Error-handling</span></span>

<span data-ttu-id="d074d-146">Il controllo Media Player Windows non genera un'eccezione quando viene rilevato un errore, ad esempio un URL non valido.</span><span class="sxs-lookup"><span data-stu-id="d074d-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="d074d-147">Il controllo segnala invece un evento.</span><span class="sxs-lookup"><span data-stu-id="d074d-147">Instead, the control signals an event.</span></span> <span data-ttu-id="d074d-148">L'applicazione deve gestire gli eventi di errore inviati dal lettore.</span><span class="sxs-lookup"><span data-stu-id="d074d-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="d074d-149">Per creare un gestore eventi, aprire la finestra del codice per la classe del form.</span><span class="sxs-lookup"><span data-stu-id="d074d-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="d074d-150">Dall'elenco a discesa nella parte superiore della finestra selezionare il controllo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d074d-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="d074d-151">Viene visualizzato un elenco di eventi nell'elenco a discesa a destra.</span><span class="sxs-lookup"><span data-stu-id="d074d-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="d074d-152">Dall'elenco selezionare [**errore MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span><span class="sxs-lookup"><span data-stu-id="d074d-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="d074d-153">Viene visualizzato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d074d-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="d074d-154">Il codice seguente può essere inserito nella subroutine per fornire una funzionalità di gestione degli errori minima.</span><span class="sxs-lookup"><span data-stu-id="d074d-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="d074d-155">Si noti che le informazioni sull'errore possono essere recuperate dall'argomento **\_ WMPOCXEvents \_ MediaErrorEvent** .</span><span class="sxs-lookup"><span data-stu-id="d074d-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a><span data-ttu-id="d074d-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d074d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d074d-157">**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="d074d-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




