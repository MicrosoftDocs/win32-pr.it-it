---
description: Specifica le dimensioni del buffer utilizzato durante la codifica. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Proprietà AVEncCommonBufferSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69eb0c4829d30f3eff0297b7e591686f671d0d67967a65dc76695878d74b454e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794731"
---
# <a name="avenccommonbuffersize-property"></a>AVEncCommonBufferSize - proprietà

Specifica le dimensioni del buffer utilizzato durante la codifica. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Gli intervalli di parametri non sono supportati per i codificatori di fotocamera H.264 UVC 1.5.

## <a name="remarks"></a>Commenti

Per alcuni formati video la dimensione del buffer è specificata in bit e per altri è specificata in byte. Per informazioni specifiche, vedere le osservazioni seguenti.

Per i video MPEG, questa proprietà definisce le dimensioni del buffer vbv (Video Buffer Verifier). Le dimensioni del buffer sono in bit.

Per il video H.264 e Windows Media Video, la proprietà definisce le dimensioni dell'ipotetico decodificatore di riferimento (HRD). Le dimensioni del buffer sono in byte.

Per le fotocamere di codifica UVC 1.5 H264, il valore CPB inviato al codificatore deve essere allineato a 16 bit. Le dimensioni del buffer sono in byte.

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

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

 

