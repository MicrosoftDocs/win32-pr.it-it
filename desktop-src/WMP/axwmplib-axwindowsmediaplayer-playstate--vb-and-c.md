---
title: Proprietà AxWindowsMediaPlayer. riproduzione
description: La proprietà riproduzione ottiene un valore di enumerazione che indica lo stato dell'operazione Windows Media Player.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Finestra delle proprietà di riproduzione Media Player
- Proprietà riproduzione Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà riproduzione
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332297"
---
# <a name="axwindowsmediaplayerplaystate-property"></a>Proprietà AxWindowsMediaPlayer. riproduzione

La proprietà riproduzione ottiene un valore di enumerazione che indica lo stato dell'operazione Windows Media Player.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a>Valore proprietà

Valore di enumerazione WMPLib. WMPPlayState.

## <a name="remarks"></a>Commenti

Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare. Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi. Non è necessario scrivere codice che si basa sull'ordine di stato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usata la proprietà riproduzione per visualizzare lo stato di riproduzione corrente del lettore in un'etichetta. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. PlayStateChange (VB e C#)**](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





