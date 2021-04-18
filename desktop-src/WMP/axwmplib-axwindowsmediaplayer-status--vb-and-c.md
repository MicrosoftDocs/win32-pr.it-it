---
title: Proprietà AxWindowsMediaPlayer. status
description: La proprietà Status ottiene un valore che indica lo stato di Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Finestra Proprietà stato Media Player
- Proprietà di stato Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà Status
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
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328303"
---
# <a name="axwindowsmediaplayerstatus-property"></a>Proprietà AxWindowsMediaPlayer. status

La proprietà Status ottiene un valore che indica lo stato di Windows Media Player.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Valore proprietà

System. String che rappresenta lo stato.

## <a name="remarks"></a>Commenti

I valori contenuti in questa proprietà sono soggetti a modifiche in qualsiasi momento e devono essere utilizzati solo a scopo di visualizzazione.

AxWindowsMediaPlayer. L'evento **StatusChange** viene generato ogni volta che questa proprietà cambia valore.

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

[**Evento AxWindowsMediaPlayer. StatusChange (VB e C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





