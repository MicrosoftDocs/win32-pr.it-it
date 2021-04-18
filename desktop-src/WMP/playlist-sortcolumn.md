---
title: PLAYLIST. sortColumn
description: Il metodo sortColumn Ordina i dati nella colonna specificata.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST. sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333835"
---
# <a name="playlistsortcolumn"></a>PLAYLIST. sortColumn

Il metodo **SortColumn** Ordina i dati nella colonna specificata.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*colonna*
</dt> <dd>

**Numero** (**Long**) che indica l'indice della colonna da ordinare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo ordina la colonna specificata nello stesso modo dei pulsanti di intestazione di colonna nell'elemento **playlist** . Se la colonna non è ancora stata ordinata, viene ordinata in ordine alfanumerico. Se è stato ordinato, l'ordine viene invertito.

Per il corretto funzionamento di questo metodo, l'attributo **allowColumnSorting** deve essere impostato su true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





