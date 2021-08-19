---
title: TBM_SETSELSTART messaggio (Commctrl.h)
description: Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo stile \_ TBS ENABLESELRANGE.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8cfdc938da5c7f5904e79f55177fe6f8eccba10f37dfdadb613c581cc809fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829315"
---
# <a name="tbm_setselstart-message"></a>Messaggio \_ TBM SETSELSTART

Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo [**stile \_ TBS ENABLESELRANGE.**](trackbar-control-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il messaggio ridisegna il trackbar dopo l'impostazione dell'intervallo di selezione. Se questo parametro è **FALSE,** il messaggio imposta l'intervallo di selezione ma non ridisegna il trackbar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione iniziale dell'intervallo di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
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

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> </dl>

 

 





