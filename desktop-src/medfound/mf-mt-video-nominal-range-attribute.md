---
description: Specifica l'intervallo nominale delle informazioni sul colore in un tipo di supporto video.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Attributo MF_MT_VIDEO_NOMINAL_RANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318716"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_ \_ \_ Attributo intervallo nominale video MF mt \_

Specifica l'intervallo nominale delle informazioni sul colore in un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

**Codificatori H. 264/AVC:**

Nel tipo di supporto di output, \_ l' \_ intervallo nominale video MF mt \_ \_ può essere impostato con **MFNominalRange \_ 0 \_ 255** e **MFNominalRange \_ 16 \_ 235**.

Il codificatore H. 264/AVC deve considerare **MFNominalRange \_ Unknown** come **MFNominalRange \_ 16 \_ 235**.

Il codificatore H. 264/AVC deve rifiutare un tipo di supporto di output quando MF \_ mt \_ video \_ Nominal \_ Range è impostato su **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** o qualsiasi altro valore non definito in [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Informazioni sui colori estesi](extended-color-information.md)
</dt> </dl>

 

 




