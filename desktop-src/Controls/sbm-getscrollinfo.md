---
title: SBM_GETSCROLLINFO messaggio (Winuser.h)
description: Il messaggio SBM \_ GETSCROLLINFO viene inviato per recuperare i parametri di una barra di scorrimento.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fde18fe30e9d944e547305094e7ea69e6745d4e1e112d8697367cd82833588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919471"
---
# <a name="sbm_getscrollinfo-message"></a>Messaggio SBM \_ GETSCROLLINFO

Il **messaggio SBM \_ GETSCROLLINFO** viene inviato per recuperare i parametri di una barra di scorrimento.

Le applicazioni non devono inviare questo messaggio direttamente. In alternativa, devono usare la [**funzione GetScrollInfo.**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi perché la **funzione GetScrollInfo** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Prima di [**chiamare GetScrollInfo,**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)impostare il membro **cbSize** della struttura su **sizeof**(**SCROLLINFO**) e impostare il membro **fMask** per specificare i parametri della barra di scorrimento da recuperare. Prima della restituzione, il messaggio copia i parametri specificati nei membri appropriati della struttura .

Il **membro fMask** può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                      | Significato                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ ALL**</dt> </dl>                | Combinazione di SIF \_ PAGE, SIF \_ POS, SIF \_ RANGE e SIF \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**PAGINA \_ SIF**</dt> </dl>             | Copia la pagina di scorrimento nel membro nPage.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                | Copia la posizione di scorrimento nel membro nPos. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**INTERVALLO \_ SIF**</dt> </dl>          | Copia l'intervallo di scorrimento nei membri nMin e nMax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**SIF \_ TRACKPOS**</dt> </dl> | Copia la posizione di rilevamento della casella di scorrimento corrente nel membro nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha recuperato valori, il valore restituito è **TRUE.** in caso contrario, è **FALSE.**

## <a name="remarks"></a>Commenti

I messaggi che indicano la posizione della barra di scorrimento, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL,**](wm-vscroll.md)forniscono solo 16 bit di dati di posizione. Tuttavia, la struttura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usata da **SBM \_ GETSCROLLINFO,** [**SBM \_ SETSCROLLINFO,**](sbm-setscrollinfo.md) [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornisce 32 bit di dati sulla posizione della barra di scorrimento. È possibile usare questi messaggi e funzioni durante l'elaborazione dei messaggi **WM \_ HSCROLL** o **WM \_ VSCROLL** per ottenere dati sulla posizione della barra di scorrimento a 32 bit.

Per ottenere la posizione a 32 bit della casella di scorrimento (thumb) durante un codice di richiesta SB THUMBTRACK in un messaggio \_ [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL,**](wm-vscroll.md) inviare **SBM \_ GETSCROLLINFO** con il valore SIF TRACKPOS nel membro \_ **fMask** della struttura [**SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Il messaggio restituisce la posizione di rilevamento della casella di scorrimento nel **membro nTrackPos** della **struttura SCROLLINFO.** In questo modo è possibile ottenere la posizione della casella di scorrimento quando l'utente la sposta. In alternativa, è possibile usare la [**funzione GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) per ottenere le stesse informazioni.

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

[**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

