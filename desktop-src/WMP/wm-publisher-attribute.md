---
title: Attributo WM/Publisher
description: L'attributo WM/Publisher è il nome della società che ha pubblicato il contenuto.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Windows Media Player attributo WM/Publisher
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00bd0d2ab2b6d886639cffa1df0770dfe329f7f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329712"
---
# <a name="wmpublisher-attribute"></a>Attributo WM/Publisher

L'attributo **WM/Publisher** è il nome della società che ha pubblicato il contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

**Label**, **ReleasedBy** e **Studio** sono alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMPublisher.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





