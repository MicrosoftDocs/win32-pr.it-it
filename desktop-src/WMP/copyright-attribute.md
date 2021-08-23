---
title: Attributo Copyright (Msfeeds.h)
description: L'attributo Copyright è il messaggio di copyright per l'elemento.
ms.assetid: 617272cb-883f-46d6-b0a9-29ac32c63148
keywords:
- Attributi di copyright Windows Media Player
topic_type:
- apiref
api_name:
- Copyright
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b42e68e0d3485824f502dea991048121e788dfbe574b8fa4921e93a3b7afb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651961"
---
# <a name="copyright-attribute"></a>Attributo copyright

**L'attributo Copyright** è il messaggio di copyright per l'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [File multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

La Windows media format SDK per questo attributo è g \_ wszWMCopyright.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                    |
| Intestazione<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





