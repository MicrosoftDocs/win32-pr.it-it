---
title: Messaggio WM_TOUCHHITTESTING
description: Inviato a una finestra in un tocco per determinare la destinazione del tocco più probabile.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- Messaggi e notifiche di input del messaggio WM_TOUCHHITTESTING
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
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120355"
---
# <a name="wm_touchhittesting-message"></a>Messaggio WM_TOUCHHITTESTING

Inviato a una finestra in un tocco per determinare la destinazione del tocco più probabile.

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


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

Puntatore alla struttura [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) che include i dati dell'area di contatto tocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se uno o più elementi si trovano all'interno dell'area contatto tocco, un'applicazione deve restituire il risultato di [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).

Se nessun elemento si trova all'interno dell'area contatto tocco, un'applicazione deve impostare il valore di **Score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) su [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) e chiamare [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) per ottenere il valore restituito lResult.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato a Windows che effettua la registrazione tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**Punteggi hit testing tocco**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

