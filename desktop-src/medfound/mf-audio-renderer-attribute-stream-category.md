---
description: Specifica la categoria del flusso audio per il renderer audio di streaming (SAR, Streaming Audio Renderer).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4acb6bd0f40d3c6fb3caa6b4dce8801f8fa60d31222265d5dca6ff5a132444e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714881"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>Attributo CATEGORIA DEL \_ FLUSSO \_ \_ DELL'ATTRIBUTO DEL RENDERER AUDIO \_ MF \_

Specifica la categoria del flusso audio per il renderer audio di streaming (SAR, [Streaming Audio Renderer).](streaming-audio-renderer.md)

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per configurare il renderer audio. L'utilizzo dipende dalla funzione chiamata per creare il renderer audio.



| Funzione                                                               | Come impostare l'attributo                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | Usare il [**puntatore IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) specificato nel *parametro pAudioAttributes.*                                                                                          |
| [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | Usare il [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito nel *parametro ppActivate.* Impostare l'attributo prima di [**chiamare IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). |



 

Il valore dell'attributo è un membro [**dell'enumerazione AUDIO \_ STREAM \_ CATEGORY.**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) Il servizio audio usa la categoria stream per determinare i criteri audio quando più applicazioni riproducino l'audio contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
