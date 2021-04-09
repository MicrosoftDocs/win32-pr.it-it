---
description: Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video, in frame al secondo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Attributo MF_MT_FRAME_RATE_RANGE_MAX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967039"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>\_ \_ \_ \_ Attributo max frequenza frame frequenza MF mt \_

Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video, in frame al secondo.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Per impostare questo attributo, chiamare [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Commenti

La frequenza dei fotogrammi è espressa come rapporto. I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore. Se, ad esempio, la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1.

Se il dispositivo di acquisizione indica una frequenza massima dei fotogrammi, l'origine del supporto imposta questo attributo sul tipo di supporto. La frequenza minima dei fotogrammi viene specificata nell'attributo dell' [ \_ intervallo di \_ \_ frequenza \_ \_ dei fotogrammi MF mt](mf-mt-frame-rate-range-min.md) . Non è garantito che il dispositivo supporti ogni incremento entro questo intervallo.

Per impostare la frequenza dei fotogrammi del dispositivo, modificare prima di tutto il valore dell'attributo [**MF \_ mt \_ frame \_ rate**](mf-mt-frame-rate-attribute.md) nel tipo di supporto. Impostare quindi il tipo di supporto nell'origine supporto.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Come impostare la frequenza dei fotogrammi di acquisizione video](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[\_intervallo di \_ \_ frequenza frame \_ MF \_ mt](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




