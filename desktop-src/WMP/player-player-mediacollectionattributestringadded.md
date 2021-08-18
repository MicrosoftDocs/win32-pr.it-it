---
title: Evento Player.MediaCollectionAttributeStringAdded
description: L'evento MediaCollectionAttributeStringAdded si verifica quando un valore di attributo viene aggiunto alla libreria. | Evento Player.MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Evento MediaCollectionAttributeStringAdded Windows Media Player
- Evento MediaCollectionAttributeStringAdded Windows Media Player , classe Player
- Classe Player Windows Media Player, evento MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d01bd86cb3004cb3f481222f392ba47bd1c47373f55c37ee8f0e7ded57a3d268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995871"
---
# <a name="playermediacollectionattributestringadded-event"></a>Evento Player.MediaCollectionAttributeStringAdded

**L'evento MediaCollectionAttributeStringAdded** si verifica quando un valore di attributo viene aggiunto alla libreria.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Stringa** che specifica il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi](attribute-reference.md).

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Stringa** che specifica il valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un elemento multimediale viene aggiunto alla libreria, i relativi metadati vengono aggiunti **all'oggetto MediaCollection** e questo evento viene generato per ogni attributo aggiunto.

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

 

 





