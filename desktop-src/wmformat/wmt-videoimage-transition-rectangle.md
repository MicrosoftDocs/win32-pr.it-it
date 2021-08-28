---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl.h)
description: La transizione del rettangolo visualizza la nuova immagine in un rettangolo all'interno della cornice.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8721455c09a263d9c856358d2ca55bb818ac48e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467398"
---
# <a name="wmt_videoimage_transition_rectangle"></a>RETTANGOLO DI \_ TRANSIZIONE DI WMT \_ \_ VIDEOIMAGE

La transizione del rettangolo visualizza la nuova immagine in un rettangolo all'interno della cornice.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Centra X | <strong>fEffectPara0</strong> | Coordinata X, relativa al fotogramma video, del centro del rettangolo. | 
| Centra Y | <strong>fEffectPara1</strong> | Coordinata Y, relativa al fotogramma video, del centro del rettangolo. | 
| Larghezza | <strong>fEffectPara2</strong> | Larghezza del rettangolo in pixel. | 
| Altezza | <strong>fEffectPara3</strong> | Altezza del rettangolo in pixel. | 
| Composizione | <strong>fEffectPara4</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





