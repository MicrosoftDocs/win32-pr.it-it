---
description: Specifica la categoria del flusso audio.
ms.assetid: 0F2DB9A7-64ED-4952-BCB3-F2B15BA37D2A
title: MF_MEDIA_ENGINE_AUDIO_CATEGORY attributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939c5ac839544acb8dd65c2ecae1769c7dd79bb78b19fe40c1f8ae27865ca03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104787"
---
# <a name="mf_media_engine_audio_category-attribute"></a>Attributo MF \_ MEDIA \_ ENGINE AUDIO \_ \_ CATEGORY

Specifica la categoria del flusso audio.

## <a name="data-type"></a>Tipo di dati

**[**CATEGORIA \_ DI FLUSSI \_ AUDIO**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione AUDIO \_ STREAM \_ CATEGORY.**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)

Questo attributo viene usato con il [**metodo IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale. L'attributo è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
