---
description: Consente al motore multimediale di riprodurre contenuto protetto.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Attributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320550"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>\_Attributo MF media \_ Engine \_ Content \_ Protection \_ Manager

Consente al motore multimediale di riprodurre contenuto protetto.

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) . Il chiamante deve implementare l'interfaccia.

Questo attributo può essere uno degli attributi passati a [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). È necessario se il contenuto protetto deve essere riprodotto.

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

[**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




