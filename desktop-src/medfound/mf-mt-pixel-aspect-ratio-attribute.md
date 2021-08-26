---
description: Proporzioni pixel per un tipo di file multimediale video.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e14e07a8011f89d16b095728bc80cbe19faa16ef9427156868f93c2ccb412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060491"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>Attributo MF \_ MT \_ PIXEL ASPECT \_ \_ RATIO

Proporzioni pixel per un tipo di file multimediale video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

I 32 bit superiori contengono il numeratore delle proporzioni pixel e i 32 bit inferiori contengono il denominatore. Il numeratore è il componente orizzontale delle proporzioni; il denominatore è il componente verticale.

Per impostare questo attributo, usare la [**funzione MFSetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) Per ottenere questo attributo, usare la [**funzione MFGetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)

Le proporzioni in pixel descrivono la forma dei pixel nell'immagine video visualizzata. Impostare questo attributo se l'immagine ha pixel non quadrati. Per essere visualizzata correttamente in un dispositivo di visualizzazione con pixel quadrati, l'immagine deve essere ridimensionata in base all'inverso delle proporzioni in pixel dell'immagine.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Proporzioni immagine](picture-aspect-ratio.md)
</dt> </dl>

 

 




