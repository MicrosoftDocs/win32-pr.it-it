---
title: LVM_GETGROUPINFOBYINDEX messaggio (Commctrl.h)
description: Ottiene informazioni su un gruppo specificato. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetGroupInfoByIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX di controllo Windows messaggio
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
ms.openlocfilehash: 482683e9d1026c1deed17bf1f05310d63ac2127a6a2a6f32b5b5d95a0fbbea3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877401"
---
# <a name="lvm_getgroupinfobyindex-message"></a>Messaggio LVM \_ GETGROUPINFOBYINDEX

Ottiene informazioni su un gruppo specificato. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetGroupInfoByIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indice del gruppo.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) per ricevere informazioni sul gruppo specificato da *wParam.* Il processo chiamante è responsabile dell'allocazione della memoria per la struttura e per tutti i buffer nella struttura, ad esempio quello a cui punta **il membro pszHeader.** Impostare tutti i membri contingenti della struttura, ad esempio **cchHeader,** le dimensioni del buffer a cui punta **pszHeader** nei **WCHAR,** incluso il valore NULL di **terminazione.** Impostare **cbSize** su sizeof(LVGROUP).

Il ricevitore del messaggio è responsabile dell'impostazione dei membri della struttura con le informazioni per il gruppo specificato da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





