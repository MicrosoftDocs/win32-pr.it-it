---
description: Specifica l'identificatore per il dispositivo endpoint audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dd99a42442342e25c748e12f8af84a03f2322b8c3dd24bb915b50b57952d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941131"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>Attributo \_ \_ ID ENDPOINT \_ DELL'ATTRIBUTO DEL \_ RENDERER AUDIO \_ MF

Specifica l'identificatore per il dispositivo endpoint audio.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per configurare il renderer audio. L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)impostare questo attributo usando il puntatore a interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel *parametro pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)impostare questo attributo usando il puntatore di interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel *parametro ppActivate.* Impostare l'attributo prima di [**chiamare IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un dispositivo endpoint audio è un dispositivo hardware che si trova a un'estremità di un percorso dati audio, ad esempio una cuffia o un altoparlante. Per ottenere l'identificatore dell'endpoint audio, usare le API audio di base seguenti:

-   Usare [**l'interfaccia IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) per enumerare i dispositivi nel sistema.
-   Chiamare [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere l'identificatore per il dispositivo.

Per altre informazioni, vedere la documentazione [dell'API Audio](../coreaudio/core-audio-apis-in-windows-vista.md) Core. Se questo attributo non è impostato, il renderer audio usa il dispositivo endpoint predefinito.

Se questo attributo è impostato, non impostare l'attributo ENDPOINT ROLE dell'ATTRIBUTO [**\_ DEL \_ \_ \_ RENDERER AUDIO \_ MF.**](mf-audio-renderer-attribute-endpoint-role-attribute.md) Se entrambi gli attributi sono impostati, si verificherà un errore durante la creazione del renderer audio.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del renderer audio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
