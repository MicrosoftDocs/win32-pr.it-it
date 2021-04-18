---
description: Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Proprietà AVEncVideoEncodeDimension (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303754"
---
# <a name="avencvideoencodedimension-property"></a>Proprietà AVEncVideoEncodeDimension

Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Valore proprietà

I 16 bit superiori del valore contengono la larghezza in pixel e i 16 bit inferiori contengono l'altezza in pixel.

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per ritagliare il video di input. La dimensione specificata deve essere minore della dimensione dei fotogrammi video di input. Utilizzare la proprietà [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) per specificare gli angoli sinistro e superiore del rettangolo di ritaglio.

I codificatori possono restituire questa proprietà come una funzionalità.

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

Per i codificatori della fotocamera UVC 1,5, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) non è supportato.

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

 

