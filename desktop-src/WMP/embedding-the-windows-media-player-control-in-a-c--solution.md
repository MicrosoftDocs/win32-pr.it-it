---
title: Incorporamento del controllo Windows Media Player in una soluzione C
description: Incorporamento del controllo Windows Media Player in una soluzione C\
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Dispositivi mobili, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player,C
- Windows Media Player a oggetti, C
- modello a oggetti,C
- Windows Media Player Dispositivi mobili, C
- Windows Media Player ActiveX controllo, C
- Windows Media Player Controllo ActiveX per dispositivi mobili,C
- ActiveX controllo, C
- incorporamento, programmi C
- Incorporamento del programma C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a067a407fccdd78d71d9e60bc00d1eae6950e3fdaf204f886c5e96edf372eb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901981"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Incorporamento del controllo Windows Media Player in una soluzione C#

Per usare la funzionalità di Windows Media Player in un'applicazione [C#,](using-the-windows-media-player-control-with-microsoft-visual-studio.md) aggiungere prima di tutto il componente a un form come descritto in Uso del controllo Windows Media Player con Microsoft Visual Studio

Le sezioni seguenti descrivono come creare un'applicazione che riproduce video e usa pulsanti di riproduzione e arresto personalizzati.

## <a name="add-the-video-window"></a>Aggiungere la finestra video

Aggiungere il Windows Media Player ActiveX a un form. Ridimensionare il controllo e posizionarlo nel punto in cui si vuole visualizzare la finestra video.

Selezionare il Windows Media Player controllo, quindi modificare la **proprietà uiMode** in "none". Questa impostazione nasconde i controlli dell'interfaccia utente. Quando l'utente riproduce un video, verrà visualizzato nella finestra. Per il contenuto solo audio, verrà visualizzata una visualizzazione.

## <a name="add-two-buttons-and-adjust-the-form"></a>Aggiungere due pulsanti e modificare il form

Aggiungere ora due pulsanti al form. Selezionare il primo pulsante e modificare la **proprietà Text** in "Play". Selezionare il secondo pulsante e modificarne **la proprietà Text** in "Stop".

## <a name="add-the-play-code"></a>Aggiungere il codice di riproduzione

Fare doppio clic sul **pulsante Riproduci** per visualizzare la finestra Codice. In C# verrà visualizzato il codice seguente:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Aggiungere questa riga tra le due parentesi graffe:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



Nell'esempio di codice precedente "axWindowsMediaPlayer1" è il nome predefinito del controllo Windows Media Player e "c: mediafile.wmv" è un segnaposto per il nome dell'elemento multimediale che si \\ vuole riprodurre. È possibile usare qualsiasi percorso di file valido. Il simbolo @ indica al compilatore di non interpretare le barre rovesciate come caratteri di escape.

Se è stato aggiunto il contenuto multimediale digitale da Windows Media Player SDK alla libreria in Windows Media Player, è possibile usare invece questo codice:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Poiché la **proprietà autoStart** è true per impostazione predefinita, Windows Media Player verrà avviata la riproduzione quando si imposta la **proprietà currentPlaylist** **o URL.**

## <a name="add-the-stop-code"></a>Aggiungere il codice di arresto

Fare doppio clic sul **pulsante Arresta** per visualizzare la finestra Codice. In C# verrà visualizzato il codice seguente:


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Aggiungere questa riga tra le due parentesi graffe:


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> Il wrapper di codice gestito per il controllo Windows Media Player espone l'oggetto **Controls** come **Ctlcontrols** per evitare conflitti con la proprietà **Controls** ereditata da **System.Windows. Forms.Control**.

 

## <a name="add-error-handling"></a>Aggiungere la gestione degli errori

Il Windows Media Player non genera un'eccezione quando rileva un errore, ad esempio un URL non valido. Segnala invece un evento. L'applicazione deve gestire gli eventi di errore inviati dal lettore.

Per creare un gestore eventi, aprire prima il Finestra Proprietà per il Windows Media Player controllo . Nell'elenco degli eventi fare doppio clic su **MediaError**. Viene visualizzato il codice seguente:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



Il codice seguente può essere inserito nel metodo per fornire funzionalità minime di gestione degli errori. Si noti che le informazioni sull'errore possono essere recuperate **\_ dall'argomento \_ MediaErrorEvent di WMPOCXEvents.**


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Incorporamento del controllo Windows Media Player in una .NET Framework soluzione**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




