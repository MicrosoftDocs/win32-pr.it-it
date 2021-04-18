---
title: Messaggio WM_POINTERACTIVATE
description: Inviato a una finestra inattiva quando un puntatore primario genera un WM_POINTERDOWN sulla finestra.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERACTIVATE
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302074"
---
# <a name="wm_pointeractivate-message"></a>Messaggio WM_POINTERACTIVATE

Inviato a una finestra inattiva quando un puntatore primario genera un [**WM_POINTERDOWN**](wm-pointerdown.md) sulla finestra. Finché il messaggio rimane non gestito, viene spostata verso l'alto nella catena della finestra padre fino a raggiungere la finestra di primo livello. Le applicazioni possono rispondere a questo messaggio per specificare se desiderano essere attivate.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e informazioni aggiuntive. Usare le macro seguenti per recuperare queste informazioni.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valore hit-test restituito dall'elaborazione del messaggio di [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene l'handle per la finestra di primo livello della finestra attivata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire uno dei valori descritti nella sezione Osservazioni.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Un'applicazione può gestire questo messaggio e restituire uno dei valori seguenti per determinare il modo in cui il sistema elabora l'attivazione e l'input di attivazione:

-   PA_ACTIVATE
-   PA_NOACTIVATE

È importante notare che, quando l'utente interagisce con il sistema con più puntatori simultanei, l'opportunità di attivazione rappresentata dal messaggio di **WM_POINTERACTIVATE** è disponibile solo per le applicazioni per il primo di tali puntatori. Le applicazioni devono pertanto tenere presente che potrebbero continuare a ricevere input dai puntatori mentre sono inattive.

Se l'applicazione non gestisce questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

