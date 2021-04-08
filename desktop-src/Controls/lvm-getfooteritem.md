---
title: Messaggio LVM_GETFOOTERITEM (COMmctrl. h)
description: Ottiene informazioni su un elemento del piè di pagina in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterItem di ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Controlli di Windows Message LVM_GETFOOTERITEM
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
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047856"
---
# <a name="lvm_getfooteritem-message"></a>\_Messaggio GETFOOTERITEM LVM

Ottiene informazioni su un elemento del piè di pagina in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice dell'elemento.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) per ricevere un valore per i membri **state** e/o **pszText** in base al valore del membro **mask** . Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri per indicare al destinatario le informazioni da restituire. Per ulteriori informazioni, vedere **LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





