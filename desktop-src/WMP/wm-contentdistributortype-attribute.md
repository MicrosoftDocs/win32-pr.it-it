---
title: Attributo WM/ContentDistributorType
description: L'attributo WM/ContentDistributorType è il tipo del server di distribuzione dell'elemento.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Media Player Windows per gli attributi WM/ContentDistributorType
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327025"
---
# <a name="wmcontentdistributortype-attribute"></a>Attributo WM/ContentDistributorType

L'attributo **WM/ContentDistributorType** è il tipo del server di distribuzione dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Il valore di questo attributo verrà impostato su "list" o "Radio". Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**ContentDistributorType** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMContentDistributorType.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





