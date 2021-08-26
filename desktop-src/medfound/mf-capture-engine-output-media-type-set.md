---
description: Indica che il tipo di output è stato impostato nel motore di acquisizione in risposta a IMFCaptureSink2::SetOutputType.
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138a5893d4ccdd014354e00718a98eda9ba41616c1f1507c8749c9b36dcc0c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013411"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>Attributo MF \_ CAPTURE ENGINE OUTPUT MEDIA TYPE \_ \_ \_ \_ \_ SET

Indica che il tipo di output è stato impostato nel motore di acquisizione in risposta a [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

È possibile chiamare [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) per determinare se l'operazione ha avuto esito positivo o meno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




