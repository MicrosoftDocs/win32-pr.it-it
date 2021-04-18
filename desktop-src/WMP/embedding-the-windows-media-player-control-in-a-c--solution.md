---
title: Incorporamento del controllo Media Player Windows in una soluzione C
description: Incorporamento del controllo Media Player Windows in una soluzione C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, C
- Modello a oggetti di Windows Media Player, C
- modello a oggetti, C
- Windows Media Player Mobile, C
- Controllo ActiveX di Windows Media Player, C
- Controllo ActiveX Windows Media Player Mobile, C
- Controllo ActiveX, C
- incorporamento, programmi C
- Incorporamento del programma C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299013"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a><span data-ttu-id="3d98f-119">Incorporamento del controllo Media Player Windows in una soluzione C#</span><span class="sxs-lookup"><span data-stu-id="3d98f-119">Embedding the Windows Media Player Control in a C# Solution</span></span>

<span data-ttu-id="3d98f-120">Per usare la funzionalità di Windows Media Player in un'applicazione C#, aggiungere prima di tutto il componente a un modulo come descritto in [uso del controllo Media Player Windows con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="3d98f-120">To use the functionality of Windows Media Player in a C# application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="3d98f-121">Le sezioni seguenti descrivono come creare un'applicazione che riproduce video e usa pulsanti di riproduzione e arresto personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3d98f-121">The following sections describe how to create an application that plays video and uses custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="3d98f-122">Aggiungere la finestra video</span><span class="sxs-lookup"><span data-stu-id="3d98f-122">Add the Video Window</span></span>

<span data-ttu-id="3d98f-123">Aggiungere il controllo ActiveX di Windows Media Player a un modulo.</span><span class="sxs-lookup"><span data-stu-id="3d98f-123">Add the Windows Media Player ActiveX control to a form.</span></span> <span data-ttu-id="3d98f-124">Ridimensionare il controllo e posizionarlo nel punto in cui si desidera visualizzare la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="3d98f-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="3d98f-125">Selezionare il controllo Media Player Windows, quindi impostare la proprietà **uiMode** su "None".</span><span class="sxs-lookup"><span data-stu-id="3d98f-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="3d98f-126">Questa impostazione nasconde i controlli dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3d98f-126">This setting hides the UI controls.</span></span> <span data-ttu-id="3d98f-127">Quando l'utente riproduce un video, viene visualizzato nella finestra.</span><span class="sxs-lookup"><span data-stu-id="3d98f-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="3d98f-128">Per il contenuto solo audio, viene visualizzata una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d98f-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="3d98f-129">Aggiungere due pulsanti e modificare il modulo</span><span class="sxs-lookup"><span data-stu-id="3d98f-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="3d98f-130">A questo punto, aggiungere due pulsanti al modulo.</span><span class="sxs-lookup"><span data-stu-id="3d98f-130">Now, add two buttons to the form.</span></span> <span data-ttu-id="3d98f-131">Selezionare il primo pulsante e modificare la proprietà **Text** in "Play".</span><span class="sxs-lookup"><span data-stu-id="3d98f-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="3d98f-132">Selezionare il secondo pulsante e modificarne la proprietà **Text** in "Stop".</span><span class="sxs-lookup"><span data-stu-id="3d98f-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="3d98f-133">Aggiungere il codice di riproduzione</span><span class="sxs-lookup"><span data-stu-id="3d98f-133">Add the Play Code</span></span>

<span data-ttu-id="3d98f-134">Fare doppio clic sul pulsante **Riproduci** per visualizzare la finestra del codice.</span><span class="sxs-lookup"><span data-stu-id="3d98f-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="3d98f-135">In C# verrà visualizzato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3d98f-135">In C#, the following code will be displayed:</span></span>


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="3d98f-136">Aggiungere questa riga tra le due parentesi graffe:</span><span class="sxs-lookup"><span data-stu-id="3d98f-136">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



