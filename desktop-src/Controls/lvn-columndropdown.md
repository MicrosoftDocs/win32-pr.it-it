---
title: Codice di notifica LVN_COLUMNDROPDOWN (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando viene premuto il pulsante a discesa della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- Controlli di Windows per il codice di notifica LVN_COLUMNDROPDOWN
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517788"
---
# <a name="lvn_columndropdown-notification-code"></a>\_Codice di notifica COLUMNDROPDOWN di LVN

Inviato da un controllo di visualizzazione elenco quando viene premuto il pulsante a discesa della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che descrive il codice di notifica. Il chiamante è responsabile dell'allocazione di questa struttura, inclusa la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta. Impostare i membri della struttura **NMHDR** . Il membro del **codice** deve essere impostato su LVN \_ COLUMNDROPDOWN.

Impostare il membro **iItem** della struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) su-1. Impostare il membro **iSubItem** sull'indice dell'elemento secondario. Impostare i membri **uNewState**, **uOldState** e **lParam** su zero. Gli altri membri della struttura **NMLISTVIEW** non vengono usati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Il parametro *wParam* contiene l'ID del controllo che invia il codice di notifica.

Se un controllo intestazione è figlio della visualizzazione elenco, il controllo intestazione deve inviare questo codice notifiche al controllo elenco-visualizzazione quando il controllo intestazione riceve il codice di notifica a [ \_ discesa HDN](hdn-dropdown.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





