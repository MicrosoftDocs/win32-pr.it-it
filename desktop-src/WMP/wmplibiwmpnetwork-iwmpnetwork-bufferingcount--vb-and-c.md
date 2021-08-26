---
title: Proprietà IWMPNetwork bufferingCount
description: La proprietà bufferingCount ottiene il numero di volte in cui si è verificato il buffering durante la riproduzione.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- BufferingCount - proprietà Windows Media Player
- proprietà bufferingCount Windows Media Player , interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player , proprietà bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b69169e950cf3794d613bfd1d79d4953ce8f8a8bb01efe9ff17d6fa5961071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899971"
---
# <a name="iwmpnetworkbufferingcount-property"></a>Proprietà IWMPNetwork::bufferingCount

La **proprietà bufferingCount** ottiene il numero di volte in cui si è verificato il buffering durante la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta il numero di buffer.

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero. Non viene reimpostata se la riproduzione è sospesa.

La memorizzazione nel buffer si applica solo al contenuto di streaming. Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato tramite la **proprietà AxWindowsMediaPlayer.URL.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene *utilizzato bufferingCount* per visualizzare il numero di volte in cui si verifica la memorizzazione nel buffer durante la riproduzione. Le informazioni vengono visualizzate in un'etichetta in risposta all'evento di memorizzazione nel buffer. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

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

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





