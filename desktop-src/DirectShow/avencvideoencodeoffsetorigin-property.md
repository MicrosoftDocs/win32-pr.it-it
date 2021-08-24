---
description: Specifica gli angoli sinistro e superiore del rettangolo di ritaglio, se il video è ritagliato.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Proprietà AVEncVideoEncodeOffsetOrigin (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdc4ffd1f168fa98ce71937b5ddc22d429c573481575432e94964fdfc5205b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275761"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>AVEncVideoEncodeOffsetOrigin - proprietà

Specifica gli angoli sinistro e superiore del rettangolo di ritaglio, se il video è ritagliato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Valore proprietà

I 16 bit superiori del valore contengono l'offset dal bordo sinistro del frame di input, in pixel. I 16 bit inferiori contengono l'offset dal bordo superiore del frame di input, in pixel.

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per ritagliare il video di input. Usare la [**proprietà AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) per specificare la larghezza e l'altezza del rettangolo di ritaglio.

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

 

 




