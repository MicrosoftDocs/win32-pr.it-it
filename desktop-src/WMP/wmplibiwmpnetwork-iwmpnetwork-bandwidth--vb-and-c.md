---
title: Proprietà della larghezza di banda IWMPNetwork
description: La proprietà bandWidth ottiene la larghezza di banda corrente dell'elemento multimediale.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- Proprietà della larghezza di banda di Windows Media Player
- Proprietà della larghezza di banda Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà bandWidth
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
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327142"
---
# <a name="iwmpnetworkbandwidth-property"></a>Proprietà IWMPNetwork:: bandWidth

La proprietà **Bandwidth** ottiene la larghezza di banda corrente dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta la larghezza di banda.

## <a name="remarks"></a>Commenti

Il valore recuperato tramite **AxWindowsMediaPlayer. URL** sarà zero se l'URL non è impostato. Questa proprietà è valida solo per i flussi multimediali.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata la **larghezza di banda** per visualizzare la larghezza di banda media corrente. Le informazioni vengono visualizzate in un'etichetta in risposta all'evento **PlayStateChange** . L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





