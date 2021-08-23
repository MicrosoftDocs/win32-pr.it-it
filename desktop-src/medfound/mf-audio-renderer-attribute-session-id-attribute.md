---
description: Specifica la classe di criteri audio per il renderer audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5830a3deeb32ca6a3f766bad1858a803948b7e2c07a36f1f1e3222d00ba6199a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104997"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>Attributo SESSION ID DELL'ATTRIBUTO \_ \_ \_ \_ RENDERER AUDIO MF \_

Specifica la classe di criteri audio per il renderer audio.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo associa il renderer audio a una classe di criteri audio. Ogni classe di criteri ha il proprio volume e il proprio controllo dei criteri. Se questo attributo non è impostato, la nuova sar aggiunge la sessione audio predefinita dell'applicazione. Per altre informazioni, vedere [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) nella documentazione dell'API audio principale.

È possibile usare questo attributo per configurare il renderer audio. L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)impostare questo attributo usando il puntatore a interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel *parametro pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)impostare questo attributo usando il puntatore a interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel *parametro ppActivate.* Impostare l'attributo prima di chiamare [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del renderer audio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
