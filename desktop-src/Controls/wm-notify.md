---
title: Messaggio WM_NOTIFY (winuser. h)
description: Inviato da un controllo comune alla relativa finestra padre quando si verifica un evento oppure il controllo richiede alcune informazioni.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Controlli di Windows Message WM_NOTIFY
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964463"
---
# <a name="wm_notify-message"></a>\_Messaggio di notifica WM

Inviato da un controllo comune alla relativa finestra padre quando si verifica un evento oppure il controllo richiede alcune informazioni.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del controllo comune che invia il messaggio. Questo identificatore non è necessariamente univoco. Per identificare il controllo, un'applicazione deve usare il membro **hwndFrom** o **IdFrom** della struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , passata come parametro *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene il codice di notifica e informazioni aggiuntive. Per alcuni messaggi di notifica, questo parametro punta a una struttura più ampia con la struttura **NMHDR** come primo membro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato tranne che per i messaggi di notifica che specificano in caso contrario.

## <a name="remarks"></a>Commenti

La destinazione del messaggio deve essere **HWND** dell'elemento padre del controllo. Questo valore può essere ottenuto tramite [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), come illustrato nell'esempio seguente, dove *m \_ controlHwnd* è l' **HWND** del controllo stesso.


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



Le applicazioni gestiscono il messaggio nella procedura della finestra padre, come illustrato nell'esempio seguente, che gestisce il messaggio di notifica inviato dal controllo personalizzato nell'esempio precedente.


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



Alcune notifiche, principalmente quelle che sono state nell'API per molto tempo, vengono inviate come messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . Per ulteriori informazioni, vedere [Control Messages](control-messages.md).

Se il gestore di messaggi si trova in una routine della finestra di dialogo, è necessario utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT per impostare un valore restituito.

Per i sistemi Windows Vista e versioni successive, non è possibile inviare il messaggio di **\_ notifica WM** tra i processi.

Molte notifiche sono disponibili nei formati ANSI e Unicode. La finestra che invia il messaggio di **\_ notifica WM** usa il messaggio [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) per determinare il formato da usare. Per ulteriori informazioni, vedere **WM \_ NOTIFYFORMAT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_NOTIFYFORMAT WM**](wm-notifyformat.md)
</dt> </dl>

 

