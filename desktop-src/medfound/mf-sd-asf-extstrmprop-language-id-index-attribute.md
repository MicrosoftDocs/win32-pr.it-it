---
description: Specifica la lingua usata da un flusso in un file ASF (Advanced Systems Format).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f77b53a4156cf21a23680618da010db781e0c7c75d7d4decb2f9e1136c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474069"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>Attributo INDEX \_ \_ DELL'ID LINGUA ASF \_ SD EXTSTRMPROP \_ \_ \_ MF

Specifica la lingua usata da un flusso in un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso per il contenuto asf. Il valore è un indice nell'elenco di lingue contenuto nell'attributo [**\_ \_ \_ LANGLIST di MF PD ASF.**](mf-pd-asf-langlist-attribute.md)

Questo attributo corrisponde al campo Stream Language ID Index nell'oggetto Extended Stream Properties. Per altre informazioni, vedere la specifica ASF.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati asf. L'applicazione può creare il descrittore di flusso per il flusso dal descrittore di presentazione chiamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)

È anche possibile ottenere il tag di lingua tramite una query sul descrittore di flusso per [**l'attributo \_ MF SD \_ LANGUAGE.**](mf-sd-language-attribute.md)

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

 

 




