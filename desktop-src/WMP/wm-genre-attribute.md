---
title: Attributo WM/Genre
description: L'attributo WM/Genre è il genere del contenuto.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Attributo WM/Genre Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0ef67b0b41ff59f644b0d52376428ae7a2330d388aa62f9765cb4842eeb561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000981"
---
# <a name="wmgenre-attribute"></a>Attributo WM/Genre

**L'attributo WM/Genre** è il genere del contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei file multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media.getItemInfoByType,** non il **metodo Media.getItemInfo.**

**Genre** è un alias per questo attributo.

La Windows media format SDK costante per questo attributo è \_ g wszWMGenre.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





