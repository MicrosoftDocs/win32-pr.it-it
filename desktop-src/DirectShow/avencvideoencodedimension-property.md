---
description: Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Proprietà AVEncVideoEncodeDimension (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d99a0c14cbb3f67f7aa1c634a59c5f4cb9184dcd861bc8f14023c4afcebcefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159320"
---
# <a name="avencvideoencodedimension-property"></a>AVEncVideoEncodeDimension - proprietà

Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Valore proprietà

I 16 bit superiori del valore contengono la larghezza in pixel e i 16 bit inferiori contengono l'altezza in pixel.

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per ritagliare il video di input. Le dimensioni specificate devono essere inferiori a quelle dei fotogrammi video di input. Usare la [**proprietà AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) per specificare gli angoli sinistro e superiore del rettangolo di ritaglio.

I codificatori possono restituire questa proprietà come funzionalità.

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

Per i codificatori di fotocamera UVC 1.5, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

