---
title: Metodo MediaCollection.getStringCollectionByQuery
description: Il metodo getStringCollectionByQuery recupera un oggetto StringCollection contenente tutte le stringhe che soddisfano le condizioni di query.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Metodo getStringCollectionByQuery Windows Media Player
- Metodo getStringCollectionByQuery Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getStringCollectionByQuery
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
ms.openlocfilehash: 6d9e8f2eae2ce52a566d4db6b8298187df1d4d444432e99dda22d3cacc0ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390111"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>Metodo MediaCollection.getStringCollectionByQuery

Il **metodo getStringCollectionByQuery** recupera un **oggetto StringCollection** contenente tutte le stringhe che soddisfano le condizioni di query.

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

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa contenente** il nome dell'attributo.

</dd> <dt>

*query* \[ Pollici\]
</dt> <dd>

**Oggetto query.**

</dd> <dt>

*mediaType* \[ Pollici\]
</dt> <dd>

**Stringa contenente** il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "photo", "playlist" o "other".

</dd> <dt>

*sortAttribute* \[ Pollici\]
</dt> <dd>

**Stringa contenente** il nome dell'attributo utilizzato per l'ordinamento. Una stringa vuota ("") indica che non viene applicato alcun ordinamento.

</dd> <dt>

*sortAscending* \[ Pollici\]
</dt> <dd>

**Valore** booleano, true che indica che **StringCollection** deve essere ordinato in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto StringCollection.**

## <a name="remarks"></a>Commenti

Le query composte che usano **Query non** supportano la distinzione tra maiuscole e minuscole.

Quando la query composta specificata dal parametro *di query* contiene una condizione compilata in base all'attributo **MediaType,** tale condizione viene ignorata. Il valore per il *parametro mediaType* viene sempre usato. Ad esempio, se la query composta contiene la condizione "MediaType Equals audio" e il valore per *il parametro mediaType* è "video", la playlist risultante conterrà solo elementi video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Attributo MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Oggetto Query**](query-object.md)
</dt> </dl>

 

 





