---
title: Proprietà sourceProtocol di IWMPNetwork
description: La proprietà sourceProtocol ottiene il protocollo di origine usato per ricevere i dati.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- Proprietà sourceProtocol Windows Media Player
- Proprietà sourceProtocol Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player proprietà , sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737bc0a5a4417735c795fc1058a7b821ee52489cf838be9eb934546f0fabacc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760851"
---
# <a name="iwmpnetworksourceprotocol-property"></a>Proprietà IWMPNetwork::sourceProtocol

La **proprietà sourceProtocol** ottiene il protocollo di origine usato per ricevere i dati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a>Valore proprietà

**System.String** che rappresenta il nome del protocollo di origine.

## <a name="remarks"></a>Commenti

Questa proprietà ottiene una stringa di lunghezza zero ("") durante la riproduzione di un CD o DVD.

## <a name="examples"></a>Esempio

L'esempio di codice seguente **usa sourceProtocol** per visualizzare il protocollo di origine usato per ricevere i dati. Le informazioni vengono visualizzate in un'etichetta, in risposta **all'evento PlayStateChange.** **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

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
</dt> </dl>

 

 





