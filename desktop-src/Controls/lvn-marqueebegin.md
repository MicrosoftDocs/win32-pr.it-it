---
title: Codice di notifica LVN_MARQUEEBEGIN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è iniziata una selezione del rettangolo di selezione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- Controlli di Windows per il codice di notifica LVN_MARQUEEBEGIN
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302797"
---
# <a name="lvn_marqueebegin-notification-code"></a>\_Codice di notifica MARQUEEBEGIN di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che è iniziata una selezione del rettangolo di selezione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per accettare il codice di notifica, restituire zero. Per uscire dalla selezione del rettangolo di selezione, restituire un valore diverso da zero.

## <a name="remarks"></a>Commenti

La *selezione* di un riquadro è il processo che consente di fare clic sull'area client della finestra visualizzazione elenco e di trascinare per selezionare più elementi contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





