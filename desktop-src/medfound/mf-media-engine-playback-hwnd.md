---
description: Imposta un handle per una finestra di riproduzione video per il motore di contenuti multimediali.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: MF_MEDIA_ENGINE_PLAYBACK_HWND attributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a273702a8a4797c0cf05bd4fe79909dd50a004f313a4caec41c3843dc2bc09b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013031"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a>Attributo \_ \_ \_ HWND DI RIPRODUZIONE DEL MOTORE \_ MULTIMEDIALE MF

Imposta un handle per una finestra di riproduzione video per il motore di contenuti multimediali.

## <a name="data-type"></a>Tipo di dati

**HWND archiviato** come **UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="remarks"></a>Commenti

Questo attributo viene usato con il [**metodo IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




