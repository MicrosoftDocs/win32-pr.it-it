---
title: LVM_GETFOOTERITEM messaggio (Commctrl.h)
description: Ottiene informazioni su un elemento del piè di pagina in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetFooterItem.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0b38bb8a91f93c456bd8096a3736eaec79e6c3472d0f18a133de482bb2c0328
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968281"
---
# <a name="lvm_getfooteritem-message"></a>Messaggio LVM \_ GETFOOTERITEM

Ottiene informazioni su un elemento del piè di pagina in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetFooterItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indice dell'elemento.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) per ricevere un valore per i membri **state** e/o **pszText** in base al valore del **membro mask.** Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri per indicare al ricevitore quali informazioni restituire. Per altre informazioni, vedere **LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





