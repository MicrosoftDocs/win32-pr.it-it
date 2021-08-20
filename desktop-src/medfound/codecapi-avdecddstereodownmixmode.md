---
description: Specifica la modalità downmix stereo per un decodificatore audio Dolby Digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: CODECAPI_AVDecDDStereoDownMixMode proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bba5cd5a75ecfbdbbd19ec7dbe063b06217322074559b8d24dae3073c244ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065059"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>PROPRIETÀ CODECAPI \_ AVDecDDStereoDownMixMode

Specifica la modalità downmix stereo per un decodificatore audio Dolby Digital.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVDecDDStereoDownMixMode.**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode)

## <a name="remarks"></a>Commenti

Questo attributo si applica quando l'input al decodificatore è audio PCM multicanale e l'output è audio stereo.

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

 

