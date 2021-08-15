---
description: Specifica il tempo, in unità da 100 nanosecondi, necessario per inviare un file ASF (Advanced Systems Format). Un tempo di invio dei pacchetti è l'ora in cui il pacchetto deve essere recapitato in rete. Non è l'ora di presentazione del pacchetto.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: MF_PD_ASF_FILEPROPERTIES_SEND_DURATION attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce635cd02766a3c9ca8b0a0d327db93a4bcaaca76bccd6ae54fda726684ec641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740943"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a>Attributo MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION

Specifica il tempo, in unità da 100 nanosecondi, necessario per inviare un file ASF (Advanced Systems Format). L'ora di *invio di un* pacchetto è l'ora in cui il pacchetto deve essere recapitato in rete. Non è l'ora di presentazione del pacchetto.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto asf.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati asf.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




