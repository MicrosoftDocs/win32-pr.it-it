---
title: Codice di notifica TVN_SELCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione è cambiata da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- Controlli di Windows per il codice di notifica TVN_SELCHANGED
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874474"
---
# <a name="tvn_selchanged-notification-code"></a>\_Codice di notifica SELCHANGED di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione è cambiata da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . I membri **itemOld** e **ItemNew** della struttura **NMTREEVIEW** sono strutture [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) contenenti informazioni sull'elemento selezionato in precedenza e sull'elemento appena selezionato. Sono validi solo i membri **mask**, **hitet**, **state** e **lParam** di queste strutture. I membri **stateMask** delle strutture **TVITEM** specificate da **itemOld** e **itemNew** non sono definiti nell'input. Il membro **Action** della struttura **NMTREEVIEW** indica il tipo di azione che ha causato la modifica della selezione. Può essere uno dei valori seguenti:



| Requisito | Valore |
|-----------------|-------------------|
| \_BYKEYBOARD TVC | Da una sequenza di tasti.   |
| \_BYMOUSE TVC    | Con un clic del mouse. |
| TVC \_ sconosciuto    | Sconosciuto.          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) e **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





