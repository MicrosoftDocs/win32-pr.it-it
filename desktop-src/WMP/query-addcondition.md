---
title: Metodo Query.addCondition
description: Il metodo addCondition aggiunge una condizione all'oggetto Query usando la logica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Metodo addCondition Windows Media Player
- Metodo addCondition Windows Media Player , classe Query
- Query class Windows Media Player , metodo addCondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a3eed0a7923b93861eabc30d115a7726046d0595b7c57625d9a9afaf9c7523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746590"
---
# <a name="queryaddcondition-method"></a>Metodo Query.addCondition

Il **metodo addCondition** aggiunge una condizione all'oggetto **Query** usando la logica AND.

## <a name="syntax"></a>Sintassi


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> <dt>

*operatore* \[ Pollici\]
</dt> <dd>

**Stringa contenente** l'operatore . Vedere Osservazioni per i valori supportati.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per le query composte che **usano Query non** viene eseguita la distinzione tra maiuscole e minuscole.

Un elenco di valori per il parametro *attribute* è disponibile nella sezione Informazioni di riferimento [sull'attributo alfabetico.](alphabetical-attribute-reference.md)

Le condizioni contenute in un **oggetto Query** sono organizzate in gruppi di condizioni. Più condizioni all'interno di un gruppo di condizioni vengono sempre concatenate usando la logica AND. I gruppi di condizioni vengono sempre concatenati tra loro usando la logica OR. Per avviare un nuovo gruppo di condizioni, chiamare **Query.beginNextGroup**.

Nella tabella seguente sono elencati i valori supportati per *l'operatore*.



| Operatore            | Si applica a     |
|---------------------|----------------|
| BeginsWith          | Stringhe        |
| Contiene            | Stringhe        |
| Uguale a              | Tutti i tipi      |
| GreaterThan         | Numeri, date |
| GreaterThanOrEquals | Numeri, date |
| LessThan            | Numeri, date |
| LessThanOrEquals    | Numeri, date |
| NotBeginsWith       | Stringhe        |
| NotContains         | Stringhe        |
| NotEquals           | Tutti i tipi      |



 

## <a name="examples"></a>Esempio

Nell'JScript seguente vengono utilizzati **Query.addCondition** e **Query.beginNextGroup** per eseguire una query di esempio.


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Oggetto Query**](query-object.md)
</dt> <dt>

[**Query.beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





