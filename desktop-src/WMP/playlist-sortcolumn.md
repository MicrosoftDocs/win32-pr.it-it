---
title: PLAYLIST.sortColumn
description: Il metodo sortColumn ordina i dati nella colonna specificata.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST.sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34dfce7306ceb39d64665538a21dbaef965ea799141a2756c2fea5bbe23ea9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335659"
---
# <a name="playlistsortcolumn"></a>PLAYLIST.sortColumn

Il **metodo sortColumn** ordina i dati nella colonna specificata.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Colonna*
</dt> <dd>

**Numero** (**long**) che indica l'indice della colonna da ordinare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo ordina la colonna specificata nello stesso modo dei pulsanti dell'intestazione di colonna **nell'elemento PLAYLIST.** Se la colonna non è ancora stata ordinata, viene ordinata in ordine alfanumerico. Se è stato ordinato, l'ordine viene invertito.

Per il funzionamento di questo metodo, **l'attributo allowColumnSorting** deve essere impostato su true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





