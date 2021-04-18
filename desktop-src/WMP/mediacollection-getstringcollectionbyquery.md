---
title: Mediacollection. getStringCollectionByQuery, metodo
description: Il metodo getStringCollectionByQuery recupera un oggetto StringCollection che contiene tutte le stringhe che soddisfano le condizioni della query.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Metodo getStringCollectionByQuery Windows Media Player
- Metodo getStringCollectionByQuery Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327165"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>Mediacollection. getStringCollectionByQuery, metodo

Il metodo **getStringCollectionByQuery** recupera un oggetto **StringCollection** che contiene tutte le stringhe che soddisfano le condizioni della query.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> <dt>

*query* \[ di in\]
</dt> <dd>

Oggetto **query** .

</dd> <dt>

*mediaType* \[ in\]
</dt> <dd>

**Stringa** che contiene il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".

</dd> <dt>

*sortAttribute* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo utilizzato per l'ordinamento. Una stringa vuota ("") indica che non viene applicato alcun ordinamento.

</dd> <dt>

*SortAscending* \[ in\]
</dt> <dd>

**Booleano**, true che indica che l'oggetto **StringCollection** deve essere ordinato in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **StringCollection** .

## <a name="remarks"></a>Commenti

Le query composte con **query** non fanno distinzione tra maiuscole e minuscole

Quando la query composta specificata dal parametro di *query* contiene una condizione basata sull'attributo **mediaType** , tale condizione viene ignorata. Viene sempre usato il valore per il parametro *mediaType* . Se, ad esempio, la query composta contiene la condizione "MediaType Equals audio" e il valore per il parametro *mediaType* è "video", la playlist risultante conterrà solo elementi video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Attributo MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Oggetto query**](query-object.md)
</dt> </dl>

 

 





