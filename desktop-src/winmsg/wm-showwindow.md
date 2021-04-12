---
description: Inviato a una finestra quando la finestra sta per essere nascosta o visualizzata.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Messaggio WM_SHOWWINDOW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345571"
---
# <a name="wm_showwindow-message"></a>\_Messaggio ShowWindow WM

Inviato a una finestra quando la finestra sta per essere nascosta o visualizzata.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se viene visualizzata una finestra. Se *wParam* è **true**, viene visualizzata la finestra. Se *wParam* è **false**, la finestra viene nascosta.

</dd> <dt>

*lParam* 
</dt> <dd>

Stato della finestra visualizzata. Se *lParam* è zero, il messaggio è stato inviato a causa di una chiamata alla funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) . in caso contrario, *lParam* è uno dei valori seguenti.



| Valore                                                                                                                                                                                                                         | Significato                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt> </dl>       | È in corso il recupero della finestra perché una finestra di ingrandimento è stata ripristinata o ridotta a icona.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt> </dl>             | La finestra è coperta da un'altra finestra ingrandita.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_ PARENTCLOSING**</dt> <dt>1</dt> </dl> | La finestra proprietaria della finestra viene ridotta a icona.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt> </dl> | È in corso il ripristino della finestra proprietaria della finestra.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nasconde o Mostra la finestra, come specificato dal messaggio. Se una finestra ha lo stile di visualizzazione [**WS \_ visibile**](window-styles.md) quando viene creato, la finestra riceve questo messaggio dopo che è stato creato, ma prima che venga visualizzato. Una finestra riceve anche questo messaggio quando lo stato di visibilità viene modificato dalla funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) o [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) .

Il messaggio **WM \_ ShowWindow** non viene inviato nelle circostanze seguenti:

-   Quando viene creata una finestra sovrapposta di primo livello con lo stile [**WS \_ ingrandito**](window-styles.md) o **WS \_** .
-   Quando il flag **SW \_ SHOWNORMAL** viene specificato nella chiamata alla funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .

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

[**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
