---
title: Evento Player.MediaCollectionMediaRemoved
description: L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale. | Evento Player.MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Evento MediaCollectionMediaRemoved Windows Media Player
- MediaCollectionMediaRemoved event Windows Media Player , Player class
- Classe Player Windows Media Player, evento MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009432040deace140dd3cf4d7d7da1246c0a38dbd9fc0da028832af137cefa83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572851"
---
# <a name="playermediacollectionmediaremoved-event"></a>Evento Player.MediaCollectionMediaRemoved

L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdispMedia* 
</dt> <dd>

**Oggetto** multimediale rimosso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento si verifica solo per la libreria locale.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





