---
description: Inviato a una finestra quando è necessario modificare l'area non client per indicare uno stato attivo o inattivo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Messaggio WM_NCACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312370"
---
# <a name="wm_ncactivate-message"></a>\_Messaggio NCACTIVATE WM

Inviato a una finestra quando è necessario modificare l'area non client per indicare uno stato attivo o inattivo.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica quando è necessario modificare una barra del titolo o un'icona per indicare uno stato attivo o inattivo. Se è necessario disegnare una barra del titolo o un'icona attiva, il parametro *wParam* è **true**. Se è necessario disegnare una barra del titolo o un'icona inattiva, *wParam* è **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando uno [stile di visualizzazione](../controls/themes-overview.md) è attivo per questa finestra, questo parametro non viene utilizzato.

Quando uno stile di visualizzazione non è attivo per questa finestra, questo parametro è un handle per un'area di aggiornamento facoltativa per l'area non client della finestra. Se questo parametro è impostato su-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non ridisegna l'area non client per riflettere la modifica dello stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Quando il parametro *wParam* è **false**, un'applicazione deve restituire **true** per indicare che il sistema deve procedere con l'elaborazione predefinita oppure deve restituire **false** per evitare la modifica. Quando *wParam* è **true**, il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Non è consigliabile elaborare i messaggi correlati all'area non client di una finestra standard, perché l'applicazione deve essere in grado di creare tutte le parti necessarie dell'area non client per la finestra. Se un'applicazione elabora il messaggio, deve restituire **true** per indicare al sistema di completare la modifica della finestra attiva. Se la finestra è ridotta a icona quando viene ricevuto questo messaggio, l'applicazione deve passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna la barra del titolo o il titolo dell'icona nei colori attivi quando il parametro *wParam* è **true** e nei colori inattivi quando *wParam* è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

 

 
