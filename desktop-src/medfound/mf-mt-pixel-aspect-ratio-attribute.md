---
description: Proporzioni in pixel per un tipo di supporto video.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Attributo MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526599"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>Attributo proporzioni MF \_ mt \_ pixel \_ \_

Proporzioni in pixel per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

I 32 bit superiori contengono il numeratore delle proporzioni in pixel e i 32 bit inferiori contengono il denominatore. Il numeratore è il componente orizzontale della proporzioni; il denominatore è il componente verticale.

Per impostare questo attributo, utilizzare la funzione [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Per ottenere questo attributo, usare la funzione [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

Le proporzioni in pixel descrivono la forma dei pixel nell'immagine video visualizzata. Impostare questo attributo se l'immagine ha pixel non quadrati. Per visualizzare correttamente in un dispositivo di visualizzazione con pixel quadrati, l'immagine deve essere ridimensionata in base all'inverso delle proporzioni in pixel dell'immagine.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Proporzioni immagine](picture-aspect-ratio.md)
</dt> </dl>

 

 




