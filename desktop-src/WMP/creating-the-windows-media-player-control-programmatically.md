---
title: Creazione del controllo Media Player Windows a livello di codice
description: Creazione del controllo Media Player Windows a livello di codice
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player, creazione di un controllo ActiveX a livello di codice
- Modello a oggetti di Windows Media Player, creazione di controlli ActiveX a livello di codice
- modello a oggetti, creazione di un controllo ActiveX a livello di codice
- Windows Media Player Mobile, creazione di un controllo ActiveX a livello di codice
- Controllo ActiveX di Windows Media Player, creazione a livello di codice
- Controllo ActiveX Windows Media Player Mobile, creazione a livello di codice
- Controllo ActiveX, creazione a livello di codice
- creazione di un controllo ActiveX a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332871"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a><span data-ttu-id="6c136-111">Creazione del controllo Media Player Windows a livello di codice</span><span class="sxs-lookup"><span data-stu-id="6c136-111">Creating the Windows Media Player Control Programmatically</span></span>

<span data-ttu-id="6c136-112">Quando si aggiunge il controllo Media Player Windows a un form dalla casella degli strumenti, viene creato un oggetto della classe **AxWMPLib. AxWindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="6c136-112">When you add the Windows Media Player control to a form from the Toolbox, an object of the class **AxWMPLib.AxWindowsMediaPlayer** is created.</span></span> <span data-ttu-id="6c136-113">Questa classe wrapper fornisce al lettore tutte le funzionalità di un controllo ActiveX, incluso l'accesso alle proprietà dell'interfaccia utente, ad esempio la **posizione** e le **dimensioni**.</span><span class="sxs-lookup"><span data-stu-id="6c136-113">This wrapper class gives the Player all the functionality of an ActiveX control, including access to UI properties such as **Location** and **Size**.</span></span>

<span data-ttu-id="6c136-114">Se non sono necessarie le proprietà esposte da **AxWindowsMediaPlayer** o se l'applicazione non dispone di un'interfaccia utente grafica, è possibile creare un controllo lettore a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="6c136-114">If you do not require the properties exposed by **AxWindowsMediaPlayer**, or if your application does not have a graphical user interface, you can create a Player control programmatically.</span></span> <span data-ttu-id="6c136-115">In questo caso, si crea un oggetto della classe **wmplib. WindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="6c136-115">In this case, you create an object of the **WMPLib.WindowsMediaPlayer** class.</span></span>

> [!Note]  
> <span data-ttu-id="6c136-116">Poiché l'oggetto **windowsmediaplayer** non viene incapsulato come controllo ActiveX, non dispone di alcuna proprietà ereditata da **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="6c136-116">Because the **WindowsMediaPlayer** object is not wrapped as an ActiveX control, it does not have any properties inherited from **System.Windows.Forms.Control**.</span></span> <span data-ttu-id="6c136-117">Di conseguenza, la proprietà **Controls** non viene rinominata in **CtlControls**, così come si trova in **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="6c136-117">As a result, the **Controls** property is not renamed to **CtlControls**, as it is in **AxWindowsMediaPlayer**.</span></span>

 

<span data-ttu-id="6c136-118">Per creare il controllo Media Player di Windows a livello di codice, è innanzitutto necessario aggiungere un riferimento a wmp.dll, disponibile nella \\ \\ cartella system32 di Windows.</span><span class="sxs-lookup"><span data-stu-id="6c136-118">To create the Windows Media Player control programmatically, you must first add a reference to wmp.dll, which is found in the \\Windows\\system32 folder.</span></span> <span data-ttu-id="6c136-119">L'aggiunta di questo riferimento crea WMPLib.dll nella cartella del progetto e viene visualizzato un riferimento a WMPLib in Esplora soluzioni.</span><span class="sxs-lookup"><span data-stu-id="6c136-119">Adding this reference creates WMPLib.dll in your project folder, and a reference to WMPLib appears in Solution Explorer.</span></span>

<span data-ttu-id="6c136-120">Il codice di esempio seguente, parte di una classe Form1, Mostra come creare un oggetto **Player** e riprodurre un file.</span><span class="sxs-lookup"><span data-stu-id="6c136-120">The following example code, part of a Form1 class, shows how to create a **Player** object and play a file.</span></span> <span data-ttu-id="6c136-121">Al termine della riproduzione o se il file non può essere riprodotto, il form viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="6c136-121">When playback ends, or if the file cannot be played, the form is closed.</span></span>


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a><span data-ttu-id="6c136-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c136-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c136-123">**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="6c136-123">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




