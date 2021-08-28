---
title: Metodo AxWindowsMediaPlayer.openPlayer
description: Il metodo openPlayer apre Windows Media Player usando l'URL specificato. | Metodo AxWindowsMediaPlayer.openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Metodo openPlayer Windows Media Player
- Metodo openPlayer Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , metodo openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a2ae5660969e78aeb165c5f9fd9420ea04c79a6aeec9a57c4627cd61d32ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764711"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Metodo AxWindowsMediaPlayer.openPlayer

Il **metodo openPlayer** apre Windows Media Player usando l'URL specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System.String che** rappresenta l'URL dell'elemento multimediale da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo avvia Windows Media Player con l'URL specificato impostato come elemento multimediale corrente. Se il lettore è stato chiuso in precedenza in modalità interfaccia, si aprirà usando l'ultima interfaccia scelta dall'utente. In caso contrario, il lettore viene aperto in modalità completa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





