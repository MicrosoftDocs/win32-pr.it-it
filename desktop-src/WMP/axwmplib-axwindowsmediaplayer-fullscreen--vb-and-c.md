---
title: AxWindowsMediaPlayer.fullScreen - proprietà
description: La proprietà fullScreen ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Proprietà fullScreen Windows Media Player
- Proprietà fullScreen Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player proprietà , fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e128d8c7e0cf49d3feaae723a7fb5a51740cda47e5016df6290b4852c20ec27b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902621"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>AxWindowsMediaPlayer.fullScreen - proprietà

La proprietà fullScreen ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System.Boolean che indica se il contenuto viene riprodotto in modalità schermo intero. Il valore predefinito è false.

## <a name="remarks"></a>Commenti

Per il corretto funzionamento della modalità schermo intero durante l'incorporamento del controllo Windows Media Player, l'area di visualizzazione video deve avere un'altezza e una larghezza di almeno un pixel. Se **uiMode è** impostato su "mini" o "full", l'altezza del controllo stesso deve essere 65 o superiore per contenere l'area di visualizzazione video oltre all'interfaccia utente.

Se **uiMode** è impostato su "invisible", l'impostazione di questa proprietà su true genera un errore e non influisce sul comportamento del controllo.

Durante la riproduzione a schermo intero, Windows Media Player il cursore del mouse quando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) è uguale a false e **uiMode** è uguale a "none".

Se **uiMode è** impostato su "full" o "mini", Windows Media Player visualizza i controlli di trasporto in modalità schermo intero quando il cursore del mouse viene spostato. Dopo un breve intervallo di assenza di spostamento del mouse, i controlli di trasporto vengono nascosti. Se **uiMode** è impostato su "none", non viene visualizzato alcun controllo in modalità schermo intero.

> [!Note]  
> La visualizzazione dei controlli di trasporto in modalità schermo intero richiede Windows sistema operativo XP.

 

Se i controlli di trasporto non vengono visualizzati in modalità schermo intero, Windows Media Player automaticamente la modalità schermo intero all'arresto della riproduzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante che usa la proprietà fullScreen per passare un oggetto lettore incorporato alla modalità schermo intero. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                  |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                            |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.uiMode (VB e C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





