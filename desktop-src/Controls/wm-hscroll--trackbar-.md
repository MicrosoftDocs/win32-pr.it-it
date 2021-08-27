---
title: WM_HSCROLL di notifica (Trackbar) (Winuser.h)
description: Il messaggio WM HSCROLL viene inviato al proprietario di un controllo \_ trackbar orizzontale quando il dispositivo di scorrimento cambia posizione. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- WM_HSCROLL di notifica (Trackbar) Windows controlli
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
ms.openlocfilehash: 5a21000f9eeeb3ff83d4fb65456b21447aa3fd604412f3b4d6d3b94fda58606b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059311"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>Codice \_ di notifica WM HSCROLL (Trackbar)

Il **messaggio WM \_ HSCROLL** viene inviato al proprietario di un controllo trackbar orizzontale quando il dispositivo di scorrimento cambia posizione.

Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posizione corrente del dispositivo di scorrimento se [**il valore LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è TB \_ THUMBPOSITION o TB \_ THUMBTRACK. Per tutti gli altri codici di notifica, la parola di ordine elevato è zero. inviare il [**messaggio \_ GETPOS TBM**](tbm-getpos.md) per determinare la posizione del dispositivo di scorrimento.

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica un codice di notifica che indica l'interazione dell'utente con il trackbar. Questa parola può essere uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ INFERIORE**</dt> </dl>                      | L'utente ha premuto il tasto END ([**VK \_ END**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | Il trackbar ha ricevuto [**WM \_ KEYUP,**](/windows/desktop/inputdev/wm-keyup)ovvero l'utente ha rilasciato una chiave che ha inviato un codice chiave virtuale pertinente. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB \_ LINEDOWN**</dt> </dl>                | L'utente ha premuto il tasto FRECCIA DESTRA ([**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) o FRECCIA GIÙ ([**VK \_ DOWN).**](/windows/desktop/inputdev/virtual-key-codes)<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**TB \_ LINEUP**</dt> </dl>                      | L'utente ha premuto il tasto FRECCIA SINISTRA ([**VK \_ SINISTRA**](/windows/desktop/inputdev/virtual-key-codes)) o FRECCIA SU ([**VK \_ SU).**](/windows/desktop/inputdev/virtual-key-codes)<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PAGEDOWN**</dt> </dl>                | L'utente ha fatto clic sul canale sotto o a destra del dispositivo di scorrimento ([**VK \_ NEXT**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB \_ PAGEUP**</dt> </dl>                      | L'utente ha fatto clic sul canale sopra o a sinistra del dispositivo di scorrimento ([**VK \_ PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB \_ THUMBPOSITION**</dt> </dl> | Il trackbar ha ricevuto [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) in seguito a un codice \_ di notifica THUMBTRACK da TB.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB \_ THUMBTRACK**</dt> </dl>          | L'utente ha trascinato il dispositivo di scorrimento.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ TOP**</dt> </dl>                               | L'utente ha premuto il tasto HOME ([**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo trackbar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il codice THUMBTRACK tb viene in genere usato dalle applicazioni che forniscono commenti e suggerimenti quando l'utente \_ trascina la casella di scorrimento.

Si noti che **il messaggio \_ WM HSCROLL** contiene solo 16 bit di dati di posizione. Di conseguenza, le applicazioni che si basano esclusivamente su **WM \_ HSCROLL** (e [**WM \_ VSCROLL)**](wm-vscroll--trackbar-.md)per i dati di posizione del dispositivo di scorrimento hanno un valore pratico di posizione massima di 65.535.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

