---
title: Metodo query. addCondition
description: Il metodo addCondition aggiunge una condizione all'oggetto query usando la logica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Metodo addCondition Windows Media Player
- Metodo addCondition Media Player Windows, classe query
- Classe di query Windows Media Player, metodo addCondition
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
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325984"
---
# <a name="queryaddcondition-method"></a>Metodo query. addCondition

Il metodo **addCondition** aggiunge una condizione all'oggetto **query** usando la logica and.

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

*attributo* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> <dt>

*operatore* \[ di in\]
</dt> <dd>

**Stringa** contenente l'operatore. Vedere la sezione Osservazioni per i valori supportati.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

**Stringa** contenente il valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le query composte con **query** non fanno distinzione tra maiuscole e minuscole

Un elenco di valori per il parametro *attribute* è reperibile nella sezione [riferimento all'attributo alfabetico](alphabetical-attribute-reference.md) .

Le condizioni contenute in un oggetto **query** sono organizzate in gruppi di condizioni. Più condizioni all'interno di un gruppo di condizioni sono sempre concatenate usando e la logica. I gruppi di condizioni sono sempre concatenati l'uno all'altro usando la logica o. Per avviare un nuovo gruppo di condizioni, chiamare **query. beginNextGroup**.

Nella tabella seguente sono elencati i valori supportati per *operator*.



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

Nell'esempio JScript seguente vengono utilizzati **query. addCondition** e **query. beginNextGroup** per eseguire una query di esempio.


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

[**Mediacollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**Mediacollection. getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Mediacollection. getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Oggetto query**](query-object.md)
</dt> <dt>

[**Query. beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





