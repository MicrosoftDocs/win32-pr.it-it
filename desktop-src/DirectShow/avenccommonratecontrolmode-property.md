---
description: Specifica la modalità di controllo della frequenza.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Proprietà AVEncCommonRateControlMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa914f445fcbc535ec423b41306938890d64b747258cb0159add5e4fd43c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794671"
---
# <a name="avenccommonratecontrolmode-property"></a>AVEncCommonRateControlMode - proprietà

Specifica la modalità di controllo della frequenza.

Le applicazioni possono impostare questa proprietà per specificare la modalità di controllo della frequenza. I codificatori possono anche restituire questa proprietà come funzionalità.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVEncCommonRateControlMode.**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

[CODECAPI \_ AVEncVideoRalLayerCount,](/windows/desktop/medfound/codecapi-avencvideotemporallayercount) [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)e CODECAPI \_ AVEncCommonRateControlMode sono proprietà del codificatore statico. Una volta impostati, questi saranno effettive solo dopo che un tipo di supporto impostato viene chiamato sul pin di output della fotocamera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

