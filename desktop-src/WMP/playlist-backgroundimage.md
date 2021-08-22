---
title: PLAYLIST.backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST.backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ddcb42f118a5a672b6678079825b6cb3d6aba5fbdc54953fb566e4222f583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054249"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST.backgroundImage

**L'attributo backgroundImage** specifica o recupera l'immagine di sfondo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Se l'altezza e la larghezza dell'immagine sono inferiori all'altezza e alla larghezza dell'elemento **PLAYLIST,** l'immagine viene affiancata. I formati supportati sono BMP, JPG, GIF e PNG.

Se si specifica il valore "gradient" per l'immagine di sfondo, lo sfondo della playlist viene visualizzato come sfumatura di colore. Ciò significa che il colore di sfondo passa gradualmente tra i valori [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (nella parte superiore dello sfondo) e [PLAYLIST.statusColor.](playlist-statuscolor.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva, Windows Media Player 10 per la funzionalità sfumatura<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





