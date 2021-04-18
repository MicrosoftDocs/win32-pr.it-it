---
title: Attributo WM/genre
description: L'attributo WM/genre è il genere del contenuto.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Windows Media Player attributo WM/genre
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327017"
---
# <a name="wmgenre-attribute"></a>Attributo WM/genre

L'attributo **WM/genre** è il genere del contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .

**Genre** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMGenre.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





