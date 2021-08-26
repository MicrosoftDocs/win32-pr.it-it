---
description: Specifica se la modalità panoramica/analisi è abilitata.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955491"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>Attributo \_ MF MT \_ PAN \_ SCAN \_ ENABLED

Specifica se la modalità panoramica/analisi è abilitata.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE,** deve essere visualizzata solo l'area di panoramica/analisi del video. L'area di panoramica/analisi viene specificata dall'attributo [**\_ MF MT \_ PAN SCAN \_ \_ APERTURE.**](mf-mt-pan-scan-aperture-attribute.md)

Se questo attributo è **FALSE** o non è impostato, verrà visualizzata l'intera apertura di visualizzazione del video. L'apertura dello schermo viene specificata [**dall'attributo \_ MF MT \_ MINIMUM \_ DISPLAY \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md)

Se si imposta questo attributo su **TRUE,** impostare anche il valore dell'attributo [**\_ MF MT \_ PAN SCAN \_ \_ APERTURE.**](mf-mt-pan-scan-aperture-attribute.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Proporzioni immagine](picture-aspect-ratio.md)
</dt> </dl>

 

 




