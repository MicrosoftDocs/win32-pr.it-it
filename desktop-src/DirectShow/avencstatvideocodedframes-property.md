---
description: Restituisce il numero di fotogrammi video codificati.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Proprietà AVEncStatVideoCodedFrames (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124806"
---
# <a name="avencstatvideocodedframes-property"></a>Proprietà AVEncStatVideoCodedFrames

Restituisce il numero di fotogrammi video codificati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile al termine della codifica.

Il valore di questa proprietà è uguale alla proprietà [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) meno il numero di frame eliminati. Il codificatore potrebbe rilasciare frame per rimanere entro i vincoli di velocità in bit specificati. Potrebbe inoltre rilasciare frame alla fine del flusso (vedere la proprietà [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).

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

 

 