<span data-ttu-id="3d98f-137">Nell'esempio di codice precedente, "axWindowsMediaPlayer1" è il nome predefinito del controllo Media Player di Windows e "c: \\ mediafile. wmv" è un segnaposto per il nome dell'elemento multimediale che si desidera riprodurre.</span><span class="sxs-lookup"><span data-stu-id="3d98f-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control, and "c:\\mediafile.wmv" is a placeholder for the name of the media item you want to play.</span></span> <span data-ttu-id="3d98f-138">È possibile utilizzare qualsiasi percorso di file valido.</span><span class="sxs-lookup"><span data-stu-id="3d98f-138">Any valid file path can be used.</span></span> <span data-ttu-id="3d98f-139">Il simbolo @ indica al compilatore di non interpretare le barre rovesciate come caratteri di escape.</span><span class="sxs-lookup"><span data-stu-id="3d98f-139">The @ symbol instructs the compiler to not interpret backslashes as escape characters.</span></span>

<span data-ttu-id="3d98f-140">Se è stato aggiunto il contenuto multimediale digitale da Windows Media Player SDK alla libreria in Windows Media Player, è possibile usare questo codice:</span><span class="sxs-lookup"><span data-stu-id="3d98f-140">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



<span data-ttu-id="3d98f-141">Poiché la proprietà **autostart** è true per impostazione predefinita, Windows Media Player inizierà a essere riprodotto quando si imposta la proprietà **currentPlaylist** o **URL** .</span><span class="sxs-lookup"><span data-stu-id="3d98f-141">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="3d98f-142">Aggiungere il codice di arresto</span><span class="sxs-lookup"><span data-stu-id="3d98f-142">Add the Stop Code</span></span>

<span data-ttu-id="3d98f-143">Fare doppio clic sul pulsante **Arresta** per visualizzare la finestra del codice.</span><span class="sxs-lookup"><span data-stu-id="3d98f-143">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="3d98f-144">In C# verrà visualizzato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3d98f-144">In C#, the following code will be displayed:</span></span>


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="3d98f-145">Aggiungere questa riga tra le due parentesi graffe:</span><span class="sxs-lookup"><span data-stu-id="3d98f-145">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> <span data-ttu-id="3d98f-146">Il wrapper di codice gestito per il controllo Media Player di Windows espone l'oggetto **Controls** come **Ctlcontrols** per evitare conflitti con la proprietà **Controls** ereditata da **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="3d98f-146">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="3d98f-147">Aggiungere la gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="3d98f-147">Add Error-handling</span></span>

<span data-ttu-id="3d98f-148">Il controllo Media Player Windows non genera un'eccezione quando viene rilevato un errore, ad esempio un URL non valido.</span><span class="sxs-lookup"><span data-stu-id="3d98f-148">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="3d98f-149">Segnala invece un evento.</span><span class="sxs-lookup"><span data-stu-id="3d98f-149">Instead, it signals an event.</span></span> <span data-ttu-id="3d98f-150">L'applicazione deve gestire gli eventi di errore inviati dal lettore.</span><span class="sxs-lookup"><span data-stu-id="3d98f-150">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="3d98f-151">Per creare un gestore eventi, aprire innanzitutto il Finestra Proprietà per il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="3d98f-151">To create an event handler, first open the Properties window for the Windows Media Player control.</span></span> <span data-ttu-id="3d98f-152">Nell'elenco di eventi fare doppio clic su **errore MediaError**.</span><span class="sxs-lookup"><span data-stu-id="3d98f-152">In the list of events, double-click **MediaError**.</span></span> <span data-ttu-id="3d98f-153">Viene visualizzato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3d98f-153">The following code is displayed:</span></span>


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



<span data-ttu-id="3d98f-154">Il codice seguente può essere inserito nel metodo per fornire una funzionalità di gestione degli errori minima.</span><span class="sxs-lookup"><span data-stu-id="3d98f-154">The following code could be inserted in the method to provide minimal error-handling capability.</span></span> <span data-ttu-id="3d98f-155">Si noti che le informazioni sull'errore possono essere recuperate dall'argomento **\_ WMPOCXEvents \_ MediaErrorEvent** .</span><span class="sxs-lookup"><span data-stu-id="3d98f-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a><span data-ttu-id="3d98f-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d98f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d98f-157">**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="3d98f-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




