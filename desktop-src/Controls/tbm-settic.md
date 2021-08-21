---
title: TBM_SETTIC messaggio (Commctrl.h)
description: Imposta un segno di graduazione in un trackbar in corrispondenza della posizione logica specificata.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f286a2f03e318629a10651d066da5aa6cfe70aa293f242ad7508d0ef4739a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540021"
---
# <a name="tbm_settic-message"></a>Messaggio \_ TBM SETTIC

Imposta un segno di graduazione in un trackbar in corrispondenza della posizione logica specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Posizione del segno di graduazione. Questo parametro può essere uno qualsiasi dei valori interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il segno di graduazione è impostato oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Un trackbar crea il primo e l'ultimo segno di graduazione. Non usare questo messaggio per impostare il primo e l'ultimo segno di graduazione.

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

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





