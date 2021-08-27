---
description: Contiene un puntatore al descrittore di presentazione per l'origine multimediale.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: MF_TOPONODE_PRESENTATION_DESCRIPTOR attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bfa43a57bcead1312ba8138ab085771d29a008fe2558ea7c6bfb29121d631bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113707"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a>Attributo MF \_ TOPONODE \_ PRESENTATION \_ DESCRIPTOR

Contiene un puntatore al descrittore di presentazione per l'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

Il valore dell'attributo è un puntatore [**all'interfaccia IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione. Questo attributo è obbligatorio.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 




