---
description: Contiene i flag per configurare il renderer audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Attributo MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309593"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>\_ \_ \_ Attributo Flags dell'attributo del RENDERER MF audio \_

Contiene i flag per configurare il renderer audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è **un operatore OR** bit per bit dei flag seguenti.



| Valore                                                   | Descrizione                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_flag di \_ attributo del RENDERER MF audio \_ \_ \_ CROSSPROCESS** | Il renderer audio usa una sessione audio tra processi. Questo flag consente ai renderer audio in più processi di condividere la stessa sessione audio, insieme ai controlli del volume e dei criteri associati.<br/> Se questo flag non è impostato, la sessione audio non può essere condivisa dai renderer audio in altri processi.<br/> |
| **\_flag di attributo del RENDERER MF audio \_ \_ \_ \_ nopermanente**    | L'API di sessione audio (WASAPI) di Windows non rende permanente le proprietà per questa sessione audio, ad esempio il volume della sessione.<br/> Se questo flag non è impostato, WASAPI manterranno le proprietà della sessione audio.<br/>                                                                                                       |



 

È possibile usare questo attributo per configurare il renderer audio. L'utilizzo dipende dalla funzione chiamata per creare il renderer audio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): impostare questo attributo usando il puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel parametro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): impostare questo attributo usando il puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperato nel parametro *ppActivate* . Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

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

 

 




