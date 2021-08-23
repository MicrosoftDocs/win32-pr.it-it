---
description: Regola le caratteristiche di colore di un flusso video.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: DSP trasformazione controllo colore (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606211"
---
# <a name="color-control-transform-dsp"></a>DSP trasformazione controllo colore

Regola le caratteristiche di colore di un flusso video.

## <a name="clsid"></a>CLSID

CLSID \_ CColorControlDmo

## <a name="interfaces"></a>Interfacce

-   **Oggetto IMediaObject**
-   **IMFTransform**
-   **Ipropertystore**

## <a name="formats"></a>Formati

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>Proprietà

-   [LUMINOSITÀ DEL COLORE MFPKEY \_ \_](mfpkey-color-brightness.md)
-   [CONTRASTO DEI COLORI MFPKEY \_ \_](mfpkey-color-contrast.md)
-   [MFPKEY \_ COLOR \_ HUE](mfpkey-color-hue.md)
-   [SATURAZIONE DEL COLORE MFPKEY \_ \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Commenti

Questo DSP modifica il contenuto del flusso video. Per la riproduzione, è possibile ottenere effetti simili in modo più efficiente usando **l'interfaccia IMFVideoProcessor,** che controlla l'elaborazione video nella scheda grafica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




