---
description: Specifica se un file ASF (Advanced Systems Format) contiene flussi non audio o video.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7033eb93ccfdf1c7431b92bebb2ee0e4e4193e5055328923ac81c81fa1ccd244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876262"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a>MF \_ PD \_ ASF \_ INFO HA \_ \_ \_ l'attributo VIDEO NON AUDIO \_

Specifica se un file ASF (Advanced Systems Format) contiene flussi non audio o video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto di ASF. Se il valore è **TRUE,** il file ha almeno un flusso che non è audio o video. Ad esempio, flussi di immagini, comandi di script e dati arbitrari personalizzati.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati asf.

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

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto Intestazione ASF](asf-file-structure.md)
</dt> </dl>

 

 




