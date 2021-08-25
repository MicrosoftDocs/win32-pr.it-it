---
description: I GUID seguenti definiscono le estensioni del payload per i flussi ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID dell'estensione del payload ASF (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6478c024d3e79b0f8035f03b6e893e2e5d0308037242f9ac3013450b57f83242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959571"
---
# <a name="asf-payload-extension-guids"></a>GUID dell'estensione del payload ASF

I GUID seguenti definiscono le estensioni del payload per i flussi ASF (Advanced Systems Format).



| Costante                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**MFASFSampleExtension \_ SampleDuration**</dt> </dl>         | I dati indicano la durata, in millisecondi, del campione contenuto nell'oggetto buffer.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**Output di MFASFSampleExtensionCleanPoint \_**</dt> </dl> | I dati indicano se l'esempio è un fotogramma chiave. Il valore zero indica che l'esempio non è un fotogramma chiave. Un valore diverso da zero indica che si tratta di un fotogramma chiave.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**MFASFSampleExtension \_ SMPTE**</dt> </dl>                                             | I dati sono un time code SMPTE.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**Nome file MFASFSampleExtension \_**</dt> </dl>                                 | I dati nell'estensione di esempio specificano il nome del file da cui è stato tratto il contenuto dell'esempio.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**MFASFSampleExtension \_ ContentType**</dt> </dl>                     | I dati identificano il tipo di contenuto contenuto nell'esempio.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt> </dl> | I dati indicano le proporzioni pixel del contenuto nell'esempio.<br/>                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Media Foundation costanti](media-foundation-constants.md)
</dt> </dl>

 

 




