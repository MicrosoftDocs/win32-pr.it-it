---
title: Proprietà downloadProgress di IWMPNetwork
description: La proprietà downloadProgress ottiene la percentuale di download completata.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Finestra delle proprietà di downloadProgress Media Player
- Proprietà di downloadProgress Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324525"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>IWMPNetwork::d proprietà ownloadProgress

La proprietà **downloadProgress** ottiene la percentuale di download completata.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta lo stato di avanzamento del download espresso come percentuale.

## <a name="remarks"></a>Commenti

Quando il controllo Windows Media Player è connesso a un file multimediale digitale che può essere riprodotto e scaricato nello stesso momento, la proprietà **downloadProgress** ottiene la percentuale del file totale che è stato scaricato. Questa funzionalità è attualmente supportata solo per i file multimediali digitali scaricati da server Web. È possibile scaricare e riprodurre simultaneamente un file di uno dei formati seguenti:

-   Advanced Systems Format (ASF)
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)
-   MP3
-   MPEG
-   WAV

Inoltre, alcuni file AVI possono essere scaricati e riprodotti simultaneamente.

Usare **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** per determinare quando il buffering viene avviato o arrestato.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene usato **downloadProgress** per visualizzare la percentuale di download completato. Le informazioni vengono visualizzate in un'etichetta, in risposta all'evento di **buffering** . Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento AxWindowsMediaPlayer. buffering (VB e C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





