---
description: Contiene IMFMediaType che descrive il tipo di formato dell'immagine contenuto nell'attributo MFSampleExtension \_ PhotoThumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713601"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>Attributo MFSampleExtension \_ PhotoThumbnailMediaType

Contiene [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che descrive il tipo di formato dell'immagine contenuto nell'attributo [MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)

## <a name="data-type"></a>Tipo di dati

**IUnknown** archiviato come **IMFMediaType**

## <a name="remarks"></a>Commenti

Se l'attributo [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md) è presente nell'esempio di foto, l'attributo MFSampleExtension PhotoThumbnailMediaType è obbligatorio e deve contenere \_ almeno [MF \_ MT MAJOR \_ \_ TYPE,](mf-mt-major-type-attribute.md) [MF MT \_ \_ SUBTYPE](mf-mt-subtype-attribute.md) e [MF MT FRAME \_ \_ \_ SIZE](mf-mt-frame-size-attribute.md) che descrivono l'anteprima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




