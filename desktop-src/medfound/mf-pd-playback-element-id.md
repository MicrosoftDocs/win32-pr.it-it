---
description: Contiene l'identificatore dell'elemento playlist nella presentazione.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 775aca29ab1cea36be9a2b87d64566210c03f6d6771d3493c73d34572975671e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102888"
---
# <a name="mf_pd_playback_element_id-attribute"></a>Attributo MF \_ PD \_ PLAYBACK ELEMENT \_ \_ ID

Contiene l'identificatore dell'elemento playlist nella presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

Le origini multimediali che forniscono playlist possono facoltativamente impostare questo attributo sui relativi descrittori di presentazione.

Quando un'origine multimediale recapita una playlist, invia un [evento MENewPresentation](menewpresentation.md) per ogni elemento playlist dopo il primo. Questo evento contiene un descrittore di presentazione per il nuovo elemento playlist. L'origine multimediale può assegnare identificatori agli elementi impostando l'attributo MF PD PLAYBACK ELEMENT ID per ogni descrittore di presentazione, incluso quello creato da \_ \_ \_ \_ [**IMFMediaSource::CreatePresentationDescriptor.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)

Un'origine multimediale può anche inviare l'evento [MENewPresentation](menewpresentation.md) a causa di un cambio di flusso dinamico o di una modifica nel numero di flussi. In questo caso, il valore di MF PD PLAYBACK ELEMENT ID deve rimanere lo stesso in entrambe le presentazioni, per indicare che entrambe le presentazioni rappresentano \_ \_ lo stesso elemento \_ \_ playlist. Se due presentazioni consecutive hanno lo stesso valore per questo attributo, la pipeline Microsoft Media Foundation prevede che i timestamp rimangano continui durante la transizione. Pertanto, l'origine multimediale non deve usare l'attributo [ \_ MF EVENT \_ SOURCE ACTUAL \_ \_ START](mf-event-source-actual-start-attribute.md) quando esegue la transizione alla presentazione successiva.

Le origini multimediali che implementano [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devono usare l'attributo [ \_ MF TOPONODE \_ SEQUENCE \_ ELEMENTID](mf-toponode-sequence-elementid-attribute.md) anziché l'attributo MF \_ PD \_ PLAYBACK ELEMENT \_ \_ ID.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




