---
title: AxWindowsMediaPlayer. openPlayer, metodo
description: Il metodo openPlayer apre Windows Media Player usando l'URL specificato. | AxWindowsMediaPlayer. openPlayer, metodo
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Metodo openPlayer Windows Media Player
- Metodo openPlayer Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo openPlayer
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
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325873"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>AxWindowsMediaPlayer. openPlayer, metodo

Il metodo **openPlayer** apre Windows Media Player usando l'URL specificato.

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

**System. String** che rappresenta l'URL dell'elemento multimediale da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo avvia Media Player Windows con l'URL specificato impostato come elemento multimediale corrente. Se il lettore è stato chiuso in precedenza in modalità Skin, verrà aperto utilizzando l'ultima interfaccia selezionata dall'utente. In caso contrario, il lettore verrà aperto in modalità completa.

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

 

 





