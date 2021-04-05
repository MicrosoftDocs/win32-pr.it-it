---
title: Codice di notifica TCN_SELCHANGE (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata è stata modificata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- Controlli di Windows per il codice di notifica TCN_SELCHANGE
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739863"
---
# <a name="tcn_selchange-notification-code"></a>\_Codice di notifica SelChange di TCN

Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata è stata modificata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Per determinare la scheda attualmente selezionata, usare la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_SELCHANGING TCN](tcn-selchanging.md)
</dt> </dl>

 

 





