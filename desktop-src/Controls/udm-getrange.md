---
title: UDM_GETRANGE messaggio (Commctrl.h)
description: Recupera le posizioni minima e massima (intervallo) per un controllo di tipo up-down.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13811f383886e0e4985eb3f2f5093eec53cb0745349a36ca133fa3de9656773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408101"
---
# <a name="udm_getrange-message"></a>Messaggio GETRANGE di UDM \_

Recupera le posizioni minima e massima (intervallo) per un controllo di tipo up-down.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore a 32 bit che contiene le posizioni minima e massima. LOWORD [**è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la posizione massima per il controllo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è la posizione minima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

