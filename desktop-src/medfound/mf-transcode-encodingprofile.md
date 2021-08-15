---
description: Specifica il profilo di conformità del dispositivo per la codifica di file ASF (Advanced Streaming Format).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b44a923abc563a84f3536fd6353ac2a3dd2352e472344edf7053d647674908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244232"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>Attributo MF \_ TRANSCODE \_ ENCODINGPROFILE

Specifica il profilo di conformità del dispositivo per la codifica di file ASF (Advanced Streaming Format).

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Usare questo attributo quando si esegue la transcoding in un dispositivo che supporta Windows multimediali. Se questo attributo è impostato, il codificatore userà il profilo di conformità del dispositivo, o modello, Windows codec multimediali. Impostare l'attributo nel profilo di transcodifica prima di compilare la topologia di transcodifica.

Il valore di questo attributo può essere una delle stringhe del modello di conformità elencate negli argomenti seguenti:

-   [Modelli di conformità dei dispositivi audio](../wmformat/audio-device-conformance-templates.md)
-   [Modelli di conformità dei dispositivi video](../wmformat/video-device-conformance-templates.md)

Per Windows codifica Media Video, il generatore di topologie usa questo attributo per impostare la proprietà [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) nel codificatore. Il codificatore tenterà di usare il modello specificato per codificare il contenuto. Per ottenere il modello effettivo, attraversare i nodi della topologia di transcodifica per ottenere un puntatore al nodo del codificatore. Ottenere quindi il valore della proprietà [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) dal codificatore.

Il generatore di topologie usa anche il valore di questo attributo per impostare la proprietà "DeviceConformanceTemplate" nel sink multimediale di ASF.

Se questo attributo è impostato, l'oggetto metadati del file ASF viene sempre generato indipendentemente dal valore specificato dall'applicazione [dell'attributo MF \_ TRANSCODE \_ SKIP METADATA \_ \_ TRANSFER.](mf-transcode-skip-metadata-transfer.md)

Di seguito sono riportati i valori tipici di questo attributo:



| Valore   | Descrizione                      |
|---------|----------------------------------|
| "AP"    | Video sul profilo avanzato           |
| "MP"    | Video del profilo principale               |
| "SP"    | Video semplice sul profilo             |
| "MP@LL" | Profilo principale, video di livello medio |
| "L2"    | Profilo audio, <= 160 Kbps    |



 

La costante GUID per questo attributo viene esportata da mfuuid.lib.

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
</dt> <dt>

[**IMFTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
