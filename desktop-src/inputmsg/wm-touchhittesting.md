---
title: WM_TOUCHHITTESTING messaggio
description: Inviato a una finestra con un tocco verso il basso per determinare la destinazione del tocco più probabile.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING messaggi di input e notifiche del messaggio
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 895c535330674767683d0155bd2e22b8a40389c08378187377497380d71d97b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829491"
---
# <a name="wm_touchhittesting-message"></a>WM_TOUCHHITTESTING messaggio

Inviato a una finestra con un tocco verso il basso per determinare la destinazione del tocco più probabile.

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) che contiene i dati dell'area di contatto tocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se uno o più elementi si trova all'interno dell'area di contatto tocco, un'applicazione deve restituire il risultato di [**PackTouchHitTestingProximityEvaluation.**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)

Se nessun elemento si trova all'interno dell'area di contatto tocco, un'applicazione deve impostare il valore di **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) su [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) e chiamare [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) per ottenere il valore restituito LRESULT.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alle finestre che eseguono la registrazione [**tramite la funzione RegisterTouchHitTestingWindow.**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**Punteggi di hit testing tocco**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

