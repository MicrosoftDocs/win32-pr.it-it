---
title: PLAYLIST.itemPlaylist
description: L'attributo itemPlaylist recupera la playlist per l'elemento multimediale visualizzato in corrispondenza dell'indice specificato nell'elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- PLAYLIST.itemPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f2ed3173042d68ec048486189d909be60427df92e9936d4446f8d7a99ef592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571174"
---
# <a name="playlistitemplaylist"></a>PLAYLIST.itemPlaylist

**L'attributo itemPlaylist** recupera la playlist per l'elemento multimediale visualizzato in corrispondenza dell'indice specificato nell'elemento **PLAYLIST.**

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un oggetto **Playlist di sola** lettura.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero**(**long**) contenente l'indice di un elemento della playlist.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà itemPlaylist** restituirà l'oggetto playlist espanso nell'elemento **PLAYLIST.** Ad esempio, se sono presenti due playlist annidate che non vengono espanse nell'elemento **PLAYLIST** e che contengono tre clip multimediali ognuna, **itemPlaylist**(1) restituirà la playlist padre che contiene le due playlist annidate. Se la seconda playlist viene espansa, **itemPlaylist**(1) restituirà la seconda playlist. Se entrambe le playlist sono espanse, **itemPlaylist**(1) restituirà la prima playlist.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> </dl>

 

 





