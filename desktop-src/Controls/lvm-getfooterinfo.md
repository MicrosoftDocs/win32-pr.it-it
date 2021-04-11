---
title: Messaggio LVM_GETFOOTERINFO (COMmctrl. h)
description: Ottiene informazioni sul piè di pagina di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterInfo di ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Controlli di Windows Message LVM_GETFOOTERINFO
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963767"
---
# <a name="lvm_getfooterinfo-message"></a>\_Messaggio GETFOOTERINFO LVM

Ottiene informazioni sul piè di pagina di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterInfo di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato. Deve essere 0.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) per ricevere informazioni a seconda del valore del membro **mask** . Il processo chiamante è responsabile dell'allocazione della struttura e dell'impostazione del membro **mask** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





