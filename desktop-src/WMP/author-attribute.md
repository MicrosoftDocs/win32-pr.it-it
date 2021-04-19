---
title: Author (attributo)
description: L'attributo Author è il nome di un artista multimediale o di un attore associato al contenuto.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Attributo autore Media Player Windows
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329949"
---
# <a name="author-attribute"></a>Author (attributo)

L'attributo **Author** è il nome di un artista multimediale o di un attore associato al contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [File di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Media. getItemInfoByType](media-getiteminfobytype.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il *supporto*. il metodo **getItemInfoByType** , non il *supporto*. metodo **GetItemInfo** .

La costante Windows Media Format SDK per questo attributo è g \_ wszWMAuthor.

**Actor** e **Artist** sono alias per questo attributo.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





