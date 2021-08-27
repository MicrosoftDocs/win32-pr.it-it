---
title: Proprietà IWMPNetwork bandWidth
description: La proprietà bandWidth ottiene la larghezza di banda corrente dell'elemento multimediale.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- Proprietà bandWidth Windows Media Player
- Proprietà bandWidth Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player , proprietà bandWidth
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3cccc47d16f272a28fb732641a9fca743003f716e79a340df8de5d55e9ce6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098731"
---
# <a name="iwmpnetworkbandwidth-property"></a>Proprietà IWMPNetwork::bandWidth

La **proprietà bandWidth** ottiene la larghezza di banda corrente dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta la larghezza di banda.

## <a name="remarks"></a>Commenti

Il valore recuperato tramite **AxWindowsMediaPlayer.URL** sarà zero se l'URL non è impostato. Questa proprietà è valida solo per i supporti di streaming.

## <a name="examples"></a>Esempio

L'esempio seguente usa **bandWidth** per visualizzare la larghezza di banda multimediale corrente. Le informazioni vengono visualizzate in un'etichetta in risposta **all'evento PlayStateChange.** **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





