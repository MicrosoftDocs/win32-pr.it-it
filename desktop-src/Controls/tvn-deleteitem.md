---
title: Codice di notifica TVN_DELETEITEM (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che è in corso l'eliminazione di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- Controlli di Windows per il codice di notifica TVN_DELETEITEM
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476948"
---
# <a name="tvn_deleteitem-notification-code"></a>\_Codice di notifica DeleteItem di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che è in corso l'eliminazione di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Il membro **itemOld** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **Hite** e **lParam** contengono informazioni valide sull'elemento da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Se il membro **lParam** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) punta alla memoria allocata dall'applicazione, è possibile liberarla quando si riceve il codice di \_ notifica di TVN DeleteItem.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ DELETEITEMW** (Unicode) e **TVN \_ DELETEITEMA** (ANSI)<br/>             |



 

 





