---
description: Imposta l'utilizzo del video per un codificatore video.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Proprietà CODECAPI_AVEncVideoUsage (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305482"
---
# <a name="codecapi_avencvideousage-property"></a>Proprietà AVEncVideoUsage di codecapi \_

Imposta l'utilizzo del video per un codificatore video.

## <a name="data-type"></a>Tipo di dati

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoUsage**

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

[CODEcapi \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODEcapit \_ AVEncVideoUsage e [codecapi \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sono proprietà del codificatore statiche. Una volta impostate, queste diverranno effettive solo dopo la chiamata di un tipo di supporto set sul pin di output della fotocamera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

