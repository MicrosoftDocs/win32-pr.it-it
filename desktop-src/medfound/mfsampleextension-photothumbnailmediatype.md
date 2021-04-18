---
description: Contiene IMFMediaType che descrive il tipo di formato di immagine contenuto nell' \_ attributo di anteprima MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Attributo MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320679"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>\_Attributo PhotoThumbnailMediaType di MFSampleExtension

Contiene [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che descrive il tipo di formato di immagine contenuto nell'attributo di [ \_ Anteprima MFSampleExtension](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Tipo di dati

**IUnknown** archiviato come **IMFMediaType**

## <a name="remarks"></a>Commenti

Se nell'esempio Photo è presente l'attributo [MFSampleExtension \_ fotothumbnail](mfsampleextension-photothumbnail.md) , il PhotoThumbnailMediaType MFSampleExtension \_ è obbligatorio e deve contenere almeno il [ \_ \_ \_ tipo principale MF mt](mf-mt-major-type-attribute.md), il [ \_ \_ sottotipo](mf-mt-subtype-attribute.md) MF mt e la dimensione del [ \_ frame MF \_ \_ mt](mf-mt-frame-size-attribute.md) che descrivono l'anteprima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Anteprima di MFSampleExtension \_](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




