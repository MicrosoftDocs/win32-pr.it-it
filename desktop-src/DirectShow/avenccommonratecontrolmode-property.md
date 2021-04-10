---
description: Specifica la modalità di controllo della frequenza.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Proprietà AVEncCommonRateControlMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225479"
---
# <a name="avenccommonratecontrolmode-property"></a>Proprietà AVEncCommonRateControlMode

Specifica la modalità di controllo della frequenza.

Le applicazioni possono impostare questa proprietà per specificare la modalità di controllo della frequenza. I codificatori possono inoltre restituire questa proprietà come funzionalità.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[CODEcapi \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [codecapit \_ AVENCVIDEOUSAGE](/windows/desktop/medfound/codecapi-avencvideousage)e codecapi \_ AVEncCommonRateControlMode sono proprietà del codificatore statiche. Una volta impostate, queste diverranno effettive solo dopo la chiamata di un tipo di supporto set sul pin di output della fotocamera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

