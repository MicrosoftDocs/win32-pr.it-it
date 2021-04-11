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
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Incorporamento del controllo Media Player Windows in una soluzione Visual Basic .NET

Per usare la funzionalità di Windows Media Player 9 o versioni successive in un'applicazione Visual Basic .NET, aggiungere prima di tutto il componente a un modulo, come descritto in [uso del controllo windows media player con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

In questa sezione viene descritto come creare un'applicazione che riproduce video e con pulsanti di riproduzione e arresto personalizzati.

## <a name="add-the-video-window"></a>Aggiungere la finestra video

Aggiungere il controllo Media Player Windows a un modulo. Ridimensionare il controllo e posizionarlo nel punto in cui si desidera visualizzare la finestra del video.

Selezionare il controllo Media Player Windows, quindi impostare la proprietà **uiMode** su "None". Questa impostazione nasconde i controlli dell'interfaccia utente. Quando l'utente riproduce un video, viene visualizzato nella finestra. Per il contenuto solo audio, viene visualizzata una visualizzazione.

## <a name="add-two-buttons-and-adjust-the-form"></a>Aggiungere due pulsanti e modificare il modulo

Aggiungere ora due pulsanti al modulo. Selezionare il primo pulsante e modificare la proprietà **Text** in "Play". Selezionare il secondo pulsante e modificarne la proprietà **Text** in "Stop".

## <a name="add-the-play-code"></a>Aggiungere il codice di riproduzione

Fare doppio clic sul pulsante **Riproduci** per visualizzare la finestra del codice. Viene visualizzato il codice seguente:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Aggiungere questa riga alla subroutine:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



Nell'esempio di codice precedente, "axWindowsMediaPlayer1" è il nome predefinito del controllo Media Player di Windows e "c: \\ mediafile. wmv" è un segnaposto per il nome del file multimediale che si desidera riprodurre.

Se è stato aggiunto il contenuto multimediale digitale da Windows Media Player SDK alla libreria in Windows Media Player, è possibile usare questo codice:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Poiché la proprietà **autostart** è true per impostazione predefinita, Windows Media Player inizierà a essere riprodotto quando si imposta la proprietà **currentPlaylist** o **URL** .

## <a name="add-the-stop-code"></a>Aggiungere il codice di arresto

Fare doppio clic sul pulsante **Arresta** per visualizzare la finestra del codice. Viene visualizzato il codice seguente:


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



Aggiungere questa riga alla subroutine:


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> Il wrapper di codice gestito per il controllo Media Player di Windows espone l'oggetto **Controls** come **Ctlcontrols** per evitare conflitti con la proprietà **Controls** ereditata da **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Aggiungere la gestione degli errori

Il controllo Media Player Windows non genera un'eccezione quando viene rilevato un errore, ad esempio un URL non valido. Il controllo segnala invece un evento. L'applicazione deve gestire gli eventi di errore inviati dal lettore.

Per creare un gestore eventi, aprire la finestra del codice per la classe del form. Dall'elenco a discesa nella parte superiore della finestra selezionare il controllo Windows Media Player. Viene visualizzato un elenco di eventi nell'elenco a discesa a destra. Dall'elenco selezionare [**errore MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md). Viene visualizzato il codice seguente:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



Il codice seguente può essere inserito nella subroutine per fornire una funzionalità di gestione degli errori minima. Si noti che le informazioni sull'errore possono essere recuperate dall'argomento **\_ WMPOCXEvents \_ MediaErrorEvent** .


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




