---
title: UDM_SETRANGE messaggio (Commctrl.h)
description: Imposta le posizioni minima e massima (intervallo) per un controllo up-down.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60499c960b7f2e496dc4317229865a8838013fc5d78c194072bee27e761ba4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408056"
---
# <a name="udm_setrange-message"></a>Messaggio SETRANGE di UDM \_

Imposta le posizioni minima e massima (intervallo) per un controllo up-down.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **valore breve** che specifica la posizione massima per il controllo verso l'alto e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **breve** che specifica la posizione minima. Nessuna delle due posizioni può essere maggiore del valore UD \_ MAXVAL o minore del valore UD \_ MINVAL. Inoltre, la differenza tra le due posizioni non può superare UD \_ MAXVAL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La posizione massima può essere inferiore alla posizione minima. Facendo clic sul pulsante freccia su, la posizione corrente viene spostata più vicina alla posizione massima e facendo clic sul pulsante freccia giù si sposta verso la posizione minima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM \_ SETRANGE**](udm-setrange.md)
</dt> </dl>

 

