---
description: Specifica la categoria del flusso audio.
ms.assetid: 0F2DB9A7-64ED-4952-BCB3-F2B15BA37D2A
title: Attributo MF_MEDIA_ENGINE_AUDIO_CATEGORY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22cd3795886b78afae03ba4b592d4657857f76b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968883"
---
# <a name="mf_media_engine_audio_category-attribute"></a>\_ \_ \_ Attributo categoria audio del motore multimediale MF \_

Specifica la categoria del flusso audio.

## <a name="data-type"></a>Tipo di dati

**[**\_categoria flusso \_ audio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**di \_ \_ categoria del flusso audio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .

Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale. L'attributo è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                            |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
