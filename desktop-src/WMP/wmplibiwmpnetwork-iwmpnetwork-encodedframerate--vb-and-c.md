---
title: Proprietà encodedFrameRate IWMPNetwork
description: La proprietà encodedFrameRate ottiene la frequenza dei fotogrammi video specificata dall'autore del contenuto.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- Proprietà encodedFrameRate Windows Media Player
- Proprietà encodedFrameRate Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player , proprietà encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f8a08572f65e1e44027ed25d84acfe7d917f92bf4bb63d5d9b8cca1e1201d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000011"
---
# <a name="iwmpnetworkencodedframerate-property"></a>Proprietà IWMPNetwork::encodedFrameRate

La **proprietà encodedFrameRate** ottiene la frequenza dei fotogrammi video specificata dall'autore del contenuto.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32 che rappresenta** la frequenza dei fotogrammi codificata in fotogrammi al secondo (fps).

> [!Note]  
> Anche se **la proprietà encodedFrameRate** misura la frequenza dei fotogrammi codificati in fotogrammi al secondo, la **proprietà frameRate** misura la frequenza dei fotogrammi corrente in fotogrammi per cento secondi.

 

## <a name="examples"></a>Esempio

L'esempio di codice seguente **usa encodedFrameRate** per visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato. Le informazioni vengono visualizzate in un'etichetta, in risposta **all'evento PlayStateChange.** **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
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

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

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

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.frameRate (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





