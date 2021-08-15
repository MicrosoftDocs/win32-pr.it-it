---
title: Evento Player.MediaCollectionAttributeStringRemoved
description: L'evento MediaCollectionAttributeStringRemoved si verifica quando un valore di attributo viene rimosso dalla libreria. | Evento Player.MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Evento MediaCollectionAttributeStringRemoved Windows Media Player
- Classe di evento MediaCollectionAttributeStringRemoved Windows Media Player , Player
- Classe Player Windows Media Player, evento MediaCollectionAttributeStringRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b89e46d4dbe86f185fb636b5c8de453e2addbf83c92d1231b5f067ce0b3b1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747407"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Evento Player.MediaCollectionAttributeStringRemoved

**L'evento MediaCollectionAttributeStringRemoved** si verifica quando un valore di attributo viene rimosso dalla libreria.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Stringa** che specifica il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di riferimento Windows Media Player [attributi.](attribute-reference.md)

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Stringa** che specifica il valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un elemento multimediale viene rimosso dalla libreria, i relativi metadati vengono rimossi **dall'oggetto MediaCollection** e questo evento viene generato per ogni attributo rimosso.

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





