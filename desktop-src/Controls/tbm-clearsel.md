---
title: TBM_CLEARSEL messaggio (Commctrl.h)
description: Cancella l'intervallo di selezione corrente in un trackbar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- TBM_CLEARSEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 627f2c872b47bf76312856fd81d42bfe8f2739e53efb3c37492b203b150b8e8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046761"
---
# <a name="tbm_clearsel-message"></a>Messaggio \_ CLEARSEL TBM

Cancella l'intervallo di selezione corrente in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il trackbar viene ridisegnato dopo che la selezione è stata cancellata.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un trackbar può avere un intervallo di selezione solo se è stato specificato lo stile [**\_ TBS ENABLESELRANGE**](trackbar-control-styles.md) al momento della creazione.

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

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





