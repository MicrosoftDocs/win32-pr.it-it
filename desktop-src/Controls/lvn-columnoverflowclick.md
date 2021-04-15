---
title: Codice di notifica LVN_COLUMNOVERFLOWCLICK (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando si fa clic sul pulsante di overflow. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- Controlli di Windows per il codice di notifica LVN_COLUMNOVERFLOWCLICK
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479448"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>\_Codice di notifica COLUMNOVERFLOWCLICK di LVN

Inviato da un controllo di visualizzazione elenco quando si fa clic sul pulsante di overflow. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che descrive il codice di notifica. Il chiamante è responsabile dell'allocazione di questa struttura, inclusa la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta. Impostare i membri della struttura **NMHDR** . Il membro del **codice** deve essere impostato su LVN \_ COLUMNOVERFLOWCLICK.

Impostare il membro **iItem** della struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) su-1. Impostare il membro **iSubItem** sull'indice dell'elemento secondario. Impostare i membri **uNewState**, **uOldState** e **lParam** su zero. Gli altri membri della struttura **NMLISTVIEW** non vengono usati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Il parametro *wParam* contiene l'ID del controllo che invia il codice di notifica.

Se un controllo intestazione è figlio di ListView, il controllo intestazione deve inviare questo codice di notifica al controllo ListView quando il controllo intestazione riceve il codice di [notifica \_ OVERFLOWCLICK HDN](hdn-overflowclick.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





