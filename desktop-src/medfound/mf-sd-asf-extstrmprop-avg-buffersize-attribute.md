---
description: Specifica le dimensioni medie del buffer, in byte, necessarie per un flusso in un file ASF (Advanced Systems Format).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a01aa579e1e271d8d6c3297b76ceec653690ecb67b88f7dc8d314e085f111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955201"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a>Attributo MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE

Specifica le dimensioni medie del buffer, in byte, necessarie per un flusso in un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso per il contenuto asf. Corrisponde al campo Dimensioni buffer nell'oggetto Proprietà flusso esteso e definisce le dimensioni del bucket usate nel modello "bucket che perde". Per altre informazioni, vedere la specifica ASF.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati asf. L'applicazione può creare il descrittore di flusso per il flusso dal descrittore di presentazione chiamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

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

 

 




