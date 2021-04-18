---
description: Specifica se un decodificatore AAC USA equazioni downmix standard MPEG-2/MPEG-4 stereo oppure usa un downmix non standard.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Proprietà AVDecAACDownmixMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304208"
---
# <a name="avdecaacdownmixmode-property"></a>Proprietà AVDecAACDownmixMode

Specifica se un decodificatore AAC USA equazioni downmix standard MPEG-2/MPEG-4 stereo oppure usa un downmix non standard.

Un esempio di downmix non standard è quello definito dal documento ARIB STD-B21 versione 4,4.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .

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

 

