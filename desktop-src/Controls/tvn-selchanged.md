---
title: TVN_SELCHANGED di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che la selezione è stata modificata da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED del codice di notifica Windows controlli
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
ms.openlocfilehash: 7708d797edebc8c2c0bf43b910aec4dc0a1d6ece1a8a535fdcac57e6b15d6e04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957780"
---
# <a name="tvn_selchanged-notification-code"></a>Codice di notifica \_ TVN SELCHANGED

Notifica alla finestra padre di un controllo visualizzazione albero che la selezione è stata modificata da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) **ItemOld** e **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item. Sono **validi solo** i membri mask , **hItem**, **state** e **lParam** di queste strutture. I **membri stateMask** delle **strutture TVITEM** specificate da **itemOld** e **itemNew** non sono definiti nell'input. Il **membro** azione della **struttura NMTREEVIEW** indica il tipo di azione che ha causato la modifica della selezione. Può essere uno dei valori seguenti:



| Requisito | Valore |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Da una sequenza di tasti.   |
| TVC \_ BYMOUSE    | Con un clic del mouse. |
| TVC \_ UNKNOWN    | Sconosciuto.          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) e **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





