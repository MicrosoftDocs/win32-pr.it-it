---
description: Specifica la velocità in bit massima dei dati, in bit al secondo, di un flusso in un file ASF (Advanced Systems Format).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9bb445724c15604ab30e353315769f78a71c0d6dd94291392e4c34ee05a70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714361"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a>Attributo MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX DATA \_ \_ BITRATE

Specifica la velocità in bit massima dei dati, in bit al secondo, di un flusso in un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso per il contenuto asf. Corrisponde al campo Alternate Data Bit Rate nell'oggetto Extended Stream Properties. Per altre informazioni, vedere la specifica ASF.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF. L'applicazione può creare il descrittore di flusso per il flusso dal descrittore di presentazione chiamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

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

 

 




