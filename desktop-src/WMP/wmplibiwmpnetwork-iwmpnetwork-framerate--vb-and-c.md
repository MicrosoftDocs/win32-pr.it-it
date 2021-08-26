---
title: Proprietà IWMPNetwork frameRate
description: La proprietà frameRate ottiene la frequenza fotogrammi video corrente.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- proprietà frameRate Windows Media Player
- proprietà frameRate Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player , proprietà frameRate
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
ms.openlocfilehash: 3169cc21eee2317da45db3cb3ca9ceffffa01c85479312defe63cda1fa09796f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956161"
---
# <a name="iwmpnetworkframerate-property"></a>Proprietà IWMPNetwork::frameRate

La **proprietà frameRate** ottiene la frequenza fotogrammi video corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta la frequenza fotogrammi corrente in fotogrammi al centesimo di secondo.

> [!Note]  
> Anche se la **proprietà encodedFrameRate** misura la frequenza dei fotogrammi codificati in fotogrammi al secondo, la **proprietà frameRate** misura la frequenza dei fotogrammi corrente in fotogrammi al secondo. Vedere la sezione Osservazioni.

 

## <a name="remarks"></a>Commenti

Il valore corrente della frequenza dei fotogrammi viene restituito in fotogrammi per cento secondi. Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo (fps).

## <a name="examples"></a>Esempio

L'esempio di codice seguente usa **frameRate** per visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato. Le informazioni vengono visualizzate in un'etichetta in risposta **all'evento PlayStateChange.** **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.encodedFrameRate (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





