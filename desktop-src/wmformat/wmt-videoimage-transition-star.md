---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl.h)
description: La transizione a stella rivela la nuova immagine in una stella a cinque punte all'interno del frame.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7524e51908f7d941aa04b138cc67ba6c4ab6a2a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479497"
---
# <a name="wmt_videoimage_transition_star"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ STAR

La transizione a stella rivela la nuova immagine in una stella a cinque punte all'interno del frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Centra X | <strong>fEffectPara0</strong> | Coordinata X, relativa al fotogramma video, del centro della stella. | 
| Centra Y | <strong>fEffectPara1</strong> | Coordinata Y, relativa al fotogramma video, del centro della stella. | 
| Radius | <strong>fEffectPara2</strong> | Raggio, in pixel, del cerchio definito dai punti della stella. | 
| Composizione | <strong>fEffectPara3</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano.</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





