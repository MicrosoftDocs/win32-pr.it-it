---
title: Codice di notifica HDN_FILTERCHANGE (COMmctrl. h)
description: Notifica alla finestra padre del controllo intestazione che gli attributi di un filtro di controllo intestazione vengono modificati o modificati. Questo codice di notifica è stato inviato sotto forma di \_ messaggio di notifica WM.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- Controlli di Windows per il codice di notifica HDN_FILTERCHANGE
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475377"
---
# <a name="hdn_filterchange-notification-code"></a>\_Codice di notifica FILTERCHANGE di HDN

Notifica alla finestra padre del controllo intestazione che gli attributi di un filtro di controllo intestazione vengono modificati o modificati. Questo codice di notifica è stato inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento intestazione, inclusi gli attributi che stanno per essere modificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETFILTERCHANGETIMEOUT HDM**](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





