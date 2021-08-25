---
title: RB_GETRECT messaggio (Commctrl.h)
description: Recupera il rettangolo di delimitazione per una determinata banda in un controllo Rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d2f085fa7c6f413700156999f1325879f91affc2c8984fb33d08cb6cc90b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169297"
---
# <a name="rb_getrect-message"></a>Messaggio \_ GETRECT RB

Recupera il rettangolo di delimitazione per una determinata banda in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di una banda nel controllo Rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceverà i limiti della banda rebar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

