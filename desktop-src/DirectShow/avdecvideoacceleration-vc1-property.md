---
description: Abilita o Disabilita l'accelerazione hardware per la decodifica video VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Proprietà AVDecVideoAcceleration_VC1 (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304251"
---
# <a name="avdecvideoacceleration_vc1-property"></a>\_Proprietà VC1 di AVDecVideoAcceleration

Abilita o Disabilita l'accelerazione hardware per la decodifica video VC-1.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Commenti

Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video VC-1. Per i filtri DirectShow, impostare questa proprietà prima della connessione del PIN di output del decodificatore.

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

 

 




