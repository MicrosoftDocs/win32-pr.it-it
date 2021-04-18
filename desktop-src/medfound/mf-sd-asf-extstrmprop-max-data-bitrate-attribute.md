---
description: Specifica la velocità in bit massima dei dati, in bit al secondo, di un flusso in un file di formato Advanced Systems (ASF).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: Attributo MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85626be11afe2e9413852e8aec3533f987538473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317307"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a>\_ \_ \_ \_ Attributo EXTSTRMPROP Max \_ data \_ bitrate MF SD ASF

Specifica la velocità in bit massima dei dati, in bit al secondo, di un flusso in un file di formato Advanced Systems (ASF).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso per il contenuto ASF. Corrisponde al campo frequenza dei bit di dati alternativi nell'oggetto proprietà del flusso esteso. Per ulteriori informazioni, vedere la specifica ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF. L'applicazione può creare il descrittore del flusso per il flusso dal descrittore della presentazione chiamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> </dl>

 

 




