---
description: Specifica se il motore multimediale riprodurrà contenuto protetto.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS attributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956441"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>Attributo MF \_ MEDIA ENGINE CONTENT PROTECTION \_ \_ \_ \_ FLAGS

Specifica se il motore multimediale riprodurrà contenuto protetto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un **OR** bit per bit di flag dell'enumerazione [**MF \_ MEDIA ENGINE \_ PROTECTION \_ \_ FLAGS.**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) Per abilitare la riproduzione del contenuto protetto, impostare il flag **MF \_ MEDIA ENGINE ENABLE PROTECTED \_ \_ \_ \_ CONTENT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore multimediale](media-engine-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




