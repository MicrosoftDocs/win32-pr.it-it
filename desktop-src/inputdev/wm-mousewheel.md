---
title: Messaggio WM_MOUSEWHEEL (winuser. h)
description: Inviato alla finestra con lo stato attivo quando la rotellina del mouse viene ruotata.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Input della tastiera e del mouse WM_MOUSEWHEEL messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301423"
---
# <a name="wm_mousewheel-message"></a>Messaggio di WM \_ MOUSEWHEEL

Inviato alla finestra con lo stato attivo quando la rotellina del mouse viene ruotata. La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga il messaggio all'elemento padre della finestra. Non devono essere presenti inoltri interni del messaggio, poiché **DefWindowProc** lo propaga alla catena padre fino a quando non trova una finestra che la elabora.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più ordinata indica la distanza con cui la rotellina viene ruotata, espressa in multipli o divisioni di **\_ Delta della rotella**, ovvero 120. Un valore positivo indica che la rotellina è stata ruotata in orizzontale, lontano dall'utente; un valore negativo indica che la rotellina è stata ruotata indietro verso l'utente.

La parola più bassa indica se le varie chiavi virtuali sono inattive. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0x0008</dt> di controllo </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON </dl>    | Il pulsante sinistro del mouse è premuto.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON </dl>    | Il pulsante centrale del mouse è inattivo.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON </dl>    | Il pulsante destro del mouse è inattivo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1 </dl> | Il primo pulsante X è inattivo.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2 </dl> | Il secondo pulsante X è inattivo.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la coordinata x del puntatore, relativa all'angolo superiore sinistro dello schermo.

La parola più significativa specifica la coordinata y del puntatore, relativa all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere le informazioni nel parametro *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi. I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.

 

La rotazione della rotellina sarà un multiplo del **\_ Delta della rotellina**, che viene impostato su 120. Si tratta della soglia per l'azione da intraprendere e una di queste azioni, ad esempio lo scorrimento di un incremento, deve verificarsi per ogni Delta.

Il Delta è stato impostato su 120 per consentire a Microsoft o altri fornitori di creare ruote a risoluzione più fine, ovvero una rotellina a rotazione libera senza tacche, per inviare più messaggi per rotazione, ma con un valore inferiore in ogni messaggio. Per usare questa funzionalità, è possibile aggiungere i valori Delta in entrata fino a raggiungere il **\_ Delta della rotella** (pertanto, per una rotazione delta si ottiene la stessa risposta) o scorrere righe parziali in risposta ai messaggi più frequenti. È anche possibile scegliere la granularità di scorrimento e accumulare delta fino a quando non viene raggiunto.

Si noti che non esiste alcun *fwKeys* per **MSH \_ MOUSEWHEEL**. In caso contrario, i parametri sono esattamente uguali a quelli per **WM \_ MOUSEWHEEL**.

È possibile che l'applicazione inoltri **MSH \_ MOUSEWHEEL** a tutti gli oggetti o controlli incorporati. L'applicazione è necessaria per inviare il messaggio a un'applicazione OLE incorporata attiva. È facoltativo che l'applicazione lo invii a un controllo abilitato per la rotellina con lo stato attivo. Se l'applicazione invia il messaggio a un controllo, può controllare il valore restituito per verificare se il messaggio è stato elaborato. I controlli sono necessari per restituire un valore **true** se elaborano il messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**OTTENERE \_ lo stato di un \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**OTTENERE \_ la \_ Delta del cerchio \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_evento mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**PUNTI**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

