---
title: Incorporamento del controllo Windows Media Player in una Visual Basic .NET
description: Incorporamento del controllo Windows Media Player in una Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Mobile, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player Controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player,Visual Basic .NET
- Windows Media Player a oggetti, Visual Basic .NET
- modello a oggetti, Visual Basic .NET
- Windows Media Player Mobile,Visual Basic .NET
- Windows Media Player ActiveX controllo, Visual Basic .NET
- Windows Media Player Controllo ActiveX per dispositivi mobili, Visual Basic .NET
- ActiveX, Visual Basic .NET
- incorporamento, Visual Basic programmi .NET
- Visual Basic incorporamento di programmi .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819387ac9d04f1ff229ff3665257324eddd042b15dff562a55f085a0fc86ca48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935253"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Incorporamento del controllo Windows Media Player in una Visual Basic .NET

Per usare la funzionalità di Windows Media Player serie 9 o successiva in un'applicazione .NET Visual Basic, aggiungere prima il componente a un form come descritto in Uso del controllo [Windows Media Player con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

Questa sezione descrive come creare un'applicazione che riproduce video e dispone di pulsanti di riproduzione e arresto personalizzati.

## <a name="add-the-video-window"></a>Aggiungere la finestra video

Aggiungere il Windows Media Player controllo a un form. Ridimensionare il controllo e posizionarlo nel punto in cui si vuole visualizzare la finestra video.

Selezionare il Windows Media Player controllo, quindi modificare la **proprietà uiMode** in "none". Questa impostazione nasconde i controlli dell'interfaccia utente. Quando l'utente riproduce un video, verrà visualizzato nella finestra. Per il contenuto solo audio, verrà visualizzata una visualizzazione.

## <a name="add-two-buttons-and-adjust-the-form"></a>Aggiungere due pulsanti e modificare il modulo

Aggiungere ora due pulsanti al form. Selezionare il primo pulsante e impostare la **proprietà Text** su "Play". Selezionare il secondo pulsante e impostarne **la proprietà Text** su "Stop".

## <a name="add-the-play-code"></a>Aggiungere il codice di riproduzione

Fare doppio clic sul **pulsante Riproduci** per visualizzare la finestra Codice. Viene visualizzato il codice seguente:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Aggiungere questa riga alla subroutine:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



Nell'esempio di codice precedente "axWindowsMediaPlayer1" è il nome predefinito del controllo Windows Media Player e "c: mediafile.wmv" è un segnaposto per il nome del supporto da \\ riprodurre.

Se è stato aggiunto il contenuto multimediale digitale da Windows Media Player SDK alla libreria in Windows Media Player, è possibile usare questo codice:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Poiché la **proprietà autoStart** è true per impostazione predefinita, Windows Media Player verrà avviata la riproduzione quando si imposta la **proprietà currentPlaylist** **o URL.**

## <a name="add-the-stop-code"></a>Aggiungere il codice di arresto

Fare doppio clic sul **pulsante Arresta** per visualizzare la finestra Codice. Viene visualizzato il codice seguente:


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
> Il wrapper di codice gestito per il controllo Windows Media Player espone l'oggetto **Controls** come **Ctlcontrols** per evitare conflitti con la proprietà **Controls** ereditata da **System.Windows. Forms.Control**.

 

## <a name="add-error-handling"></a>Aggiungere la gestione degli errori

Il Windows Media Player non genera un'eccezione quando rileva un errore, ad esempio un URL non valido. Al contrario, il controllo segnala un evento . L'applicazione deve gestire gli eventi di errore inviati dal lettore.

Per creare un gestore eventi, aprire la finestra del codice per la classe del form. Nell'elenco a discesa nella parte superiore della finestra selezionare il Windows Media Player controllo. Nell'elenco a discesa a destra viene visualizzato un elenco di eventi. Nell'elenco selezionare [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md). Viene visualizzato il codice seguente:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



Il codice seguente può essere inserito nella subroutine per fornire una funzionalità di gestione degli errori minima. Si noti che le informazioni sull'errore possono essere recuperate **\_ dall'argomento WMPOCXEvents \_ MediaErrorEvent.**


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

[**Incorporamento del controllo Windows Media Player in una .NET Framework soluzione**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




