---
title: Evento Player. MediaCollectionMediaRemoved
description: L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale. | Evento Player. MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Media Player di Windows Event MediaCollectionMediaRemoved
- Windows Event MediaCollectionMediaRemoved Media Player, classe Player
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
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333243"
---
# <a name="playermediacollectionmediaremoved-event"></a>Evento Player. MediaCollectionMediaRemoved

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

Oggetto **multimediale** che è stato rimosso.

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

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





