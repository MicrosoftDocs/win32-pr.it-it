---
description: Specifica il profilo MPEG-2 o H. 264 in un tipo di supporto video.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: Attributo MF_MT_MPEG2_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883214"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a>\_ \_ Attributo profilo MF mt MPEG2 \_

Specifica il profilo MPEG-2 o H. 264 in un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Per il video MPEG-2, il valore di questo attributo è un membro dell'enumerazione [**am \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .

Per il video H. 264, il valore è un membro dell'enumerazione [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

Questo attributo corrisponde al membro **dwProfile** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
