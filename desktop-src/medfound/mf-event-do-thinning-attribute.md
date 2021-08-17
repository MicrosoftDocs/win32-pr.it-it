---
description: Quando un'origine multimediale richiede una nuova velocità di riproduzione, questo attributo specifica se anche l'origine richiede un thinning. Per una definizione di thinning, vedere Informazioni sul controllo della frequenza.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9305df2b17e00b03bd9788ecd8caf26db82b8e331d1c72626374b63e7dcaf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104937"
---
# <a name="mf_event_do_thinning-attribute"></a>Attributo MF \_ EVENT \_ DO \_ THINNING

Quando un'origine multimediale richiede una nuova velocità di riproduzione, questo attributo specifica se anche l'origine richiede un thinning. Per una definizione di thinning, vedere [About Rate Control](about-rate-control.md).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo viene usato con [l'evento MESourceRateChangeRequested.](mesourceratechangerequested.md) Se il valore è **TRUE,** l'origine multimediale richiede un passaggio alla riproduzione con thinning.

Il valore predefinito è **FALSE.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




