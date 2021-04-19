---
title: PLAYLIST. itemCount
description: L'attributo itemCount Recupera il numero di elementi attualmente visualizzati nell'elemento PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- PLAYLIST. itemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332539"
---
# <a name="playlistitemcount"></a>PLAYLIST. itemCount

L'attributo **ItemCount** Recupera il numero di elementi attualmente visualizzati nell'elemento **playlist** .

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Il numero totale di elementi espansi viene conteggiato dalla proprietà **ItemCount** . Se, ad esempio, sono presenti due playlist che contengono tre elementi multimediali, **ItemCount** restituirà 2 se le playlist non vengono espanse. Se viene espansa solo la prima playlist, **ItemCount** restituirà 4. Se entrambe le playlist sono espanse, **ItemCount** restituirà 6.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> </dl>

 

 





