---
title: Attributo WM/EncodingTime
description: L'attributo WM/EncodingTime è la data e l'ora in cui è stato codificato il contenuto.
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- Media Player Windows per gli attributi WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659a1ec5b192782370804745da3f232db6e439dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327019"
---
# <a name="wmencodingtime-attribute"></a>Attributo WM/EncodingTime

L'attributo **WM/EncodingTime** è la data e l'ora in cui è stato codificato il contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**CreationDate** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMEncodingTime.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





