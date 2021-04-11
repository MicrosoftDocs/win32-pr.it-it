---
description: Specifica se il motore multimediale giocherà contenuto protetto.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Attributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351351"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>\_Attributo di \_ \_ flag di protezione del contenuto del motore multimediale \_ MF \_

Specifica se il motore multimediale giocherà contenuto protetto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un operatore OR bit per bit di **flag dell'enumerazione** dei flag di [**\_ protezione MF media \_ Engine \_ \_**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) . Per abilitare la riproduzione del contenuto protetto, impostare il flag **MF \_ media \_ Engine \_ enable \_ protected \_ Content** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore multimediale](media-engine-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




