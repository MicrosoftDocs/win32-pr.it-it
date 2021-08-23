---
description: Specifica il tipo di contenitore di un file codificato.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: MF_TRANSCODE_CONTAINERTYPE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c56b0332c43f10fa61b34f47191e3946a4813b3670249a8d858317067c38d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604691"
---
# <a name="mf_transcode_containertype-attribute"></a>Attributo MF \_ TRANSCODE \_ CONTAINERTYPE

Specifica il tipo di contenitore di un file codificato. I tipi di contenitore sono supportati da Media Foundation.

## <a name="data-type"></a>Tipo di dati

**GUID**

I valori possibili per i tipi di contenitore forniti Media Foundation sono descritti nella tabella seguente.



| Valore                                                                                                                                                                                                                                                                 | Significato                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**MFTranscodeContainerType \_ ASF**</dt> </dl>             | Contenitore di file ASF.<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG4**</dt> </dl>     | Contenitore di file MP4.<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**MFTranscodeContainerType \_ MP3**</dt> </dl>             | Contenitore di file MP3.<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**MFTranscodeContainerType \_ 3GP**</dt> </dl>             | Contenitore di file 3GP. <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**MFTranscodeContainerType \_ AC3**</dt> </dl>             | Contenitore di file AC3. <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**MFTranscodeContainerType \_ ADTS**</dt> </dl>         | Contenitore di file ADTS. <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG2**</dt> </dl>     | Contenitore di file MPEG2. <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ FMPEG4**</dt> </dl> | Contenitore di file FMPEG4. <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**MFTranscodeContainerType \_ WAVE**</dt> </dl>         | Contenitore di file WAVE.<br/> Supportato in Windows 8.1 e versioni successive.<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**MFTranscodeContainerType \_ AVI**</dt> </dl>             | Contenitore di file AVI.<br/> Supportato in Windows 8.1 e versioni successive.<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**MFTranscodeContainerType \_ AMR**</dt> </dl>             | Contenitore di file AMR. <br/>                                                    |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Per impostare questo attributo, chiamare [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Commenti

Questo attributo viene usato sia con la funzionalità Di transcodifica veloce che con l'oggetto writer di sink.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

### <a name="fast-transcode"></a>Transcodifica veloce

L'applicazione deve impostare l'attributo del contenitore nel profilo di transcodifica prima di compilare la topologia di transcodifica. Il generatore di topologie analizza questo attributo e carica il sink multimediale appropriato nella pipeline. Per altre informazioni, vedere i seguenti argomenti:

-   [**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>Sink Writer

Questo attributo può essere usato per configurare il tipo di contenitore di file per il writer di sink. Per altre informazioni, vedere [Attributi del writer di sink.](sink-writer-attributes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API transcodifica](transcode-api.md)
</dt> </dl>

 

 




