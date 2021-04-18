---
description: Specifica la velocità in bit media, in bit al secondo, di un flusso in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto proprietà della velocità in bit del flusso definito nella specifica ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: Attributo MF_SD_ASF_STREAMBITRATES_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313038"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a>\_Attributo velocità in bit MF SD \_ ASF \_ STREAMBITRATES \_

Specifica la velocità in bit media, in bit al secondo, di un flusso in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto proprietà della velocità in bit del flusso definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo e lo imposta sul descrittore del flusso. L'applicazione può creare il descrittore del flusso per il flusso dal descrittore della presentazione chiamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

Il valore dell'attributo è uguale al campo velocità in bit medio nell'oggetto proprietà velocità in bit del flusso.

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

 

 




