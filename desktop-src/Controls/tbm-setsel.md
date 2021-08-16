---
title: TBM_SETSEL messaggio (Commctrl.h)
description: Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un trackbar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d055b317cc6db5e17edbe57bc57e6dbfe287274788718e8e2a920e1f25d9316b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829330"
---
# <a name="tbm_setsel-message"></a>Messaggio \_ SETSEL TBM

Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il messaggio ridisegna il trackbar dopo l'impostazione dell'intervallo di selezione. Se questo parametro è **FALSE,** il messaggio imposta l'intervallo di selezione, ma non ridisegna il trackbar.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la posizione logica iniziale per l'intervallo di selezione e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione logica finale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il trackbar non ha lo stile [**\_ TBS ENABLESELRANGE.**](trackbar-control-styles.md)

**TBM \_ SETSEL** consente di limitare il puntatore solo a una parte dell'intervallo disponibile per l'indicatore di stato.

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

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

