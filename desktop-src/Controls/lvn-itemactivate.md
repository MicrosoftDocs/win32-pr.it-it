---
title: Codice di notifica LVN_ITEMACTIVATE (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente attiva un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- Controlli di Windows per il codice di notifica LVN_ITEMACTIVATE
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121762"
---
# <a name="lvn_itemactivate-notification-code"></a>\_Codice di notifica ITEMACTIVATE di LVN

Inviato da un controllo di visualizzazione elenco quando l'utente attiva un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[Versione 4,71](common-control-versions.md). Puntatore a una struttura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni su questo codice di notifica.

[Versione 4,70](common-control-versions.md) e precedenti. Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che riceve il codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

Per ottenere gli elementi attivati, l'applicazione ricevente deve usare il messaggio [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) per recuperare il numero di elementi selezionati e quindi inviare il messaggio [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) con **LVNI \_ selezionato** fino a quando non sono stati recuperati tutti gli elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





