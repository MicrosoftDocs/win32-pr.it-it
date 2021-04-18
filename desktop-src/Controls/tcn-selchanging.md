---
title: Codice di notifica TCN_SELCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata sta per essere modificata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- Controlli di Windows per il codice di notifica TCN_SELCHANGING
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300962"
---
# <a name="tcn_selchanging-notification-code"></a>\_Codice di notifica SELCHANGING di TCN

Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata sta per essere modificata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per impedire la modifica della selezione o **false** per consentire la modifica della selezione.

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

[\_selChange TCN](tcn-selchange.md)
</dt> </dl>

 

 





