---
description: Specifica gli angoli sinistro e superiore del rettangolo di ridimensionamento, se il video è ritagliato.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Proprietà AVEncVideoEncodeOffsetOrigin (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124227"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>Proprietà AVEncVideoEncodeOffsetOrigin

Specifica gli angoli sinistro e superiore del rettangolo di ridimensionamento, se il video è ritagliato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Valore proprietà

I 16 bit superiori del valore contengono l'offset dal bordo sinistro del frame di input, espresso in pixel. I 16 bit inferiori contengono l'offset dal bordo superiore del fotogramma di input, espresso in pixel.

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per ritagliare il video di input. Utilizzare la proprietà [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) per specificare la larghezza e l'altezza del rettangolo di ridimensionamento.

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

 

 




