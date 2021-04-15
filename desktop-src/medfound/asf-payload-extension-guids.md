---
description: I seguenti GUID definiscono le estensioni del payload per i flussi ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID estensione payload ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524665"
---
# <a name="asf-payload-extension-guids"></a>GUID estensione payload ASF

I seguenti GUID definiscono le estensioni del payload per i flussi ASF (Advanced Systems Format).



| Costante                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**\_SampleDuration MFASFSampleExtension**</dt> </dl>         | I dati indicano la durata, in millisecondi, dell'esempio contenuto nell'oggetto buffer.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**\_OutputCleanPoint MFASFSampleExtension**</dt> </dl> | I dati indicano se l'esempio è un fotogramma chiave. Un valore pari a zero indica che l'esempio non è un fotogramma chiave. Un valore diverso da zero indica che si tratta di un fotogramma chiave.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**\_SMPTE MFASFSampleExtension**</dt> </dl>                                             | I dati sono un codice ora SMPTE.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**\_Nome file MFASFSampleExtension**</dt> </dl>                                 | I dati nell'estensione di esempio specificano il nome del file da cui è stato utilizzato il contenuto del campione.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**\_ContentType MFASFSampleExtension**</dt> </dl>                     | I dati identificano il tipo di contenuto contenuto nell'esempio.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**\_PixelAspectRatio MFASFSampleExtension**</dt> </dl> | I dati indicano le proporzioni in pixel del contenuto nell'esempio.<br/>                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Costanti Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




