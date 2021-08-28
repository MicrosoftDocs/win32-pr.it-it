---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl.h)
description: La transizione dell'iris rivela la nuova immagine lungo un asse x e un asse y. L'effetto visivo di questa transizione è che la nuova immagine viene visualizzata in una sezione incrociata che si ampliare fino a tutti i lati del frame.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919af0b15ef8a7437c9852df3ff12623553cdabf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472967"
---
# <a name="wmt_videoimage_transition_iris"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ IRIS

La transizione dell'iris rivela la nuova immagine lungo un asse x e un asse y. L'effetto visivo di questa transizione è che la nuova immagine viene visualizzata in una sezione incrociata che si ampliare fino a tutti i lati del frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Centra X | <strong>fEffectPara0</strong> | Coordinata X, relativa al fotogramma video, del centro dell'effetto iris. | 
| Centra Y | <strong>fEffectPara1</strong> | Coordinata Y, relativa al fotogramma video, del centro dell'effetto iris. | 
| Larghezza | <strong>fEffectPara2</strong> | Larghezza della linea verticale che rivela la nuova immagine, in pixel. | 
| Altezza | <strong>fEffectPara3</strong> | Altezza della linea orizzontale che rivela la nuova immagine, in pixel. | 
| Composizione | <strong>fEffectPara4</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





