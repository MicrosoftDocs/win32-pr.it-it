---
description: Regola le caratteristiche dei colori di un flusso video.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Trasformazione controllo colori DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749346"
---
# <a name="color-control-transform-dsp"></a>Trasformazione controllo colori DSP

Regola le caratteristiche dei colori di un flusso video.

## <a name="clsid"></a>CLSID

\_CCOLORCONTROLDMO CLSID

## <a name="interfaces"></a>Interfacce

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

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

-   [\_luminosità colore \_ MFPKEY](mfpkey-color-brightness.md)
-   [\_contrasto colori \_ MFPKEY](mfpkey-color-contrast.md)
-   [\_tonalità colore \_ MFPKEY](mfpkey-color-hue.md)
-   [\_ \_ saturazione colore MFPKEY](mfpkey-color-saturation.md)

## <a name="remarks"></a>Commenti

Questo DSP modifica il contenuto del flusso video. Per la riproduzione, è possibile ottenere effetti simili in modo più efficiente usando l'interfaccia **IMFVideoProcessor** , che controlla l'elaborazione video nella scheda grafica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




