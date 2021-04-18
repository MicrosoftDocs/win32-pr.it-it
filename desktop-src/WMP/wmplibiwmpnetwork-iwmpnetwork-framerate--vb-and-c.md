---
title: Proprietà frameRate IWMPNetwork
description: La proprietà frameRate ottiene la frequenza dei fotogrammi video corrente.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- proprietà frameRate Media Player di Windows
- proprietà frameRate Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà frameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325111"
---
# <a name="iwmpnetworkframerate-property"></a>Proprietà IWMPNetwork:: frameRate

La proprietà **framerate** ottiene la frequenza dei fotogrammi video corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che corrisponde alla frequenza dei fotogrammi corrente in frame per cento secondi.

> [!Note]  
> Sebbene la proprietà **encodedFrameRate** misuri la frequenza dei fotogrammi codificata in frame al secondo, la proprietà **framerate** misura la frequenza dei fotogrammi corrente in frame per cento secondi. Vedere la sezione Osservazioni.

 

## <a name="remarks"></a>Commenti

Il valore della frequenza dei fotogrammi corrente viene restituito in frame per cento secondi. Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo (fps).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene usato il **framerate** per visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato. Le informazioni vengono visualizzate in un'etichetta in risposta all'evento **PlayStateChange** . L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

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

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. encodedFrameRate (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





