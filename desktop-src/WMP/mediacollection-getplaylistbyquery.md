---
title: Mediacollection. getPlaylistByQuery, metodo
description: Il metodo getPlaylistByQuery recupera un oggetto playlist contenente oggetti multimediali che corrispondono alle condizioni della query.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- Metodo getPlaylistByQuery Windows Media Player
- Metodo getPlaylistByQuery Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327166"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Mediacollection. getPlaylistByQuery, metodo

Il metodo **getPlaylistByQuery** recupera un oggetto **playlist** contenente oggetti **multimediali** che corrispondono alle condizioni della query.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*query* \[ di in\]
</dt> <dd>

Oggetto **query** che definisce le condizioni utilizzate per creare la playlist.

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

**Booleano**, true che indica che la playlist deve essere ordinata in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist** .

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

 

 





