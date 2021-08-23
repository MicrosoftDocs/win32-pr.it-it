---
description: Specifica se il codificatore produce gruppi aperti di immagini (GOP) o GOP chiusi. Questa proprietà si applica ai codificatori video MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Proprietà AVEncMPVGOPOpen (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6be085bde5588fecd5a2274d442f38d4198702475f3ed13c7bb3a5569687375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540901"
---
# <a name="avencmpvgopopen-property"></a>AVEncMPVGOPOpen - proprietà

Specifica se il codificatore produce gruppi aperti di immagini (GOP) o GOP chiusi. Questa proprietà si applica ai codificatori video MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Valore proprietà



| Valore          | Descrizione |
|----------------|-------------|
| VARIANT \_ FALSE | GOP chiusi |
| VARIANT \_ TRUE  | OPEN GOP   |



 

## <a name="remarks"></a>Commenti

Un GOP aperto contiene frame differenziali che fanno riferimento ai fotogrammi del GOP precedente. Un GOP chiuso non contiene frame differenziali che fanno riferimento al GOP precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server desktop apps UWP apps (App desktop UWP di Windows 2000 \[ \| Server)\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




