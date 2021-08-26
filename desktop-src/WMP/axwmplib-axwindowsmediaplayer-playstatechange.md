---
title: Evento PlayStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PlayStateChange si verifica quando cambia lo stato di riproduzione Windows Media Player controllo.
ms.assetid: f8823c90-2084-4771-a2fe-7081d4e49e63
keywords:
- Evento PlayStateChange dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PlayStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a02f533211ccb6f2f2617d402eed8343a444fad4a7c3ccf49e187ede71ce9513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003991"
---
# <a name="playstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento PlayStateChange dell'oggetto AxWindowsMediaPlayer

L'evento PlayStateChange si verifica quando cambia lo stato di riproduzione Windows Media Player controllo.

``` syntax
[C#]
private void player_PlayStateChange(
  object sender,
  _WMPOCXEvents_PlayStateChangeEvent e
)

[Visual Basic]
 Private Sub player_PlayStateChange(   
 sender As Object,  
 e As _WMPOCXEvents_PlayStateChangeEvent 
 ) Handles player.PlayStateChange
 
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlayStateChangeEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlayStateChangeEvent**, che contiene la proprietà seguente correlata a questo evento.



| Proprietà     | Descrizione                                     |
|--------------|-------------------------------------------------|
| **newState** | System.Int32Specifica il nuovo stato.<br/> |



 

## <a name="remarks"></a>Commenti

Windows Media Player non è garantito che gli stati si verifichino in un ordine particolare. Inoltre, non tutti gli stati si verificano necessariamente durante una sequenza di eventi. È consigliabile non scrivere codice che si basa sull'ordine di stato.

## <a name="examples"></a>Esempio

L'esempio seguente illustra un gestore eventi per l'evento PlayStateChange che visualizza lo stato di riproduzione corrente in un'etichetta. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test the current state of the player and display a message for each state.
    switch (e.newState)
    {
        case 0:    // Undefined
            currentStateLabel.Text = "Undefined";
            break;

        case 1:    // Stopped
            currentStateLabel.Text = "Stopped";
            break;

        case 2:    // Paused
            currentStateLabel.Text = "Paused";
            break;

        case 3:    // Playing
            currentStateLabel.Text = "Playing";
            break;

        case 4:    // ScanForward
            currentStateLabel.Text = "ScanForward";
            break;

        case 5:    // ScanReverse
            currentStateLabel.Text = "ScanReverse";
            break;

        case 6:    // Buffering
            currentStateLabel.Text = "Buffering";
            break;

        case 7:    // Waiting
            currentStateLabel.Text = "Waiting";
            break;

        case 8:    // MediaEnded
            currentStateLabel.Text = "MediaEnded";
            break;

        case 9:    // Transitioning
            currentStateLabel.Text = "Transitioning";
            break;

        case 10:   // Ready
            currentStateLabel.Text = "Ready";
            break;

        case 11:   // Reconnecting
            currentStateLabel.Text = "Reconnecting";
            break;

        case 12:   // Last
            currentStateLabel.Text = "Last";
            break;

        default:
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString());
            break;
    }
}
```




```VB
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    ' Test the current state of the player, display a message for each state.
    Select Case e.newState

        Case 0 ' Undefined
            currentStateLabel.Text = "Undefined"

        Case 1 ' Stopped
            currentStateLabel.Text = "Stopped"

        Case 2 ' Paused
            currentStateLabel.Text = "Paused"

        Case 3 ' Playing
            currentStateLabel.Text = "Playing"

        Case 4 ' ScanForward
            currentStateLabel.Text = "ScanForward"

        Case 5 ' ScanReverse
            currentStateLabel.Text = "ScanReverse"

        Case 6 ' Buffering
            currentStateLabel.Text = "Buffering"

        Case 7 ' Waiting
            currentStateLabel.Text = "Waiting"

        Case 8 ' MediaEnded
            currentStateLabel.Text = "MediaEnded"

        Case 9 ' Transitioning
            currentStateLabel.Text = "Transitioning"

        Case 10 ' Ready
            currentStateLabel.Text = "Ready"

        Case 11 ' Reconnecting
            currentStateLabel.Text = "Reconnecting"

        Case 12 ' Last
            currentStateLabel.Text = "Last"

        Case Else
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString())

    End Select

End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.playState (VB e C#)**](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> </dl>

 

 





