---
description: Abilita o disabilita l'accelerazione hardware per la decodifica video MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: AVDecVideoAcceleration_MPEG2 proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2aa5db2d738afc0097ee4e09e7562dd7a3ae30b6138b2a003d85c6058fb22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159954"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a>AVDecVideoAcceleration \_ - proprietà MPEG2

Abilita o disabilita l'accelerazione hardware per la decodifica video MPEG-2.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoAcceleration \_ MPEG2**

## <a name="remarks"></a>Commenti

Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video MPEG-2. Per DirectShow, impostare questa proprietà prima che il pin di output del decodificatore sia connesso.

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

 

 




