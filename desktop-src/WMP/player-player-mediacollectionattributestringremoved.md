---
title: Evento Player. MediaCollectionAttributeStringRemoved
description: L'evento MediaCollectionAttributeStringRemoved si verifica quando viene rimosso un valore di attributo dalla libreria. | Evento Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Media Player di Windows Event MediaCollectionAttributeStringRemoved
- Windows Event MediaCollectionAttributeStringRemoved Media Player, classe Player
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
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324219"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Evento Player. MediaCollectionAttributeStringRemoved

L'evento **MediaCollectionAttributeStringRemoved** si verifica quando viene rimosso un valore di attributo dalla libreria.

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

**Stringa** che specifica il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Stringa** che specifica il valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un elemento multimediale viene rimosso dalla libreria, i relativi metadati vengono rimossi dall'oggetto **mediacollection** e questo evento viene generato per ogni attributo rimosso.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





