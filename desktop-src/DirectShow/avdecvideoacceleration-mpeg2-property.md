---
description: Abilita o Disabilita l'accelerazione hardware per la decodifica video MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: Proprietà AVDecVideoAcceleration_MPEG2 (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747250"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a>\_Proprietà MPEG2 AVDecVideoAcceleration

Abilita o Disabilita l'accelerazione hardware per la decodifica video MPEG-2.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoAcceleration \_ MPEG2**

## <a name="remarks"></a>Commenti

Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video MPEG-2. Per i filtri DirectShow, impostare questa proprietà prima della connessione del PIN di output del decodificatore.

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

 

 




