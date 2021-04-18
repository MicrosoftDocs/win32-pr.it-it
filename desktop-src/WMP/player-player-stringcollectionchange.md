---
title: Evento Player. StringCollectionChange
description: L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe. | Evento Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Media Player di Windows Event StringCollectionChange
- Windows Event StringCollectionChange Media Player, classe Player
- Classe Player Windows Media Player, evento StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325232"
---
# <a name="playerstringcollectionchange-event"></a>Evento Player. StringCollectionChange

L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe.

## <a name="syntax"></a>Sintassi


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdispStringCollection* 
</dt> <dd>

Oggetto **StringCollection** modificato.

</dd> <dt>

*change* 
</dt> <dd>

Numero (Long) che indica il tipo di modifica apportata alla raccolta di stringhe. Include uno dei valori seguenti.



|        |                                    |
|--------|------------------------------------|
| Number | Descrizione                        |
| 0      | Sconosciuto. (Valore non valido)       |
| 1      | È stato inserito un elemento.              |
| 2      | Raccolta di stringhe modificata.     |
| 3      | Un elemento è stato eliminato.               |
| 4      | Raccolta di stringhe cancellata. |
| 5      | Inizio degli aggiornamenti in blocco.        |
| 6      | Gli aggiornamenti in blocco sono terminati.           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Numero (Long) che contiene l'indice dell'elemento della raccolta di stringhe modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**StringCollection (oggetto)**](stringcollection-object.md)
</dt> </dl>

 

 





