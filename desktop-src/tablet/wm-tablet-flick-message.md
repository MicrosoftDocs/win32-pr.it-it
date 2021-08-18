---
description: Inviato quando un utente esegue un gesto rapido della penna. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: WM_TABLET_FLICK messaggio (Tpcshrd.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb01fce646d2e7c6cb4e1b25c2f49f0c4dde5258ba2167e117a23eff22a5d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842777"
---
# <a name="wm_tablet_flick-message"></a>MESSAGGIO WM \_ TABLET \_ FLICK

Inviato quando un utente esegue un gesto rapido della penna. Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Struttura [**FLICK DATA che \_ contiene**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) informazioni sul gesto rapido della penna che si è verificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FLICK POINT che specifica \_ dove**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) si è verificato il gesto rapido della penna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un tocco con penna è un movimento di penna unidirezionale che richiede all'utente di contattare il digitalizzatore con un movimento rapido e diretto. Un gesto rapido è caratterizzato da velocità elevata e un elevato grado di rettezza. Un gesto rapido è identificato dalla direzione. È possibile eseguire i gesti rapidi in otto direzioni corrispondenti alle direzioni della bussola cardinale e secondaria.

Quando si verifica un gesto rapido con penna, Windows invia prima una notifica a un'applicazione inviando un messaggio **WM \_ TABLET \_ FLICK** che una finestra riceve tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Restituisce la **costante FLICK \_ WM \_ HANDLED \_ MASK,** descritta in [Costanti di Flicks,](flicks-constants.md)per indicare che l'applicazione ha risposto al messaggio **WM TABLET \_ \_ FLICK.** Se l'applicazione non restituisce **FLICK \_ WM \_ HANDLED \_ MASK,** Windows esegue l'azione predefinita specificata nel pannello di controllo dei gesti rapidi inviando una notifica di follow-up, ad esempio [**WM \_ APPCOMMAND,**](../inputdev/wm-appcommand.md) [**WM \_ VSCROLL**](../controls/wm-vscroll.md)o [**WM \_ KEYDOWN,**](../inputdev/wm-keydown.md)a seconda dell'azione associata al movimento della penna.

Prestare attenzione quando si gestisce il **messaggio WM \_ TABLET \_ FLICK.** **WM \_ TABLET \_ FLICK** viene passato tramite la [**funzione SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) Se si chiamano metodi su un'interfaccia COM, tale oggetto deve essere all'interno dello stesso processo. In caso contrario, COM genera un'eccezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Tpcshrd.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Struttura dei \_ dati di tipo sfarfallio**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**wm \_ tablet \_ flick message**](wm-tablet-flick-message.md)
</dt> <dt>

[gesti rapidi](flicks-gestures.md)
</dt> <dt>

[risposta ai gesti rapidi della penna](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
