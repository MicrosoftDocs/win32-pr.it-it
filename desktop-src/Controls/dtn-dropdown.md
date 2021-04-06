---
title: Codice di notifica DTN_DROPDOWN (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente attiva il calendario mensile a discesa. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- Controlli di Windows per il codice di notifica DTN_DROPDOWN
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874165"
---
# <a name="dtn_dropdown-notification-code"></a>\_Codice di notifica a discesa DTN

Inviato da un controllo di selezione data e ora (DTP) quando l'utente attiva il calendario mensile a discesa. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sulla notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Un'attività che il gestore di notifiche potrebbe dover eseguire è personalizzare il controllo del calendario a discesa month. Ad esempio, se non si desidera "Vai a oggi", è necessario impostare lo stile [**MCS \_ notoday**](month-calendar-control-styles.md)  del controllo. Per recuperare un handle per il controllo di calendario mensile, inviare il controllo DTP a un messaggio [**\_ GETMONTHCAL DTM**](dtm-getmonthcal.md) . È quindi possibile usare questo handle e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare lo stile del calendario mensile desiderato.

I controlli DTP non gestiscono un controllo calendario mensile figlio statico. Il controllo DTP crea un nuovo controllo di calendario mensile prima di inviare il codice di notifica. Inoltre, il controllo DTP Elimina il controllo figlio quando non è attivo (visibile). Quindi, l'applicazione non deve basarsi su un handle di finestra statico per il calendario mensile figlio del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[primo piano DTN \_](dtn-closeup.md)
</dt> <dt>

[**\_GETMONTHCAL DTM**](dtm-getmonthcal.md)
</dt> </dl>

 

