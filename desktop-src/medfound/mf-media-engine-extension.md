---
description: Contiene un puntatore all'interfaccia IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: Attributo MF_MEDIA_ENGINE_EXTENSION (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104401830"
---
# <a name="mf_media_engine_extension-attribute"></a>\_Attributo di estensione MF media \_ Engine \_

Contiene un puntatore all'interfaccia [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .

## <a name="data-type"></a>Tipo di dati

**IMFMediaEngineExtension \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.

Questo attributo è facoltativo. Usarlo per fornire un oggetto che implementa l'interfaccia [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) . Questa interfaccia consente all'applicazione di caricare le risorse multimediali personalizzate.

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

 

 




