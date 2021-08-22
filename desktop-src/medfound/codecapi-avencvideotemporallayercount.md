---
description: Imposta il numero di livelli temporali video per un codificatore video.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81ceaf82d9d202e97927e0e141aa03a4e8e27c49a28880509aa9bb3c24f9319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743847"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>PROPRIETÀ CODECAPI \_ AVEncVideoTemporalLayerCount

Imposta il numero di livelli temporali video per un codificatore video.

## <a name="data-type"></a>Tipo di dati

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)e [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sono proprietà del codificatore statico. Una volta impostati, questi saranno effettive solo dopo che un tipo di supporto impostato viene chiamato sul segnaposto di output della fotocamera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

