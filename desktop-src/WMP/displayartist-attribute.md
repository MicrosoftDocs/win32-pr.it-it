---
title: Attributo DisplayArtist
description: L'attributo DisplayArtist è il nome dell'artista visualizzato per un elemento.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Attributo DisplayArtist Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327624"
---
# <a name="displayartist-attribute"></a>Attributo DisplayArtist

L'attributo **DisplayArtist** è il nome dell'artista visualizzato per un elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)

## <a name="remarks"></a>Commenti

In genere, **DisplayArtist** avrà lo stesso valore dell'attributo **WM/AlbumArtist** quando viene impostato l'attributo. In caso contrario, il valore sarà il nome dell'artista associato alla prima traccia sull'album.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Attributo WM/AlbumArtist**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





