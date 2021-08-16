---
description: Restituisce il numero di fotogrammi video codificati.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Proprietà AVEncStatVideoCodedFrames (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f8858aba7a36d79096eccad40990e1859d4073695aaf80910587bac4005d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342562"
---
# <a name="avencstatvideocodedframes-property"></a>AVEncStatVideoCodedFrames - proprietà

Restituisce il numero di fotogrammi video codificati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile dopo il completamento della codifica.

Il valore di questa proprietà è uguale alla proprietà [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) meno il numero di fotogrammi eliminati. Il codificatore potrebbe eliminare i fotogrammi per rimanere entro i vincoli di velocità in bit specificati. Potrebbe anche eliminare i frame alla fine del flusso (vedere la [**proprietà AVEncCommonStreamEndHandling).**](avenccommonstreamendhandling-property.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop app \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




