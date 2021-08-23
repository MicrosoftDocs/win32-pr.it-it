---
title: WM_VSCROLL messaggio (Winuser.h)
description: Il messaggio WM VSCROLL viene inviato a una finestra quando si verifica un evento di scorrimento nella barra di scorrimento \_ verticale standard della finestra.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbb87f63cb0f4801787be1f2cb23b321470b1053a58b13d0f3eea34112b1341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636711"
---
# <a name="wm_vscroll-message"></a>Messaggio \_ VSCROLL WM

Il **messaggio \_ WM VSCROLL** viene inviato a una finestra quando si verifica un evento di scorrimento nella barra di scorrimento verticale standard della finestra. Questo messaggio viene inviato anche al proprietario di un controllo barra di scorrimento verticale quando si verifica un evento di scorrimento nel controllo.

Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posizione corrente della casella di scorrimento se [**il valore LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è SB THUMBPOSITION o \_ SB THUMBTRACK. In caso contrario, questa \_ parola non viene usata.

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica un valore della barra di scorrimento che indica la richiesta di scorrimento dell'utente. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ BOTTOM**</dt> </dl>                      | Scorre verso l'angolo inferiore destro.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | Termina lo scorrimento.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | Scorre una riga verso il basso.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> </dl>                      | Scorre una riga verso l'alto.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl>                | Scorre una pagina verso il basso.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> </dl>                      | Scorre di una pagina verso l'alto.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | L'utente ha trascinato la casella di scorrimento (thumb) e rilasciato il pulsante del mouse. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posizione della casella di scorrimento alla fine dell'operazione di trascinamento.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | L'utente sta trascinando la casella di scorrimento. Questo messaggio viene inviato ripetutamente fino a quando l'utente non rilascia il pulsante del mouse. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posizione in cui è stata trascinata la casella di scorrimento.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> </dl>                               | Scorre verso l'alto a sinistra.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Se il messaggio viene inviato da un controllo barra di scorrimento, questo parametro è l'handle per il controllo barra di scorrimento. Se il messaggio viene inviato da una barra di scorrimento standard, questo parametro è **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il codice della richiesta THUMBTRACK SB viene in genere usato dalle applicazioni che forniscono commenti e suggerimenti quando l'utente \_ trascina la casella di scorrimento.

Se un'applicazione scorre il contenuto della finestra, deve anche reimpostare la posizione della casella di scorrimento usando la [**funzione SetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)

Si noti che il **messaggio WM \_ VSCROLL** contiene solo 16 bit di dati sulla posizione della casella di scorrimento. Di conseguenza, le applicazioni che si basano esclusivamente su **WM \_ VSCROLL** (e [**WM \_ HSCROLL**](wm-hscroll.md)) per i dati sulla posizione di scorrimento hanno un valore pratico di posizione massima di 65.535.

Tuttavia, poiché le funzioni [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)e [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) supportano i dati di posizione della barra di scorrimento a 32 bit, è possibile aggirare la barriera a 16 bit dei messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e **WM \_ VSCROLL.** Per una descrizione della tecnica, vedere **GetScrollInfo.**

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

[**WM \_ HSCROLL**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (Trackbar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

