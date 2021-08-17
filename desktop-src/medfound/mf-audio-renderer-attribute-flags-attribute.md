---
description: Contiene flag per configurare il renderer audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1146ce4e363dca63819badd96abcd9d9e91051419df3b5007c237a002bb39d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105007"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>Attributo \_ FLAGS \_ dell'ATTRIBUTO RENDERER AUDIO \_ MF \_

Contiene flag per configurare il renderer audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un **OR** bit per bit dei flag seguenti.



| Valore                                                   | Descrizione                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FLAG DI ATTRIBUTI DEL RENDERER AUDIO MF \_ \_ \_ \_ \_ CROSSPROCESS** | Il renderer audio usa una sessione audio cross-process. Questo flag consente ai renderer audio in più processi di condividere la stessa sessione audio, insieme al volume e ai controlli dei criteri associati.<br/> Se questo flag non è impostato, la sessione audio non può essere condivisa dai renderer audio in altri processi.<br/> |
| **FLAG DEGLI ATTRIBUTI DEL RENDERER AUDIO MF \_ \_ \_ \_ \_ NOPERSIST**    | L Windows'API della sessione audio (WASAPI) non rende persistenti le proprietà per questa sessione audio, ad esempio il volume della sessione.<br/> Se questo flag non è impostato, WASAPI rende persistenti le proprietà della sessione audio.<br/>                                                                                                       |



 

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 




