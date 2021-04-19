---
title: Attributo MediaContentTypes
description: L'attributo MediaContentTypes specifica il tipo di contenuto nell'elemento.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Attributo MediaContentTypes Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327153"
---
# <a name="mediacontenttypes-attribute"></a>Attributo MediaContentTypes

L'attributo **MediaContentTypes** specifica il tipo di contenuto nell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Playlist](playlist-attributes-ref.md)

## <a name="remarks"></a>Commenti

Questo attributo può essere uno dei valori seguenti:



| Valore | Significato                                |
|-------|----------------------------------------|
| 1     | La playlist contiene contenuto audio.   |
| 2     | Da fornire.                        |
| 3     | La playlist contiene contenuto audio.   |
| 4     | La playlist contiene contenuto video.   |
| 5     | La playlist contiene contenuto immagine. |
| 6     | La playlist contiene contenuto TV.      |



 

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





