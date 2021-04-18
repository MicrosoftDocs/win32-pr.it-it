---
description: Contiene l'identificatore dell'elemento playlist nella presentazione.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Attributo MF_PD_PLAYBACK_ELEMENT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318421"
---
# <a name="mf_pd_playback_element_id-attribute"></a>\_ \_ \_ Attributo ID elemento riproduzione MF PD \_

Contiene l'identificatore dell'elemento playlist nella presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

Le origini multimediali che forniscono playlist possono facoltativamente impostare questo attributo sui rispettivi descrittori di presentazione.

Quando un'origine multimediale recapita una playlist, invia un evento [MENewPresentation](menewpresentation.md) per ogni elemento della playlist dopo il primo. Questo evento contiene un descrittore di presentazione per il nuovo elemento playlist. L'origine multimediale può assegnare gli identificatori agli elementi impostando l' \_ \_ attributo ID dell'elemento di riproduzione MF PD \_ \_ su ogni descrittore di presentazione, incluso quello creato da [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).

Un'origine multimediale può anche inviare l'evento [MENewPresentation](menewpresentation.md) a causa di un commutatore di flusso dinamico o di una modifica nel numero di flussi. In tal caso, il valore dell' \_ ID dell'elemento di riproduzione MF PD \_ \_ \_ deve rimanere invariato in entrambe le presentazioni, per indicare che entrambe le presentazioni rappresentano lo stesso elemento della playlist. Se due presentazioni consecutive hanno lo stesso valore per questo attributo, la pipeline Microsoft Media Foundation prevede che i timestamp rimangano continui attraverso la transizione. Pertanto, l'origine multimediale non deve usare l'attributo di [ \_ \_ \_ \_ avvio effettivo dell'origine eventi MF](mf-event-source-actual-start-attribute.md) quando passa alla presentazione successiva.

Le origini multimediali che implementano [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devono usare l'attributo [ElementID della \_ \_ sequenza \_ MF TOPONODE](mf-toponode-sequence-elementid-attribute.md) anziché \_ l' \_ attributo ID dell'elemento di riproduzione MF PD \_ \_ .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




