---
title: AxWindowsMediaPlayer.status - proprietà
description: La proprietà status ottiene un valore che indica lo stato di Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Proprietà status Windows Media Player
- proprietà status Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac46eeef411e1d728994d829d95727cdaf4020c2ef1b7511391b6ca0d2e31ff7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864561"
---
# <a name="axwindowsmediaplayerstatus-property"></a>AxWindowsMediaPlayer.status - proprietà

La proprietà status ottiene un valore che indica lo stato di Windows Media Player.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Valore proprietà

System.String che rappresenta lo stato.

## <a name="remarks"></a>Commenti

I valori contenuti in questa proprietà sono soggetti a modifiche in qualsiasi momento e devono essere usati solo a scopo di visualizzazione.

The AxWindowsMediaPlayer. **L'evento StatusChange** viene generato ogni volta che questa proprietà cambia valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.StatusChange (VB e C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





