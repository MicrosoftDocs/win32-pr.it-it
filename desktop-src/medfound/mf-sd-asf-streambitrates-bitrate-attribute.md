---
description: Specifica la velocità in bit media, in bit al secondo, di un flusso in un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto Stream Bitrate Properties definito nella specifica ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: MF_SD_ASF_STREAMBITRATES_BITRATE attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4190ed64a1d241e17a4fad1481977a27dd62ba0f293f686b55a45f417e89d3d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605171"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a>Attributo MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATES

Specifica la velocità in bit media, in bit al secondo, di un flusso in un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto Stream Bitrate Properties definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo e lo imposta sul descrittore di flusso. L'applicazione può creare il descrittore di flusso per il flusso dal descrittore di presentazione chiamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

Il valore dell'attributo è uguale al campo Velocità in bit media nell'oggetto Proprietà velocità bit del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> </dl>

 

 




