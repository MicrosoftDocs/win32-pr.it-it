---
description: Inviato quando un utente esegue un gesto di penna. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Messaggio WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226046"
---
# <a name="wm_tablet_flick-message"></a>\_Messaggio di \_ scorrimento rapido del Tablet WM

Inviato quando un utente esegue un gesto di penna. Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Una [**\_ struttura di dati di scorrimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) che contiene informazioni sul Flick della penna che si è verificato.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Struttura del \_ punto di scorrimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) che specifica la posizione in cui si è verificato il tocco di penna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un gesto rapido con penna è un movimento di penna unidirezionale che richiede all'utente di contattare il digitalizzatore in un movimento rapido e semplice. Un gesto rapido è caratterizzato da alta velocità e da un elevato grado di unidritità. Un gesto rapido viene identificato in base alla direzione. I gesti rapidi possono essere eseguiti in otto direzioni corrispondenti alle direzioni Cardinal e secondaria della bussola.

Quando si verifica un gesto rapido penna, Windows invia prima di tutto una notifica a un'applicazione inviando un messaggio di **\_ \_ scorrimento rapido del Tablet WM** , che una finestra riceve tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Restituisce la **costante \_ \_ \_ maschera gestita WM di scorrimento** , descritta in [costanti rapide](flicks-constants.md), per indicare che l'applicazione ha risposto al messaggio di **\_ \_ scorrimento rapido del Tablet WM** . Se l'applicazione non restituisce la **\_ \_ \_ maschera gestita di Flick WM**, Windows esegue l'azione predefinita specificata nel pannello di controllo Flicks inviando una notifica di completamento, ad esempio [**WM \_ APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM \_ VSCROLL**](../controls/wm-vscroll.md)o [**WM \_ KeyDown**](../inputdev/wm-keydown.md), a seconda dell'azione associata al gesto rapido della penna.

Prestare attenzione quando si gestisce il messaggio di **\_ \_ scorrimento rapido del Tablet WM** . **WM \_ Il TABLET \_ Flick** viene passato tramite la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Se si chiamano metodi su un'interfaccia COM, tale oggetto deve trovarsi all'interno dello stesso processo. In caso contrario, COM genera un'eccezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Scorri la \_ struttura dei dati**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**\_messaggio di \_ scorrimento rapido del Tablet WM**](wm-tablet-flick-message.md)
</dt> <dt>

[movimenti rapidi](flicks-gestures.md)
</dt> <dt>

[risposta ai gesti rapidi della penna](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
