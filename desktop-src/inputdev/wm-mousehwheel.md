---
title: WM_MOUSEHWHEEL messaggio (Winuser.h)
description: Inviato alla finestra attiva quando la rotellina di scorrimento orizzontale del mouse viene inclinata o ruotata.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- WM_MOUSEHWHEEL messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de63d214d087cb804c3973fbba6a90c46955506ebddf5da57a7578d224edb803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451491"
---
# <a name="wm_mousehwheel-message"></a>Messaggio \_ WM MOUSEHWHEEL

Inviato alla finestra attiva quando la rotellina di scorrimento orizzontale del mouse viene inclinata o ruotata. La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga il messaggio all'elemento padre della finestra. Non deve essere presente alcun inoltro interno del messaggio, perché **DefWindowProc** lo propaga fino alla catena padre finché non trova una finestra che lo elabora.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine superiore indica la distanza di rotazione della ruota, espressa in multipli o fattori di **WHEEL \_ DELTA,** che è impostata su 120. Un valore positivo indica che la rotellina è stata ruotata a destra; un valore negativo indica che la rotellina è stata ruotata a sinistra.

La parola meno in ordine indica se varie chiavi virtuali non sono disponibili. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Controllo**</dt> <dt>0x0008</dt> </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Il pulsante sinistro del mouse è in basso.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Il pulsante centrale del mouse è in basso.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Il pulsante destro del mouse è in basso.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Il primo pulsante X è in basso.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Il secondo pulsante X è in basso.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la coordinata x dell'indicatore di misura rispetto all'angolo superiore sinistro dello schermo.

La parola più alta specifica la coordinata y dell'indicatore di misura rispetto all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere le informazioni nel *parametro wParam.*


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Usare il codice seguente per ottenere la posizione orizzontale e verticale.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Come indicato in precedenza, la coordinata x si trova nell'ordine più basso **del** valore restituito. La coordinata y si trova nell'ordine  più breve **(entrambi** rappresentano valori con segno perché possono assumere valori negativi nei sistemi con più monitor). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. È anche possibile usare la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre la coordinata x o y.

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

La rotazione della ruota è un multiplo di **WHEEL \_ DELTA,** impostato su 120. Questa è la soglia per l'azione da eseguire e una di queste azioni (ad esempio, lo scorrimento di un incremento) deve verificarsi per ogni delta.

Il delta è stato impostato su 120 per consentire a Microsoft o ad altri fornitori di creare ruote con risoluzione più fine (ad esempio, una ruota a rotazione libera senza punti) per inviare più messaggi per rotazione, ma con un valore inferiore in ogni messaggio. Per usare questa funzionalità, è possibile aggiungere i valori delta in ingresso fino a quando non viene raggiunto **WHEEL \_ DELTA** (in modo che per una rotazione delta si otterrà la stessa risposta) o scorrere righe parziali in risposta a messaggi più frequenti. È anche possibile scegliere la granularità di scorrimento e accumulare delta fino a quando non viene raggiunto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GET \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GET \_ WHEEL \_ DELTA \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**evento \_ mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**PUNTI DI APPLICAZIONE**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**Systemparametersinfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

