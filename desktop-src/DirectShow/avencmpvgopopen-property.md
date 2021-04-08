---
description: Specifica se il codificatore produce gruppi di immagini aperti (GOPs) o GOPs chiusi. Questa proprietà si applica ai codificatori video MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Proprietà AVEncMPVGOPOpen (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746927"
---
# <a name="avencmpvgopopen-property"></a>Proprietà AVEncMPVGOPOpen

Specifica se il codificatore produce gruppi di immagini aperti (GOPs) o GOPs chiusi. Questa proprietà si applica ai codificatori video MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Valore proprietà



| Valore          | Descrizione |
|----------------|-------------|
| VARIANTE \_ false | GOPs chiuso |
| VARIANT \_ true  | Apri GOPs   |



 

## <a name="remarks"></a>Commenti

Un GOP aperto contiene frame Delta che fanno riferimento a frame del GOP precedente. Un GOP chiuso non contiene frame Delta che fanno riferimento al GOP precedente.

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

 

 




