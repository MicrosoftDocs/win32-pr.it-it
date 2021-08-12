---
title: Evento Player.StringCollectionChange
description: L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe. | Evento Player.StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Evento StringCollectionChange Windows Media Player
- Evento StringCollectionChange Windows Media Player , classe Player
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
ms.openlocfilehash: 5012cd94c14532eb94eb452c9c7aa20d50ffb8a447c2d14f56e8c6df02456849
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572419"
---
# <a name="playerstringcollectionchange-event"></a>Evento Player.StringCollectionChange

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

**Oggetto StringCollection** modificato.

</dd> <dt>

*change* 
</dt> <dd>

Numero (long) che indica il tipo di modifica apportata alla raccolta di stringhe. Include uno dei valori seguenti.



| Number | Descrizione                        |
|--------|------------------------------------|
| 0      | Sconosciuto. (Non è un valore valido)       |
| 1      | È stato inserito un elemento.              |
| 2      | La raccolta di stringhe è stata modificata.     |
| 3      | Un elemento è stato eliminato.               |
| 4      | La raccolta di stringhe è stata cancellata. |
| 5      | Sono in corso gli aggiornamenti in blocco.        |
| 6      | Gli aggiornamenti in blocco sono terminati.           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Numero (long) contenente l'indice dell'elemento della raccolta di stringhe modificato.

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

[**Oggetto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





