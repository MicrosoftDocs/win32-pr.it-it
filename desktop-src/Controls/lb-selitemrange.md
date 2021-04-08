---
title: Messaggio LB_SELITEMRANGE (winuser. h)
description: Consente di selezionare o deselezionare uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Controlli di Windows Message LB_SELITEMRANGE
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
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048652"
---
# <a name="lb_selitemrange-message"></a>\_Messaggio SELITEMRANGE lb

Consente di selezionare o deselezionare uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**True** per selezionare l'intervallo di elementi oppure **false** per deselezionarlo.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero del primo elemento da selezionare. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice in base zero dell'ultimo elemento da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio solo con caselle di riepilogo a selezione multipla.

Questo messaggio può selezionare un intervallo solo entro i primi 65.536 elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

