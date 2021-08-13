---
description: Imposta la soglia alla quale il codificatore considera ridondante un campo video.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Proprietà AVEncVideoInverseTelecineThreshold (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297dae601c5112714272a2d1c2e0b1a7ebeee5faa3aa2fabebc32e79c1745c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275180"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>AVEncVideoInverseTelecineThreshold - proprietà

Imposta la soglia alla quale il codificatore considera ridondante un campo video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà ha l'intervallo seguente.



| Valore | Descrizione                                                    |
|-------|----------------------------------------------------------------|
| 0     | È meno probabile che il codificatore consideri ridondanti i campi video. |
| 100   | È più probabile che il codificatore consideri ridondanti i campi video. |



 

## <a name="remarks"></a>Commenti

Impostare questa proprietà se il codificatore sta eseguendo telecine inverso con un'origine video analoga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 app \[ desktop per app desktop \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




