---
description: Abilita o Disabilita l'accelerazione hardware per la decodifica video H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Proprietà AVDecVideoAcceleration_H264 (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876909"
---
# <a name="avdecvideoacceleration_h264-property"></a>\_Proprietà H264 AVDecVideoAcceleration

Abilita o Disabilita l'accelerazione hardware per la decodifica video H. 264.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>Commenti

Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video H. 264. Per i filtri DirectShow, impostare questa proprietà prima della connessione del PIN di output del decodificatore.

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

 

 




