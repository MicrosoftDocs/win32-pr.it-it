---
title: Codice di notifica di WM_VSCROLL (TrackBar) (winuser. h)
description: Il \_ messaggio WM VSCROLL viene inviato al proprietario di un controllo TrackBar verticale quando il dispositivo di scorrimento cambia posizione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Codice di notifica di WM_VSCROLL (TrackBar)-controlli Windows
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
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120262"
---
# <a name="wm_vscroll-trackbar-notification-code"></a>Codice di notifica di WM \_ VSCROLL (TrackBar)

Il messaggio **WM \_ VSCROLL** viene inviato al proprietario di un controllo TrackBar verticale quando il dispositivo di scorrimento cambia posizione.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente del dispositivo di scorrimento se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è TB \_ THUMBPOSITION o TB \_ THUMBTRACK. Per tutti gli altri codici di notifica, la parola più ordinata è zero; inviare il messaggio [**TBM \_ GETPOS**](tbm-getpos.md) per determinare la posizione del dispositivo di scorrimento.

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica un codice di notifica che indica l'interazione dell'utente con il TrackBar. Questa parola può essere uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB in \_ basso**</dt> </dl>                      | L'utente ha premuto il tasto fine ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | Il TrackBar ha ricevuto [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), vale a dire che l'utente ha rilasciato una chiave che ha inviato un codice di chiave virtuale pertinente. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB \_ LINEDOWN**</dt> </dl>                | L'utente ha premuto il tasto freccia destra ([**VK a \_ destra**](/windows/desktop/inputdev/virtual-key-codes)) o freccia giù ([**VK in \_ basso**](/windows/desktop/inputdev/virtual-key-codes)).<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**\_lineup TB**</dt> </dl>                      | L'utente ha premuto il tasto freccia sinistra ([**VK a \_ sinistra**](/windows/desktop/inputdev/virtual-key-codes)) o freccia su ([**VK \_ in alto**](/windows/desktop/inputdev/virtual-key-codes)).<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PGGIÙ**</dt> </dl>                | L'utente ha fatto clic sul canale sotto o a destra del dispositivo di scorrimento ([**VK \_ Avanti**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB \_ PAGEUP**</dt> </dl>                      | L'utente ha fatto clic sul canale sopra o a sinistra del dispositivo di scorrimento ([**VK \_ precedente**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB \_ THUMBPOSITION**</dt> </dl> | Il TrackBar ha ricevuto [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) dopo un \_ codice di notifica THUMBTRACK TB.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB \_ THUMBTRACK**</dt> </dl>          | L'utente ha trascinato il dispositivo di scorrimento.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ superiore**</dt> </dl>                               | L'utente ha premuto il tasto HOME ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il \_ codice THUMBTRACK TB viene in genere usato dalle applicazioni che forniscono commenti e suggerimenti quando l'utente trascina la casella di scorrimento.

Si noti che il messaggio **WM \_ VSCROLL** contiene solo 16 bit di dati sulla posizione. Pertanto, le applicazioni che si basano esclusivamente su **WM \_ VSCROLL** (e [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) per i dati della posizione del dispositivo di scorrimento hanno un valore di posizione massimo pratica di 65.535.

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

[**\_HSCROLL WM**](wm-hscroll--trackbar-.md)
</dt> </dl>

 

