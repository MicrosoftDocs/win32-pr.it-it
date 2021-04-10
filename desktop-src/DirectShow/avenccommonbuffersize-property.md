---
description: Specifica le dimensioni del buffer utilizzato durante la codifica. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Proprietà AVEncCommonBufferSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125250"
---
# <a name="avenccommonbuffersize-property"></a>Proprietà AVEncCommonBufferSize

Specifica le dimensioni del buffer utilizzato durante la codifica. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Gli intervalli di parametri non sono supportati per i codificatori della fotocamera H. 264 UVC 1,5.

## <a name="remarks"></a>Commenti

Per alcuni formati video, le dimensioni del buffer vengono specificate in bit e per altre vengono specificate in byte. Per informazioni specifiche, vedere la sezione Osservazioni riportata di seguito.

Per il video MPEG questa proprietà definisce la dimensione del buffer VBV (video buffer Verifier). Le dimensioni del buffer sono in bit.

Per il video e la Windows Media Video H. 264, la proprietà definisce la dimensione del decodificatore di riferimento ipotetico (HRD). Dimensioni del buffer in byte.

Per le fotocamere di codifica UVC 1,5 H264, il valore CPB inviato al codificatore della fotocamera deve essere allineato a 16 bit. Dimensioni del buffer in byte.

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

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

 

