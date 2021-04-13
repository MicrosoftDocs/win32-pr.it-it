---
title: Messaggio WM_NEXTDLGCTL (winuser. h)
description: Inviato a una procedura della finestra di dialogo per impostare lo stato attivo su un altro controllo nella finestra di dialogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Finestre di dialogo WM_NEXTDLGCTL messaggio
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518345"
---
# <a name="wm_nextdlgctl-message"></a>\_Messaggio NEXTDLGCTL WM

Inviato a una procedura della finestra di dialogo per impostare lo stato attivo su un altro controllo nella finestra di dialogo.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Se *lParam* è **true**, questo parametro identifica il controllo che riceve lo stato attivo. Se *lParam* è **false**, questo parametro indica se il controllo successivo o precedente con lo stile **WS \_ TABSTOP** riceve lo stato attivo. Se *wParam* è zero, il controllo successivo riceve lo stato attivo; in caso contrario, il controllo precedente con lo stile **WS \_ TABSTOP** riceve lo stato attivo.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa indica il modo in cui il sistema usa *wParam*. Se la parola di ordine inferiore è **true**, *wParam* è un handle associato al controllo che riceve lo stato attivo; in caso contrario, *wParam* è un flag che indica se il controllo successivo o precedente con lo stile **WS \_ TABSTOP** riceve lo stato attivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Questo messaggio esegue ulteriori operazioni di gestione della finestra di dialogo oltre a quelle eseguite dalla funzione di [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** aggiorna il bordo predefinito del pulsante, imposta l'identificatore di controllo predefinito e seleziona automaticamente il testo di un controllo di modifica (se la finestra di destinazione è un controllo di modifica).

Non utilizzare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per inviare un messaggio **WM \_ NEXTDLGCTL** se l'applicazione elaborerà simultaneamente altri messaggi che impostano lo stato attivo. Usare invece la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

