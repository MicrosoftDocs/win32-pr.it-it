---
title: Proprietà AxWindowsMediaPlayer. fullScreen
description: La proprietà fullScreen Ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Finestre delle proprietà a schermo intero Media Player
- Proprietà fullScreen Media Player Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, proprietà fullScreen
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
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324384"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>Proprietà AxWindowsMediaPlayer. fullScreen

La proprietà fullScreen Ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System. Boolean che indica se il contenuto viene riprodotto in modalità schermo intero. Il valore predefinito è false.

## <a name="remarks"></a>Commenti

Per il corretto funzionamento della modalità a schermo intero quando si incorpora il controllo Media Player di Windows, l'area di visualizzazione del video deve avere un'altezza e una larghezza pari ad almeno un pixel. Se **uiMode** è impostato su "mini" o "full", l'altezza del controllo deve essere 65 o superiore per ospitare l'area di visualizzazione video oltre all'interfaccia utente.

Se **uiMode** è impostato su "invisibile", l'impostazione di questa proprietà su true genera un errore e non influisce sul comportamento del controllo.

Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) è uguale a false e **uiMode** è uguale a "None".

Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero quando il cursore del mouse si sposta. Dopo un breve intervallo di assenza del movimento del mouse, i controlli di trasporto sono nascosti. Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.

> [!Note]  
> Per visualizzare i controlli di trasporto in modalità schermo intero, è necessario il sistema operativo Windows XP.

 

Se i controlli di trasporto non vengono visualizzati in modalità schermo intero, Windows Media Player esce automaticamente dalla modalità schermo intero quando la riproduzione viene arrestata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un pulsante che usa la proprietà fullScreen per passare un oggetto Player incorporato alla modalità schermo intero. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                  |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                            |
| Assembly<br/>  | <dl> <dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. uiMode (VB e C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





