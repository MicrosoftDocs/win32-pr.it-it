---
title: TBM_SETSELEND messaggio (Commctrl.h)
description: Imposta la posizione logica finale dell'intervallo di selezione corrente in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo stile \_ TBS ENABLESELRANGE.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND dei messaggi Windows
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ee524bf6a519a7d0071e4149ed03191a9aec989e2deefe596cca1072dbd098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167066"
---
# <a name="tbm_setselend-message"></a>TBM \_ SETSELEND message

Imposta la posizione logica finale dell'intervallo di selezione corrente in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo stile [**\_ TBS ENABLESELRANGE.**](trackbar-control-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il messaggio ridisegna il trackbar dopo l'impostazione dell'intervallo di selezione. Se questo parametro è **FALSE,** il messaggio imposta l'intervallo di selezione, ma non ridisegna il trackbar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione logica finale dell'intervallo di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





