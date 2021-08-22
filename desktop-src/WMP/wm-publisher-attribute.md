---
title: Attributo WM/Publisher
description: L'attributo WM/Publisher è il nome della società che ha pubblicato il contenuto.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Attributi WM/Publisher Windows Media Player
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22aa04eecb3999b3029948739eef51dab094d0ebf9b65ba01ccdcf6de59efc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053789"
---
# <a name="wmpublisher-attribute"></a>Attributo WM/Publisher

**L'attributo WM/Publisher** è il nome della società che ha pubblicato il contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

**Label**, **ReleasedBy** e **Studio** sono alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMPublisher.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





