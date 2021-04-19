---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: La transizione di dissolvenza a colori viene risolta dall'immagine in un frame di colore a tinta unita.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327263"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>\_ \_ dissolvenza WMT VIDEOIMAGE transizione \_ \_ a \_ colore

La transizione di dissolvenza a colori viene risolta dall'immagine in un frame di colore a tinta unita.

## <a name="parameters"></a>Parametri

Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.



| Parametro         | Membro della struttura | Descrizione                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Red               | **fEffectPara0** | Valore rosso del colore di sfondo. Impostare su un numero compreso tra 0 e 255.                                                                                                                                                     |
| Green             | **fEffectPara1** | Valore verde del colore di sfondo. Impostare su un numero compreso tra 0 e 255.                                                                                                                                                   |
| Blu              | **fEffectPara2** | Valore blu del colore di sfondo. Impostare su un numero compreso tra 0 e 255.                                                                                                                                                    |
| Spessore sfondo | **fEffectPara3** | Spessore del colore di sfondo. Questo parametro esprime la percentuale del colore di sfondo nella combinazione come decimale. Ad esempio, per fondere il colore di sfondo al 30%, impostando su 0,30 l'immagine 70% della combinazione. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





