---
title: UDM_GETRANGE32 messaggio (Commctrl.h)
description: Recupera l'intervallo a 32 bit di un controllo di tipo up-down.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 controlli di Windows messaggio
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72078327b7a580768321f14c1d512e097561ae3441667497a822dc8a8a28b4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077101"
---
# <a name="udm_getrange32-message"></a>Messaggio GETRANGE32 di UDM \_

Recupera l'intervallo a 32 bit di un controllo di tipo up-down.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a un intero con segno che riceve il limite inferiore dell'intervallo di controllo verso l'alto verso il basso. Questo parametro può essere **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un intero con segno che riceve il limite superiore dell'intervallo di controllo verso l'alto. Questo parametro può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





