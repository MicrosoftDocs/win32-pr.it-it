---
description: Quando un'origine multimediale richiede una nuova velocità di riproduzione, questo attributo specifica se l'origine richiede anche l'assottigliamento. Per una definizione di assottigliamento, vedere informazioni sul controllo della frequenza.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Attributo MF_EVENT_DO_THINNING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966800"
---
# <a name="mf_event_do_thinning-attribute"></a>\_Attributo di \_ assottigliamento dell'evento MF \_

Quando un'origine multimediale richiede una nuova velocità di riproduzione, questo attributo specifica se l'origine richiede anche l'assottigliamento. Per una definizione di assottigliamento, vedere [informazioni sul controllo della frequenza](about-rate-control.md).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato con l'evento [MESourceRateChangeRequested](mesourceratechangerequested.md) . Se il valore è **true**, l'origine del supporto richiede un passaggio alla riproduzione diluita.

Il valore predefinito è **false**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




