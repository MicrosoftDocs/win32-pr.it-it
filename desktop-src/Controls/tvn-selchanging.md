---
title: Codice di notifica TVN_SELCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione sta per passare da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- Controlli di Windows per il codice di notifica TVN_SELCHANGING
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048252"
---
# <a name="tvn_selchanging-notification-code"></a>\_Codice di notifica SELCHANGING di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione sta per passare da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . I membri **itemOld** e **itemNew** contengono informazioni valide sull'elemento attualmente selezionato e sull'elemento appena selezionato. Il membro dell' **azione** indica se un'azione del mouse o della tastiera sta causando la modifica della selezione. Per un elenco di valori possibili, vedere la descrizione del codice di notifica di [TVN \_ SELCHANGED](tvn-selchanged.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per impedire la modifica della selezione.

## <a name="remarks"></a>Commenti

Quando si rispondo a questo codice di notifica, le applicazioni non devono eliminare gli elementi che stanno ottenendo o non hanno perso la selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ SELCHANGINGW** (Unicode) e **TVN \_ SELCHANGINGA** (ANSI)<br/>           |



 

 





