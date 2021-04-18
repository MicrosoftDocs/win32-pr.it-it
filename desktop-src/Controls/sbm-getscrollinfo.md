---
title: Messaggio SBM_GETSCROLLINFO (winuser. h)
description: Il \_ messaggio GETSCROLLINFO SBM viene inviato per recuperare i parametri di una barra di scorrimento.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Controlli di Windows Message SBM_GETSCROLLINFO
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
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302640"
---
# <a name="sbm_getscrollinfo-message"></a>\_Messaggio GETSCROLLINFO SBM

Il **messaggio \_ GETSCROLLINFO SBM** viene inviato per recuperare i parametri di una barra di scorrimento.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollInfo** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Prima di chiamare [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), impostare il membro **cbSize** della struttura su **sizeof**(**ScrollInfo**) e impostare il membro **fmask** per specificare i parametri della barra di scorrimento da recuperare. Prima di restituire, il messaggio copia i parametri specificati nei membri appropriati della struttura.

Il membro **fmask** può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                      | Significato                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**\_tutte le sfi**</dt> </dl>                | Combinazione della \_ pagina sif, SIF \_ pos, SIF \_ Range e SIF \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_pagina sif**</dt> </dl>             | Copia la pagina di scorrimento nel membro nPage.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ pos**</dt> </dl>                | Copia la posizione di scorrimento nel membro nPos. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**\_intervallo sif**</dt> </dl>          | Copia l'intervallo di scorrimento nei membri nMin e nMax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**\_TRACKPOS sif**</dt> </dl> | Copia la posizione di rilevamento della casella di scorrimento corrente nel membro nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio recupera tutti i valori, il valore restituito è **true**; in caso contrario, è **false**.

## <a name="remarks"></a>Commenti

I messaggi che indicano la posizione della barra di scorrimento, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md), forniscono solo 16 bit di dati sulla posizione. Tuttavia, la struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usata da **SBM \_ GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornisce 32 bit dei dati relativi alla posizione della barra di scorrimento. È possibile usare questi messaggi e funzioni durante l'elaborazione dei messaggi **WM \_ HSCROLL** o **WM \_ VSCROLL** per ottenere i dati relativi alla posizione della barra di scorrimento a 32 bit.

Per ottenere la posizione a 32 bit della casella di scorrimento (Thumb) durante un \_ codice di richiesta SB THUMBTRACK in un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) , inviare **SBM \_ GETSCROLLINFO** con il \_ valore sif TRACKPOS nel membro **fmask** della struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Il messaggio restituisce la posizione di rilevamento della casella di scorrimento nel membro **nTrackPos** della struttura **ScrollInfo** . Questo consente di ottenere la posizione della casella di scorrimento quando l'utente lo sposta. In alternativa, è possibile usare la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) per ottenere le stesse informazioni.

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

[**\_SETSCROLLINFO SBM**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

