---
title: Proprietà AxWindowsMediaPlayer. enableContextMenu
description: La proprietà enableContextMenu Ottiene o imposta un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Finestra delle proprietà di enableContextMenu Media Player
- Proprietà enableContextMenu Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà enableContextMenu
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324399"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>Proprietà AxWindowsMediaPlayer. enableContextMenu

La proprietà enableContextMenu Ottiene o imposta un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System. Boolean che indica se abilitare il menu di scelta rapida. Il valore predefinito è true.

## <a name="remarks"></a>Commenti

Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





