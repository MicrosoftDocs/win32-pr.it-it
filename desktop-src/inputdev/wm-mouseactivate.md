---
title: Messaggio WM_MOUSEACTIVATE (winuser. h)
description: Inviato quando il cursore si trova in una finestra inattiva e l'utente preme un pulsante del mouse. La finestra padre riceve questo messaggio solo se la finestra figlio la passa alla funzione DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Input della tastiera e del mouse WM_MOUSEACTIVATE messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119507"
---
# <a name="wm_mouseactivate-message"></a>\_Messaggio MOUSEACTIVATE WM

Inviato quando il cursore si trova in una finestra inattiva e l'utente preme un pulsante del mouse. La finestra padre riceve questo messaggio solo se la finestra figlio la passa alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra padre di primo livello della finestra attivata.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica il valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) . Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.

La parola più ordinata specifica l'identificatore del messaggio del mouse generato quando l'utente ha premuto un pulsante del mouse. Il messaggio del mouse viene rimosso o inviato alla finestra, a seconda del valore restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica se la finestra deve essere attivata e se l'identificatore del messaggio del mouse deve essere ignorato. Deve essere uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                          | Descrizione                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**Ma \_ ATTIVA**</dt> <dt>1</dt> </dl>         | Attiva la finestra e non rimuove il messaggio del mouse.<br/>         |
| <dl> <dt>**Ma \_ ACTIVATEANDEAT**</dt> <dt>2</dt> </dl>   | Attiva la finestra ed Elimina il messaggio del mouse.<br/>                 |
| <dl> <dt>**Ma \_ Noactivate**</dt> <dt>3</dt> </dl>       | Non attiva la finestra e non rimuove il messaggio del mouse.<br/> |
| <dl> <dt>**Ma \_ NOACTIVATEANDEAT**</dt> <dt>4</dt> </dl> | Non attiva la finestra, ma elimina il messaggio del mouse.<br/>         |



 

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre di una finestra figlio prima che venga eseguita qualsiasi elaborazione. La finestra padre determina se attivare la finestra figlio. Se attiva la finestra figlio, la finestra padre deve restituire **ma \_ noactivate** o **ma \_ NOACTIVATEANDEAT** per impedire al sistema di elaborare ulteriormente il messaggio.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_NCHITTEST WM**](wm-nchittest.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> </dl>

 

