---
title: Codice di notifica TVN_BEGINDRAG (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- Controlli di Windows per il codice di notifica TVN_BEGINDRAG
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873882"
---
# <a name="tvn_begindrag-notification-code"></a>\_Codice di notifica BEGINDRAG di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento trascinato nei membri **Hite**, **state** e **lParam** . Il membro **ptDrag** specifica le coordinate dello schermo correnti del mouse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Un controllo di visualizzazione albero con lo stile [**\_ DISABLEDRAGDROP TV**](tree-view-control-window-styles.md) non invia questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ BEGINDRAGW** (Unicode) e **TVN \_ BEGINDRAGA** (ANSI)<br/>               |



 

 





