---
description: Specifica se un decodificatore AAC usa equazioni di downmix stereo MPEG-2/MPEG-4 standard o se usa un downmix non standard.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Proprietà AVDecAACDownmixMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3fde61acdd5d29574f316e269d5b04a0a94649827777504fe31c33bbf79bd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641281"
---
# <a name="avdecaacdownmixmode-property"></a>AVDecAACDownmixMode - proprietà

Specifica se un decodificatore AAC usa equazioni di downmix stereo MPEG-2/MPEG-4 standard o se usa un downmix non standard.

Un esempio di downmix non standard è quello definito dal documento ARIB STD-B21 versione 4.4.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVDecAACDownmixMode.**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

