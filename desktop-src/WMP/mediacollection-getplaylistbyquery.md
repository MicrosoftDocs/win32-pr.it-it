---
title: Metodo MediaCollection.getPlaylistByQuery
description: Il metodo getPlaylistByQuery recupera un oggetto Playlist contenente oggetti Media che soddisfano le condizioni di query.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- Metodo getPlaylistByQuery Windows Media Player
- Metodo getPlaylistByQuery Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getPlaylistByQuery
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
ms.openlocfilehash: 47f64f054fe59865fb8d213d343696c86d83a5f8698d498c854660f76dc9085f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837144"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Metodo MediaCollection.getPlaylistByQuery

Il **metodo getPlaylistByQuery** recupera un oggetto **Playlist** contenente **oggetti Media** che soddisfano le condizioni di query.

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

*query* \[ Pollici\]
</dt> <dd>

**Oggetto query** che definisce le condizioni usate per creare la playlist.

</dd> <dt>

*mediaType* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il tipo di supporto. Deve contenere uno dei valori seguenti: "audio", "video", "photo", "playlist" o "other".

</dd> <dt>

*sortAttribute* \[ Pollici\]
</dt> <dd>

**Stringa contenente** il nome dell'attributo utilizzato per l'ordinamento. Una stringa vuota ("") indica che non viene applicato alcun ordinamento.

</dd> <dt>

*sortAscending* \[ Pollici\]
</dt> <dd>

**Valore** booleano, true che indica che la playlist deve essere ordinata in ordine crescente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Per le query composte che **usano Query non** viene eseguita la distinzione tra maiuscole e minuscole.

Quando la query composta specificata dal parametro *di query* contiene una condizione compilata sull'attributo **MediaType,** tale condizione viene ignorata. Viene sempre usato il valore per il parametro *mediaType.* Ad esempio, se la query composta contiene la condizione "MediaType Equals audio" e il valore per il *parametro mediaType* è "video", la playlist risultante conterrà solo elementi video.

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

 

 





