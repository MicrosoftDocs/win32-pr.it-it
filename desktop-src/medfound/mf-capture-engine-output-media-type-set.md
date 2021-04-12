---
description: 'Indica che il tipo di output è stato impostato sul motore di acquisizione in risposta a IMFCaptureSink2:: SetOutputType.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: Attributo MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351646"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>\_ \_ \_ \_ \_ Attributo set del tipo di supporto di output del motore \_ di acquisizione MF

Indica che il tipo di output è stato impostato sul motore di acquisizione in risposta a [**IMFCaptureSink2:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

È possibile chiamare [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) per verificare se l'operazione ha avuto esito positivo o negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




