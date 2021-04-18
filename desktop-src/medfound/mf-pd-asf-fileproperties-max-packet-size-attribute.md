---
description: Specifica la dimensione massima del pacchetto, in byte, di un file di formato Advanced Systems (ASF).
ms.assetid: 8dcae150-2363-47ba-b0d3-0bc182574d81
title: Attributo MF_PD_ASF_FILEPROPERTIES_MAX_PACKET_SIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9c95b7511525570a9e04a33db8128f374f9472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315029"
---
# <a name="mf_pd_asf_fileproperties_max_packet_size-attribute"></a>\_Attributo delle \_ \_ \_ dimensioni massime del \_ pacchetto \_ per le proprietà dell'ASF di MF PD ASF

Specifica la dimensione massima del pacchetto, in byte, di un file di formato Advanced Systems (ASF).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.

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

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




