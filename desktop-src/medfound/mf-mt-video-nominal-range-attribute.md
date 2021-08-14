---
description: Specifica l'intervallo nominale delle informazioni sui colori in un tipo di supporto video.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876721"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>Attributo \_ MF MT \_ VIDEO \_ NOMINAL \_ RANGE

Specifica l'intervallo nominale delle informazioni sui colori in un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione MFNominalRange.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

**Codificatori H.264/AVC:**

Nel tipo di supporto di output è possibile impostare MF MT VIDEO NOMINAL RANGE con \_ \_ \_ \_ **MFNominalRange \_ 0 \_ 255** e **MFNominalRange \_ 16 \_ 235.**

Il codificatore H.264/AVC deve considerare **MFNominalRange \_ Unknown** **come MFNominalRange \_ 16 \_ 235.**

Il codificatore H.264/AVC rifiuta un tipo di supporto di output quando MF MT VIDEO NOMINAL RANGE è impostato su \_ \_ \_ \_ **MFNominalRange \_ 48 \_ 208,** **MFNominalRange \_ 64 \_ 127** o qualsiasi altro valore non definito in [**MFNominalRange.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Informazioni estese sui colori](extended-color-information.md)
</dt> </dl>

 

 




