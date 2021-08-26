---
description: Inviato a una finestra quando la relativa area non client deve essere modificata per indicare uno stato attivo o inattivo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: WM_NCACTIVATE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095f0cc7f555b4daf80a67a2394e29286f32a49dcba687780e8747f5d1b193fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056001"
---
# <a name="wm_ncactivate-message"></a>Messaggio \_ WM NCACTIVATE

Inviato a una finestra quando la relativa area non client deve essere modificata per indicare uno stato attivo o inattivo.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica quando è necessario modificare una barra del titolo o un'icona per indicare uno stato attivo o inattivo. Se deve essere disegnata una barra del titolo o un'icona attiva, il *parametro wParam* è **TRUE.** Se deve essere disegnata una barra del titolo o un'icona inattiva, *wParam* è **FALSE**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando uno [stile di visualizzazione](../controls/themes-overview.md) è attivo per questa finestra, questo parametro non viene usato.

Quando uno stile di visualizzazione non è attivo per questa finestra, questo parametro è un handle per un'area di aggiornamento facoltativa per l'area non client della finestra. Se questo parametro è impostato su -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non ridisegna l'area non client per riflettere la modifica dello stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Quando il *parametro wParam* è **FALSE,** un'applicazione deve restituire **TRUE** per indicare che il sistema deve procedere con l'elaborazione predefinita oppure deve restituire **FALSE** per impedire la modifica. Quando *wParam* è **TRUE,** il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

L'elaborazione di messaggi correlati all'area non client di una finestra standard non è consigliata, perché l'applicazione deve essere in grado di disegnare tutte le parti necessarie dell'area non client per la finestra. Se un'applicazione elabora questo messaggio, deve restituire **TRUE** per indirizzare il sistema a completare la modifica della finestra attiva. Se la finestra viene ridotta a icona quando viene ricevuto questo messaggio, l'applicazione deve passare il messaggio alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna la barra del titolo o il titolo dell'icona nei colori attivi quando il *parametro wParam* è **TRUE** e nei colori inattivi quando *wParam* è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
