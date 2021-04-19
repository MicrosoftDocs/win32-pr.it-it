---
title: PLAYLIST. itemPlaylist
description: L'attributo itemPlaylist recupera la playlist per l'elemento multimediale visualizzato in corrispondenza dell'indice specificato nell'elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- PLAYLIST. itemPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332530"
---
# <a name="playlistitemplaylist"></a>PLAYLIST. itemPlaylist

L'attributo **itemPlaylist** recupera la playlist per l'elemento multimediale visualizzato in corrispondenza dell'indice specificato nell'elemento **playlist** .

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un oggetto **playlist** di sola lettura.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero**(**Long**) che contiene l'indice di un elemento della playlist.

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **itemPlaylist** restituirà l'oggetto playlist espanso nell'elemento **playlist** . Se ad esempio sono presenti due Playlist nidificate che non sono espanse nell'elemento **playlist** e che contengono tre clip multimediali ciascuna, **itemPlaylist**(1) restituirà la playlist padre che contiene le due Playlist nidificate. Se la seconda playlist è espansa, **itemPlaylist**(1) restituirà la seconda playlist. Se entrambe le playlist sono espanse, **itemPlaylist**(1) restituirà la prima playlist.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> </dl>

 

 





