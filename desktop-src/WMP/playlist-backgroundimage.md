---
title: PLAYLIST. backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST. backgroundImage Media Player Windows
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329599"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST. backgroundImage

L'attributo **BackgroundImage** specifica o recupera l'immagine di sfondo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Se l'altezza e la larghezza dell'immagine sono inferiori all'altezza e alla larghezza dell'elemento della **playlist** , viene affiancata l'immagine. I formati supportati sono BMP, JPG, GIF e PNG.

Se si specifica il valore "gradiente" per l'immagine di sfondo, lo sfondo della playlist viene visualizzato come sfumatura di colore. Ciò significa che il colore di sfondo passa gradualmente tra i valori [playlist. BackgroundColor](playlist-backgroundcolor.md) (nella parte superiore dello sfondo) e [playlist. statusColor](playlist-statuscolor.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva, Windows Media Player 10 per la funzionalità gradiente<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> </dl>

 

 





