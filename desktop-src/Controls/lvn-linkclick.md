---
title: Codice di notifica LVN_LINKCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stato fatto clic su un collegamento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- Controlli di Windows per il codice di notifica LVN_LINKCLICK
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479432"
---
# <a name="lvn_linkclick-notification-code"></a>\_Codice di notifica LINKCLICK di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che è stato fatto clic su un collegamento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) . L'identificatore del gruppo contenente il collegamento si trova nel membro **iSubItem** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato il modo in cui un'applicazione può rispondere a questo codice di notifica nel gestore di messaggi di [**\_ notifica WM**](wm-notify.md) . Nell'esempio viene attivato o disattivato lo stato compresso del gruppo e viene impostato il testo del collegamento appropriato.

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





