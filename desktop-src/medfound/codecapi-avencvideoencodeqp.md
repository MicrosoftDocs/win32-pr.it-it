---
description: Specifica il parametro di quantizzazione (QP) per la codifica video.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ed7ba8e3cf522c1e3cfa07d22cf5e37639717c230ca571ffd89d9e1d513a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974890"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>CODECAPI \_ AVEncVideoEncodeQP - proprietà

Specifica il parametro di quantizzazione (QP) per la codifica video.

## <a name="data-type"></a>Tipo di dati

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valore proprietà

Set di quattro campi a 16 bit usati per specificare i QP dei frame nella codifica QP fissa.

I campi sono:

-   Bit 0-15: QP predefinito
-   Bit 16-31: QP usato per i fotogrammi I
-   Bit 32-47: QP usato per i fotogrammi P
-   Bit 48-63: QP usato per i fotogrammi B

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

Per assicurare un utilizzo coerente tra codificatori diversi, è consigliabile presupporre che i codificatori animino solo il QP predefinito e possano ignorare i valori QP per le immagini I/P/B.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

