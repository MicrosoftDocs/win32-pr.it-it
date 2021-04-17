---
description: Specifica la modalità downmix stereo per un decodificatore Dolby Digital audio.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: Proprietà CODECAPI_AVDecDDStereoDownMixMode (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401550"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>Proprietà AVDecDDStereoDownMixMode di codecapi \_

Specifica la modalità downmix stereo per un decodificatore Dolby Digital audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) .

## <a name="remarks"></a>Commenti

Questo attributo si applica quando l'input per il decodificatore è un audio PCM multicanale e l'output è audio stereo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

