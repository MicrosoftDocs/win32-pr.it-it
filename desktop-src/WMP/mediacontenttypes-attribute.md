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
ms.openlocfilehash: eca3c422083954554db76657a0bb9cc10062fd878a9ebf4b31f4dc88734ac1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996241"
---
# <a name="mediacontenttypes-attribute"></a>Attributo MediaContentTypes

**L'attributo MediaContentTypes** specifica il tipo di contenuto nell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Playlist](playlist-attributes-ref.md)

## <a name="remarks"></a>Commenti

Questo attributo può essere uno dei valori seguenti:



| Valore | Significato                                |
|-------|----------------------------------------|
| 1     | La playlist contiene contenuto audio.   |
| 2     | Oggetto da ottenere.                        |
| 3     | La playlist contiene contenuto audio.   |
| 4     | La playlist contiene contenuto video.   |
| 5     | La playlist contiene il contenuto dell'immagine. |
| 6     | La playlist contiene contenuto TV.      |



 

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





