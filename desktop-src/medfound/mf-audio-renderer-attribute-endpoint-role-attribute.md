---
description: Specifica il ruolo endpoint audio per il renderer audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967846"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>\_Attributo del \_ \_ \_ ruolo endpoint dell'attributo RENDERER audio MF \_

Specifica il ruolo endpoint audio per il renderer audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per configurare il renderer audio. L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* . Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un dispositivo endpoint audio è un dispositivo hardware che si trova in un'estremità di un percorso dati audio, ad esempio una cuffia o un altoparlante.

Se questo attributo è impostato, il renderer audio utilizza il dispositivo audio predefinito per il ruolo specificato. Il valore di questo attributo è un membro dell'enumerazione **ERole** , che è definito nel file di intestazione mmdeviceapi. h. Per ulteriori informazioni, vedere la documentazione principale sull'API audio. Se questo attributo non è impostato, il renderer audio utilizza il dispositivo endpoint predefinito.

Se questo attributo è impostato, non impostare l'attributo [**\_ \_ \_ \_ \_ ID endpoint dell'attributo MF audio RENDERER**](mf-audio-renderer-attribute-endpoint-id-attribute.md) . Se entrambi gli attributi sono impostati, si verificherà un errore quando viene creato il renderer audio.

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Renderer audio di streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 




