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
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Incorporamento del controllo Media Player Windows in una soluzione C#

Per usare la funzionalità di Windows Media Player in un'applicazione C#, aggiungere prima di tutto il componente a un modulo come descritto in [uso del controllo Media Player Windows con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

Le sezioni seguenti descrivono come creare un'applicazione che riproduce video e usa pulsanti di riproduzione e arresto personalizzati.

## <a name="add-the-video-window"></a>Aggiungere la finestra video

Aggiungere il controllo ActiveX di Windows Media Player a un modulo. Ridimensionare il controllo e posizionarlo nel punto in cui si desidera visualizzare la finestra del video.

Selezionare il controllo Media Player Windows, quindi impostare la proprietà **uiMode** su "None". Questa impostazione nasconde i controlli dell'interfaccia utente. Quando l'utente riproduce un video, viene visualizzato nella finestra. Per il contenuto solo audio, viene visualizzata una visualizzazione.

## <a name="add-two-buttons-and-adjust-the-form"></a>Aggiungere due pulsanti e modificare il modulo

A questo punto, aggiungere due pulsanti al modulo. Selezionare il primo pulsante e modificare la proprietà **Text** in "Play". Selezionare il secondo pulsante e modificarne la proprietà **Text** in "Stop".

## <a name="add-the-play-code"></a>Aggiungere il codice di riproduzione

Fare doppio clic sul pulsante **Riproduci** per visualizzare la finestra del codice. In C# verrà visualizzato il codice seguente:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Aggiungere questa riga tra le due parentesi graffe:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



Nell'esempio di codice precedente, "axWindowsMediaPlayer1" è il nome predefinito del controllo Media Player di Windows e "c: \\ mediafile. wmv" è un segnaposto per il nome dell'elemento multimediale che si desidera riprodurre. È possibile utilizzare qualsiasi percorso di file valido. Il simbolo @ indica al compilatore di non interpretare le barre rovesciate come caratteri di escape.

Se è stato aggiunto il contenuto multimediale digitale da Windows Media Player SDK alla libreria in Windows Media Player, è possibile usare questo codice:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Poiché la proprietà **autostart** è true per impostazione predefinita, Windows Media Player inizierà a essere riprodotto quando si imposta la proprietà **currentPlaylist** o **URL** .

## <a name="add-the-stop-code"></a>Aggiungere il codice di arresto

Fare doppio clic sul pulsante **Arresta** per visualizzare la finestra del codice. In C# verrà visualizzato il codice seguente:


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
> Il wrapper di codice gestito per il controllo Media Player di Windows espone l'oggetto **Controls** come **Ctlcontrols** per evitare conflitti con la proprietà **Controls** ereditata da **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Aggiungere la gestione degli errori

Il controllo Media Player Windows non genera un'eccezione quando viene rilevato un errore, ad esempio un URL non valido. Segnala invece un evento. L'applicazione deve gestire gli eventi di errore inviati dal lettore.

Per creare un gestore eventi, aprire innanzitutto il Finestra Proprietà per il controllo Media Player di Windows. Nell'elenco di eventi fare doppio clic su **errore MediaError**. Viene visualizzato il codice seguente:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



Il codice seguente può essere inserito nel metodo per fornire una funzionalità di gestione degli errori minima. Si noti che le informazioni sull'errore possono essere recuperate dall'argomento **\_ WMPOCXEvents \_ MediaErrorEvent** .


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

[**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




