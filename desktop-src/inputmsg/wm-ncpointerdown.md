---
title: Messaggio WM_NCPOINTERDOWN
description: Inviato quando un puntatore fa contatto sull'area non client di una finestra.
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- Messaggi e notifiche di input del messaggio WM_NCPOINTERDOWN
topic_type:
- apiref
api_name:
- WM_NCPOINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6f4c3ef8ed75c5bd29250cd2f9ce4d666b6d961d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964589"
---
# <a name="wm_ncpointerdown-message"></a>Messaggio WM_NCPOINTERDOWN

Inviato quando un puntatore fa contatto sull'area non client di una finestra. Il messaggio è destinato alla finestra su cui il puntatore crea il contatto. Il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto.

Se una finestra ha acquisito questo puntatore, questo messaggio non viene inviato. Al contrario, viene pubblicato un [**WM_POINTERDOWN**](wm-pointerdown.md) nella finestra che ha acquisito il puntatore.

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e informazioni aggiuntive. Usare le macro seguenti per recuperare queste informazioni.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valore hit-test restituito dall'elaborazione del messaggio di [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la posizione del punto del puntatore.

> [!Note]  
> Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa. Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.

 

Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può eseguire una o più azioni di sistema a seconda del risultato dell'hit test incluso nel messaggio. In genere, le applicazioni non devono necessariamente gestire questo messaggio.

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

 

