---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl.h)
description: La transizione della ruota rivela la nuova immagine ruotando quattro linee intorno a un punto di perno comune, ad esempio gli spoke di una ruota.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b77e8640f21bd06194b2fe6b1e7048d85b323e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469268"
---
# <a name="wmt_videoimage_transition_wheel"></a>ROTELLINA DI \_ TRANSIZIONE DI WMT \_ \_ VIDEOIMAGE

La transizione della ruota rivela la nuova immagine ruotando quattro linee intorno a un punto di perno comune, ad esempio gli spoke di una ruota.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Centra X | <strong>fEffectPara0</strong> | Coordinata X, relativa al fotogramma video, del centro dell'effetto rotellina. | 
| Centra Y | <strong>fEffectPara1</strong> | Coordinata Y, relativa al fotogramma video, del centro dell'effetto rotellina. | 
| Angle | <strong>fEffectPara2</strong> | Angolo di rotazione, in gradi, degli spoke dell'effetto rotellina. Il valore 0,0 indica l'immagine precedente senza rivelare alcuna nuova immagine. Il valore 90,0 indica che la nuova immagine è stata rivelata completamente. Lo spostamento da 0,0 a 90,0 viene visualizzato come rotazione in senso orario degli spoke.<br /> | 
| Composizione | <strong>fEffectPara3</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





