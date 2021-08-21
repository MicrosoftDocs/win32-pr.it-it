---
title: WM_VSCROLL di notifica (Trackbar) (Winuser.h)
description: Il messaggio WM \_ VSCROLL viene inviato al proprietario di un controllo trackbar verticale quando il dispositivo di scorrimento cambia posizione. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- WM_VSCROLL di notifica (Trackbar) Windows controlli
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
ms.openlocfilehash: 0dabd6c3c50588c4a9052b0829473352940f0027a1c12d0f3bbc6334e5f13b08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077655"
---
# <a name="wm_vscroll-trackbar-notification-code"></a>Codice \_ di notifica WM VSCROLL (Trackbar)

Il **messaggio WM \_ VSCROLL** viene inviato al proprietario di un controllo trackbar verticale quando il dispositivo di scorrimento cambia posizione.

Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posizione corrente del dispositivo di scorrimento se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è TB \_ THUMBPOSITION o TB \_ THUMBTRACK. Per tutti gli altri codici di notifica, la parola più importante è zero. inviare il [**messaggio \_ GETPOS TBM**](tbm-getpos.md) per determinare la posizione del dispositivo di scorrimento.

LoWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un codice di notifica che indica l'interazione dell'utente con il trackbar. Questa parola può essere uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ IN BASSO**</dt> </dl>                      | L'utente ha premuto il tasto FINE ([**VK \_ END**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | Il trackbar ha ricevuto [**WM \_ KEYUP,**](/windows/desktop/inputdev/wm-keyup)ovvero l'utente ha rilasciato un tasto che ha inviato un codice chiave virtuale pertinente. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB \_ LINEDOWN**</dt> </dl>                | L'utente ha premuto il tasto FRECCIA DESTRA ([**VK \_ DESTRA**](/windows/desktop/inputdev/virtual-key-codes)) o FRECCIA GIÙ ([**VK \_ GIÙ**](/windows/desktop/inputdev/virtual-key-codes)).<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**TB \_ LINEUP**</dt> </dl>                      | L'utente ha premuto il tasto FRECCIA SINISTRA [**(VK \_ A SINISTRA)**](/windows/desktop/inputdev/virtual-key-codes)o FRECCIA SU [**(VK \_ UP).**](/windows/desktop/inputdev/virtual-key-codes)<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PAGEDOWN**</dt> </dl>                | L'utente ha fatto clic sul canale sotto o a destra del dispositivo di scorrimento [**(VK \_ NEXT).**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB \_ PAGEUP**</dt> </dl>                      | L'utente ha fatto clic sul canale sopra o a sinistra del dispositivo di scorrimento [**(VK \_ PRIOR).**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**POSIZIONE \_ DEL CURSORE DA TB**</dt> </dl> | Il trackbar ha ricevuto [**WM \_ LBUTTONUP dopo**](/windows/desktop/inputdev/wm-lbuttonup) un codice di notifica \_ THUMBTRACK da TB.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**THUMBTRACK \_ DA TB**</dt> </dl>          | L'utente ha trascinato il dispositivo di scorrimento.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ TOP**</dt> </dl>                               | L'utente ha premuto il tasto HOME ([**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo trackbar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il codice \_ THUMBTRACK da tb viene in genere usato dalle applicazioni che forniscono feedback mentre l'utente trascina la casella di scorrimento.

Si noti che **il \_ messaggio WM VSCROLL** contiene solo 16 bit di dati di posizione. Di conseguenza, le applicazioni che si basano esclusivamente su **WM \_ VSCROLL** (e [**WM \_ HSCROLL)**](wm-hscroll--trackbar-.md)per i dati di posizione del dispositivo di scorrimento hanno un valore di posizione massimo pratico di 65.535.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)
</dt> </dl>

 

