---
title: Creazione del controllo Windows Media Player a livello di codice
description: Creazione del controllo Windows Media Player a livello di codice
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player,creazione di un ActiveX a livello di codice
- Windows Media Player a oggetti, creazione di un ActiveX a livello di codice
- modello a oggetti, creazione di ActiveX a livello di codice
- Windows Media Player Dispositivi mobili, creazione di ActiveX a livello di codice
- Windows Media Player ActiveX, creazione a livello di codice
- Windows Media Player controllo ActiveX mobile, creazione a livello di codice
- ActiveX, creazione a livello di codice
- creazione di ActiveX a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57b3f4ba9d8c297aee9feb14fc05a35306e1a85d8a718aef6721b92475e19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340964"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Creazione del controllo Windows Media Player a livello di codice

Quando si aggiunge il Windows Media Player a un form dalla casella degli strumenti, viene creato un oggetto della classe **AxWMPLib.AxWindowsMediaPlayer.** Questa classe wrapper fornisce al lettore tutte le funzionalità di un controllo ActiveX, incluso l'accesso alle proprietà dell'interfaccia utente, ad esempio **Location** e **Size.**

Se non sono necessarie le proprietà esposte da **AxWindowsMediaPlayer** o se l'applicazione non ha un'interfaccia utente grafica, è possibile creare un controllo Player a livello di codice. In questo caso, si crea un oggetto della **classe WMPLib.WindowsMediaPlayer.**

> [!Note]  
> Poiché non viene eseguito il wrapping dell'oggetto **WindowsMediaPlayer** come controllo ActiveX, non ha proprietà ereditate da **System.Windows. Forms.Control**. Di conseguenza, la **proprietà Controls** non viene rinominata **in CtlControls,** come in **AxWindowsMediaPlayer.**

 

Per creare il Windows Media Player a livello di codice, è necessario innanzitutto aggiungere un riferimento a wmp.dll, disponibile nella \\ cartella Windows \\ system32. L'aggiunta di questo riferimento WMPLib.dll nella cartella del progetto e un riferimento a WMPLib viene visualizzato in Esplora soluzioni.

Il codice di esempio seguente, parte di una classe Form1, illustra come creare un oggetto **Player** e riprodurre un file. Al termine della riproduzione o se non è possibile riprodurre il file, il modulo viene chiuso.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Incorporamento del controllo Windows Media Player in una .NET Framework soluzione**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




