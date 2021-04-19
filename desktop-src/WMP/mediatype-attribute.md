---
title: Attributo MediaType
description: L'attributo MediaType è il tipo di contenuto dell'elemento.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Attributo MediaType Windows Media Player
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327150"
---
# <a name="mediatype-attribute"></a>Attributo MediaType

L'attributo **mediaType** è il tipo di contenuto dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nella libreria.

Questo attributo ha uno dei valori seguenti: "audio", "altro", "Photo", "playlist", "Radio" o "video". Utilizzare questo attributo con *mediacollection*. metodo **getByAttribute** per recuperare una playlist contenente tutti gli elementi di un determinato tipo.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Mediacollection. getByAttribute**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





