---
title: LVM_ISITEMVISIBLE messaggio (Commctrl.h)
description: Indica se un elemento nel controllo visualizzazione elenco è visibile. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView IsItemVisible.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424d321b79b4a4f497942c36ca78c751cc5404cdfaf965b451eea94a8b3c8e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958180"
---
# <a name="lvm_isitemvisible-message"></a>Messaggio \_ LVM ISITEMVISIBLE

Indica se un elemento nel controllo visualizzazione elenco è visibile. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView IsItemVisible.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indice dell'elemento nel controllo visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** visibile oppure FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





