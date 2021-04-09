---
title: Messaggio LVM_GETGROUPINFOBYINDEX (COMmctrl. h)
description: Ottiene informazioni su un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetGroupInfoByIndex di ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Controlli di Windows Message LVM_GETGROUPINFOBYINDEX
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120290"
---
# <a name="lvm_getgroupinfobyindex-message"></a>\_Messaggio GETGROUPINFOBYINDEX LVM

Ottiene informazioni su un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetGroupInfoByIndex di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice del gruppo.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) per ricevere informazioni sul gruppo specificato da *wParam*. Il processo chiamante è responsabile dell'allocazione della memoria per la struttura e di tutti i buffer nella struttura, ad esempio quella a cui fa riferimento il membro **pszHeader** . Impostare qualsiasi membro contingente della struttura, ad esempio **cchHeader** , la dimensione del buffer a cui punta **pszHeader** in **WCHAR** , incluso il **null** di terminazione. Impostare **cbSize** su sizeof (LVGROUP).

Il ricevitore del messaggio è responsabile dell'impostazione dei membri della struttura con le informazioni per il gruppo specificato da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





