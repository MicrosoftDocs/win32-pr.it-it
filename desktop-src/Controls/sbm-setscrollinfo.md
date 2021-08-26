---
title: SBM_SETSCROLLINFO messaggio (Winuser.h)
description: Il messaggio SBM \_ SETSCROLLINFO viene inviato per impostare i parametri di una barra di scorrimento.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO di controllo Windows messaggio
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
ms.openlocfilehash: 5622371abb86301e1450c9fa0d6864e8db76c9837fca48fe8bcf11cb884f6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914291"
---
# <a name="sbm_setscrollinfo-message"></a>Messaggio SBM \_ SETSCROLLINFO

Il **messaggio SBM \_ SETSCROLLINFO** viene inviato per impostare i parametri di una barra di scorrimento.

Le applicazioni non devono inviare questo messaggio direttamente. Devono invece usare la [**funzione SetScrollInfo.**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi perché la **funzione SetScrollInfo** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se la barra di scorrimento viene ridisegnata per riflettere la nuova posizione della casella di scorrimento. Se questo parametro è **TRUE,** la barra di scorrimento viene ridisegnata. Se è **FALSE,** la barra di scorrimento non viene ridisegnata.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Prima di chiamare [**SetScrollInfo,**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)impostare il membro **cbSize** della struttura su **sizeof**(**SCROLLINFO**), impostare il membro **fMask** per indicare i parametri da impostare e specificare i nuovi valori dei parametri nei membri appropriati.

Il **membro fMask** può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                           | Significato                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**SIF \_ DISABLENOSCROLL**</dt> </dl> | Disabilita la barra di scorrimento invece di rimuoverla, se i nuovi parametri della barra di scorrimento rendono la barra di scorrimento superflua.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**PAGINA \_ SIF**</dt> </dl>                                  | Imposta la pagina di scorrimento sul valore specificato nel **membro nPage.**<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                                     | Imposta la posizione di scorrimento sul valore specificato nel **membro nPos.** <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**INTERVALLO \_ SIF**</dt> </dl>                               | Imposta l'intervallo di scorrimento sul valore specificato nei membri **nMin** **e nMax.** <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la posizione corrente della casella di scorrimento.

## <a name="remarks"></a>Commenti

I messaggi che indicano la posizione della barra di scorrimento, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL,**](wm-vscroll.md)forniscono solo 16 bit di dati di posizione. Tuttavia, la struttura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usata da [**SBM \_ GETSCROLLINFO,**](sbm-getscrollinfo.md) **SBM \_ SETSCROLLINFO,** [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornisce 32 bit di dati sulla posizione della barra di scorrimento. È possibile usare questi messaggi e funzioni durante l'elaborazione dei messaggi **WM \_ HSCROLL** o **WM \_ VSCROLL** per ottenere dati sulla posizione della barra di scorrimento a 32 bit.

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

[**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

