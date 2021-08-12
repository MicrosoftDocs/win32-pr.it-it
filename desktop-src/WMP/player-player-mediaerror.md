---
title: Evento Player.MediaError
description: L'evento MediaError si verifica quando l'oggetto Media presenta una condizione di errore.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Evento MediaError Windows Media Player
- Classe di evento MediaError Windows Media Player , Player
- Classe Player Windows Media Player, evento MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1eb94d245f0b0a91786b2b1a7b677429cc9040d8cbb1372164bf6e7ed209d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572841"
---
# <a name="playermediaerror-event"></a>Evento Player.MediaError

**L'evento MediaError** si verifica quando **l'oggetto Media** presenta una condizione di errore.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaObject* 
</dt> <dd>

**Oggetto** multimediale con una condizione di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





