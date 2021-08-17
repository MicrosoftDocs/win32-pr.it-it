---
description: Flag di profilo che definiscono le impostazioni del flusso per la topologia di transcodifica. I flag sono definiti nell'enumerazione MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ FLAGS.
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb25f4df47d281ddb0e359d98e8a411cb3abb365b479388e9b7ae107e786703c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739469"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>Attributo MF \_ TRANSCODE \_ ADJUST \_ PROFILE

Flag di profilo che definiscono le impostazioni del flusso per la topologia di transcodifica. I flag sono definiti nell'enumerazione [**MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ FLAGS.**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags)

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Un'applicazione può impostare questo attributo a livello di contenitore nel profilo di transcodifica. Se questo attributo è impostato, la [**funzione MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) modifica gli attributi del flusso durante la compilazione della topologia, a seconda del flag specificato. Ad esempio, se l'applicazione specifica il flag **MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ DEFAULT,** per creare il profilo vengono usate le impostazioni del flusso specificate dall'applicazione.

Per il flusso video, la frequenza dei fotogrammi viene aggiornata in base all'origine multimediale. Se l'applicazione non specifica la modalità interlacciata, il profilo viene aggiornato per l'uso dei fotogrammi progressivi per impostazione predefinita.

Se l'applicazione specifica il flag **MF \_ TRANSCODE \_ ADJUST PROFILE USE SOURCE \_ \_ \_ \_ ATTRIBUTES,** gli attributi di flusso mancanti vengono copiati dall'origine del supporto di input alle impostazioni del flusso nel profilo di transcodifica.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




