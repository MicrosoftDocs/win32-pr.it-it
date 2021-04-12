---
description: Specifica l'identificatore per il dispositivo dell'endpoint audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344596"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>\_ \_ \_ \_ Attributo ID endpoint dell'attributo di RENDERER audio MF \_

Specifica l'identificatore per il dispositivo dell'endpoint audio.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per configurare il renderer audio. L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* . Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un dispositivo endpoint audio è un dispositivo hardware che si trova in un'estremità di un percorso dati audio, ad esempio una cuffia o un altoparlante. Per ottenere l'identificatore dell'endpoint audio, usare le API principali audio seguenti:

-   Usare l'interfaccia [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) per enumerare i dispositivi nel sistema.
-   Chiamare [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere l'identificatore per il dispositivo.

Per ulteriori informazioni, vedere la documentazione principale sull'API [audio](../coreaudio/core-audio-apis-in-windows-vista.md) . Se questo attributo non è impostato, il renderer audio utilizza il dispositivo endpoint predefinito.

Se questo attributo è impostato, non impostare l'attributo [**del \_ \_ \_ \_ \_ ruolo endpoint dell'attributo del RENDERER MF audio**](mf-audio-renderer-attribute-endpoint-role-attribute.md) . Se entrambi gli attributi sono impostati, si verificherà un errore quando viene creato il renderer audio.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi renderer audio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Renderer audio di streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
