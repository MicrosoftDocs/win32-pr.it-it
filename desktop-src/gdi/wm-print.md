---
description: Il \_ messaggio di stampa WM viene inviato a una finestra per richiedere che venga disegnato nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Messaggio WM_PRINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049873"
---
# <a name="wm_print-message"></a>\_Messaggio di stampa WM

Il messaggio di **\_ stampa WM** viene inviato a una finestra per richiedere che venga disegnato nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo da creare.

</dd> <dt>

*lParam* 
</dt> <dd>

Opzioni di disegno. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Disegna la finestra solo se è visibile.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**\_elementi figlio PRF**</dt> </dl>             | Disegna tutte le finestre figlio visibili.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_client PRF**</dt> </dl>                   | Disegna l'area client della finestra.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Cancella lo sfondo prima di disegnare la finestra.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**non \_ client PRF**</dt> </dl>          | Disegna l'area non client della finestra.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**\_Proprietà PRF**</dt> </dl>                      | Disegna tutte le finestre di proprietà.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora questo messaggio in base all'opzione di disegno specificata: se si \_ specifica PRF CHECKVISIBLE e la finestra non è visibile, non eseguire alcuna operazione se \_ si specifica PRF non client, creare l'area non client nel contesto di dispositivo specificato. Se \_ si specifica PRF ERASEBKGND, inviare alla finestra un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , se \_ è specificato il client PRF, inviare alla finestra un messaggio [**WM \_ PRINTCLIENT**](wm-printclient.md) , se \_ è impostato PRF Children, inviare ogni finestra figlio visibile un messaggio di **\_ stampa WM** , se \_ è impostata la proprietà PRF, inviare ogni finestra di proprietà visibile a un messaggio di **\_ stampa WM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari su disegno e disegno](painting-and-drawing.md)
</dt> <dt>

[Disegno e creazione di messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_ERASEBKGND WM**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**\_PRINTCLIENT WM**](wm-printclient.md)
</dt> </dl>

 

 
