---
title: Codice di notifica HDN_FILTERBTNCLICK (COMmctrl. h)
description: Notifica alla finestra padre del controllo intestazione quando viene fatto clic sul pulsante del filtro o in risposta a un \_ messaggio HDM. Questo codice di notifica è stato inviato sotto forma di \_ messaggio di notifica WM.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- Controlli di Windows per il codice di notifica HDN_FILTERBTNCLICK
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873378"
---
# <a name="hdn_filterbtnclick-notification-code"></a>\_Codice di notifica FILTERBTNCLICK di HDN

Notifica alla finestra padre del controllo intestazione quando viene fatto clic sul pulsante del filtro o in risposta a un [**messaggio \_ HDM**](hdm-setitem.md) . Questo codice di notifica è stato inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) contenente informazioni sul controllo intestazione e sul pulsante filtro intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si restituisce **true**, verrà inviato un codice di notifica [ \_ FILTERCHANGE HDN](hdn-filterchange.md) alla finestra padre del controllo intestazione. Questo codice di notifica fornisce alla finestra padre la possibilità di sincronizzare gli elementi dell'interfaccia utente. Restituisce **false** se non si desidera che venga inviata la notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





