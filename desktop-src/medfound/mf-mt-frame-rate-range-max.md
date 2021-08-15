---
description: Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video, in fotogrammi al secondo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5988a6aee872489327707c7e87639f7467560014c5bdd29bc9b0bd9a136ccbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742043"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>Attributo \_ MF MT \_ FRAME \_ RATE RANGE \_ \_ MAX

Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video, in fotogrammi al secondo.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**MFGetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)

Per impostare questo attributo, chiamare [**MFSetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)

## <a name="remarks"></a>Commenti

La frequenza dei fotogrammi è espressa come rapporto. I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore. Ad esempio, se la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1.

Se il dispositivo di acquisizione segnala una frequenza massima dei fotogrammi, l'origine multimediale imposta questo attributo sul tipo di supporto. La frequenza dei fotogrammi minima è specificata [nell'attributo \_ MF MT \_ FRAME RATE \_ RANGE \_ \_ MIN.](mf-mt-frame-rate-range-min.md) Non è garantito che il dispositivo supporti ogni incremento all'interno di questo intervallo.

Per impostare la frequenza dei fotogrammi del dispositivo, modificare prima di tutto il valore dell'attributo [**\_ MF MT \_ FRAME \_ RATE**](mf-mt-frame-rate-attribute.md) nel tipo di supporto. Impostare quindi il tipo di supporto nell'origine multimediale.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Come impostare la frequenza dei fotogrammi di acquisizione video](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




