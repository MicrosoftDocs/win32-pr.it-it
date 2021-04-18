---
description: Imposta un oggetto visivo Microsoft DirectComposition come area di riproduzione per il motore multimediale.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Attributo MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320701"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>\_ \_ \_ Attributo visivo per la riproduzione del motore multimediale \_ MF

Imposta un oggetto visivo Microsoft DirectComposition come area di riproduzione per il motore multimediale.

## <a name="data-type"></a>Tipo di dati

**IDCompositionVisual \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su DirectComposition, vedere [DirectComposition](../directcomp/directcomposition-portal.md) e [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).

Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
