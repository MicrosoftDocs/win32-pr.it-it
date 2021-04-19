---
description: Specifica se un file ASF (Advanced Systems Format) è trasmesso o cercabile. Questo valore corrisponde al campo dei flag dell'oggetto proprietà file, definito nella specifica ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Attributo MF_PD_ASF_FILEPROPERTIES_FLAGS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315030"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>\_ \_ \_ \_ Attributo FLAGs per le proprietà di MF PD ASF

Specifica se un file ASF (Advanced Systems Format) è trasmesso o cercabile. Questo valore corrisponde al campo dei flag dell'oggetto proprietà file, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF. Il valore dell'attributo è un OR bit per bit dei flag seguenti:



| Flag | Descrizione                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Flag broadcast. È in corso la creazione del file.                                                                                                                                                                                                                                      |
| 0x02 | Flag ricercabile. Il file è ricercabile.<br/> Un file è ricercabile se è presente un flusso audio e la dimensione massima del pacchetto di dati è uguale alla dimensione minima del pacchetto di dati. Può anche essere ricercabile se il file ha un flusso audio e un flusso video con un oggetto indice semplice corrispondente.<br/> |



 

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.

Se viene impostato il flag broadcast, i seguenti attributi nel descrittore di presentazione non sono validi:

-   [**\_ \_ \_ ID file delle proprietà dell'ASF MF \_ PD \_**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**ora di creazione delle proprietà di MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**\_ \_ \_ pacchetti FileProperties ASF MF \_ PD**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**\_ \_ \_ durata riproduzione FileProperties ASF \_ di MF PD \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**\_durata dell' \_ \_ invio delle Proprietà FileProperties ASF \_ \_ di MF PD**](mf-pd-asf-fileproperties-send-duration-attribute.md)

Inoltre, i valori di attributo [**\_ \_ \_ \_ Max \_ Packet \_ size**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) e MF PD ASF FileProperties [**\_ \_ \_ \_ Min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) sono impostati sulle dimensioni effettive del pacchetto.

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

 

 




