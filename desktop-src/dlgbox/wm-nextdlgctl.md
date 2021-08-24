---
title: WM_NEXTDLGCTL messaggio (Winuser.h)
description: Inviato a una routine della finestra di dialogo per impostare lo stato attivo della tastiera su un controllo diverso nella finestra di dialogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL finestre di dialogo del messaggio
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
ms.openlocfilehash: 1a14de889e614aaba28757716326bcd1cf843aed64fe2dc58ca86430d65db628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606221"
---
# <a name="wm_nextdlgctl-message"></a>Messaggio WM \_ NEXTDLGCTL

Inviato a una routine della finestra di dialogo per impostare lo stato attivo della tastiera su un controllo diverso nella finestra di dialogo.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Se *lParam* è **TRUE,** questo parametro identifica il controllo che riceve lo stato attivo. Se *lParam* è **FALSE,** questo parametro indica se il controllo successivo o precedente con lo **stile \_ WS TABSTOP** riceve lo stato attivo. Se *wParam* è zero, il controllo successivo riceve lo stato attivo. In caso contrario, il controllo precedente con lo **stile \_ WS TABSTOP** riceve lo stato attivo.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso indica il modo in cui il sistema usa *wParam*. Se la parola di ordine basso è **TRUE,** *wParam* è un handle associato al controllo che riceve lo stato attivo. in caso contrario, *wParam* è un flag che indica se il controllo successivo o precedente con lo **stile \_ WS TABSTOP** riceve lo stato attivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Questo messaggio esegue altre operazioni di gestione delle finestre di dialogo oltre a quelle eseguite dalla funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** aggiorna il bordo predefinito del pulsante, imposta l'identificatore di controllo predefinito e seleziona automaticamente il testo di un controllo di modifica (se la finestra di destinazione è un controllo di modifica).

Non usare la [**funzione SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per inviare un messaggio **WM \_ NEXTDLGCTL** se l'applicazione eelaborare contemporaneamente altri messaggi che impostano lo stato attivo. Usare invece [**la funzione PostMessage.**](/windows/desktop/api/winuser/nf-winuser-postmessagea)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**Setfocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

