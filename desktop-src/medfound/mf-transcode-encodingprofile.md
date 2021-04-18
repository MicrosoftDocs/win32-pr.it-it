---
description: Specifica il profilo di conformità del dispositivo per la codifica di file ASF (Advanced Streaming Format).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Attributo MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527408"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>\_Attributo transcode \_ ENCODINGPROFILE MF

Specifica il profilo di conformità del dispositivo per la codifica di file ASF (Advanced Streaming Format).

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Usare questo attributo per la transcodifica in un dispositivo che supporta Windows Media. Se questo attributo è impostato, il codificatore utilizzerà il profilo di conformità del dispositivo, o modello, per i codec Windows Media. Impostare l'attributo sul profilo transcode prima di compilare la topologia transcodifica.

Il valore di questo attributo può essere una qualsiasi delle stringhe di modello di conformità elencate negli argomenti seguenti:

-   [Modelli di conformità del dispositivo audio](../wmformat/audio-device-conformance-templates.md)
-   [Modelli di conformità del dispositivo video](../wmformat/video-device-conformance-templates.md)

Per Windows Media Video codifica, il generatore di topologia utilizza questo attributo per impostare la proprietà [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) nel codificatore. Il codificatore tenterà di utilizzare il modello specificato per codificare il contenuto. Per ottenere il modello effettivo, attraversare i nodi della topologia transcodifica per ottenere un puntatore al nodo del codificatore. Ottenere quindi il valore della proprietà [**\_ DECODERCOMPLEXITYPROFILE di MFPKEY**](mfpkey-decodercomplexityprofileproperty.md) dal codificatore.

Il generatore di topologia usa inoltre il valore di questo attributo per impostare la proprietà "DeviceConformanceTemplate" sul sink multimediale ASF.

Se questo attributo è impostato, l'oggetto di metadati del file ASF viene sempre generato indipendentemente dal valore specificato dall'applicazione dell'attributo [MF \_ transcode \_ Skip \_ Metadata \_ Transfer](mf-transcode-skip-metadata-transfer.md) .

I valori tipici di questo attributo includono i seguenti:



| Valore   | Descrizione                      |
|---------|----------------------------------|
| Asia Pacifico    | Video profilo avanzato           |
| MP    | Video del profilo principale               |
| SP    | Video di profilo semplice             |
| "MP@LL" | Profilo principale, video di livello medio |
| L2    | Profilo audio, <= 160 Kbps    |



 

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
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

 

 
