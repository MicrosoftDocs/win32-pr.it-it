---
title: Messaggio WM_HSCROLL (winuser. h)
description: Il \_ messaggio WM HSCROLL viene inviato a una finestra quando si verifica un evento Scroll nella barra di scorrimento orizzontale standard della finestra.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- Controlli di Windows Message WM_HSCROLL
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120266"
---
# <a name="wm_hscroll-message"></a>\_Messaggio HSCROLL WM

Il messaggio **WM \_ HSCROLL** viene inviato a una finestra quando si verifica un evento Scroll nella barra di scorrimento orizzontale standard della finestra. Questo messaggio viene inoltre inviato al proprietario di un controllo barra di scorrimento orizzontale quando si verifica un evento di scorrimento nel controllo.

Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente della casella di scorrimento se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è SB \_ THUMBPOSITION o SB THUMBTRACK. \_ in caso contrario, la parola non viene utilizzata.

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica un valore della barra di scorrimento che indica la richiesta di scorrimento dell'utente. Questa parola può essere uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**\_ENDSCROLL SB**</dt> </dl>             | Termina lo scorrimento.<br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB a \_ sinistra**</dt> </dl>                            | Scorre l'angolo in alto a sinistra.<br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB a \_ destra**</dt> </dl>                         | Scorre verso destra in basso.<br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**\_LINELEFT SB**</dt> </dl>                | Scorre verso sinistra di un'unità.<br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**\_LINERIGHT SB**</dt> </dl>             | Scorre verso destra di un'unità.<br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**\_PAGELEFT SB**</dt> </dl>                | Scorre verso sinistra in base alla larghezza della finestra.<br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**\_PAGERIGHT SB**</dt> </dl>             | Scorre verso destra in base alla larghezza della finestra.<br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**\_THUMBPOSITION SB**</dt> </dl> | L'utente ha trascinato la casella di scorrimento (Thumb) e ha rilasciato il pulsante del mouse. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posizione della casella di scorrimento alla fine dell'operazione di trascinamento.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**\_THUMBTRACK SB**</dt> </dl>          | L'utente sta trascinando la casella di scorrimento. Questo messaggio viene inviato ripetutamente fino a quando l'utente rilascia il pulsante del mouse. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posizione in cui è stata trascinata la casella di scorrimento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Se il messaggio viene inviato da un controllo barra di scorrimento, questo parametro è l'handle per il controllo barra di scorrimento. Se il messaggio viene inviato da una barra di scorrimento standard, questo parametro è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il \_ codice di richiesta SB THUMBTRACK viene in genere usato dalle applicazioni che forniscono commenti e suggerimenti quando l'utente trascina la casella di scorrimento.

Se un'applicazione scorre il contenuto della finestra, è necessario reimpostare anche la posizione della casella di scorrimento usando la funzione [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Si noti che il messaggio **WM \_ HSCROLL** contiene solo 16 bit di dati di posizione della casella di scorrimento. Di conseguenza, le applicazioni che si basano esclusivamente su **WM \_ HSCROLL** (e [**WM \_ VSCROLL**](wm-vscroll.md)) per i dati della posizione di scorrimento hanno un valore di posizione massimo pratica pari a 65.535.

Tuttavia, poiché le funzioni [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)e [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) supportano i dati di posizione della barra di scorrimento a 32 bit, è possibile aggirare la barriera a 16 bit dei messaggi **WM \_ HSCROLL** e [**WM \_ VSCROLL**](wm-vscroll.md) . Per una descrizione della tecnica, vedere **GetScrollInfo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**\_HSCROLL WM (TrackBar)**](wm-hscroll--trackbar-.md)
</dt> <dt>

[**\_VSCROLL WM**](wm-vscroll.md)
</dt> </dl>

 

