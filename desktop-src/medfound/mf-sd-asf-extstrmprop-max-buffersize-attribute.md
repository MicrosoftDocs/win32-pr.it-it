---
description: Specifica le dimensioni massime del buffer, in byte, necessarie per un flusso in un file ASF (Advanced Systems Format).
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399f6af425020a72caf6185da18f7747c037a71245b8e8d841d886d7b7eabd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113731"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a>Attributo MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE

Specifica le dimensioni massime del buffer, in byte, necessarie per un flusso in un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso per il contenuto asf. Corrisponde al campo Alternate Buffer Size nell'oggetto Extended Stream Properties. Per altre informazioni, vedere la specifica ASF.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati asf. L'applicazione può creare il descrittore di flusso per il flusso dal descrittore di presentazione chiamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> <dt>

[Oggetto Intestazione ASF](asf-file-structure.md)
</dt> </dl>

 

 




