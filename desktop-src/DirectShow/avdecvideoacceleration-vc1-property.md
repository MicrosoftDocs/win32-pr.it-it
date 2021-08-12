---
description: Abilita o disabilita l'accelerazione hardware per la decodifica video VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: AVDecVideoAcceleration_VC1 proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1767206fab479dbcae1dec5e768b21d768440a66776b1f41610b75be4190d6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663840"
---
# <a name="avdecvideoacceleration_vc1-property"></a>AVDecVideoAcceleration \_ VC1 - proprietà

Abilita o disabilita l'accelerazione hardware per la decodifica video VC-1.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Commenti

Se il valore è zero, il decodificatore non usa DirectX Video Acceleration (DXVA) per la decodifica video VC-1. Per DirectShow filtri, impostare questa proprietà prima che il pin di output del decodificatore sia connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 app \[ desktop per le app desktop \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




