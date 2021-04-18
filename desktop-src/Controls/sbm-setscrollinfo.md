---
title: Messaggio SBM_SETSCROLLINFO (winuser. h)
description: Il \_ messaggio SETSCROLLINFO SBM viene inviato per impostare i parametri di una barra di scorrimento.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- Controlli di Windows Message SBM_SETSCROLLINFO
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302128"
---
# <a name="sbm_setscrollinfo-message"></a>\_Messaggio SETSCROLLINFO SBM

Il **messaggio \_ SETSCROLLINFO SBM** viene inviato per impostare i parametri di una barra di scorrimento.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollInfo** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se la barra di scorrimento viene ridisegnato per riflettere la nuova posizione della casella di scorrimento. Se questo parametro è **true**, la barra di scorrimento viene ridisegnato. Se è **false**, la barra di scorrimento non viene ridisegnato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Prima di chiamare [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), impostare il membro **cbSize** della struttura su **sizeof**(**ScrollInfo**), impostare il membro **fmask** per indicare i parametri da impostare e specificare i nuovi valori dei parametri nei membri appropriati.

Il membro **fmask** può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                           | Significato                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL sif**</dt> </dl> | Disabilita la barra di scorrimento anziché rimuoverla, se i nuovi parametri della barra di scorrimento rendono superflua la barra di scorrimento.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_pagina sif**</dt> </dl>                                  | Imposta la pagina di scorrimento sul valore specificato nel membro **nPage** .<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ pos**</dt> </dl>                                     | Imposta la posizione di scorrimento sul valore specificato nel membro **nPos** . <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**\_intervallo sif**</dt> </dl>                               | Imposta l'intervallo di scorrimento sul valore specificato nei membri **nmin** e **nmax** . <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la posizione corrente della casella di scorrimento.

## <a name="remarks"></a>Commenti

I messaggi che indicano la posizione della barra di scorrimento, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md), forniscono solo 16 bit di dati sulla posizione. Tuttavia, la struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usata da [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornisce 32 bit dei dati relativi alla posizione della barra di scorrimento. È possibile usare questi messaggi e funzioni durante l'elaborazione dei messaggi **WM \_ HSCROLL** o **WM \_ VSCROLL** per ottenere i dati relativi alla posizione della barra di scorrimento a 32 bit.

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

[**\_GETSCROLLINFO SBM**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

