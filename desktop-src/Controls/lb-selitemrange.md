---
title: LB_SELITEMRANGE messaggio (Winuser.h)
description: Seleziona o deseleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958600"
---
# <a name="lb_selitemrange-message"></a>Messaggio LB \_ SELITEMRANGE

Seleziona o deseleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**TRUE** per selezionare l'intervallo di elementi oppure **FALSE per** deselezionarlo.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero del primo elemento da selezionare. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) l'indice in base zero dell'ultimo elemento da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ ERR.

## <a name="remarks"></a>Commenti

Usare questo messaggio solo con caselle di riepilogo a selezione multipla.

Questo messaggio può selezionare un intervallo solo all'interno dei primi 65.536 elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

