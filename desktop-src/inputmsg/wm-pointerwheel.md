---
title: WM_POINTERWHEEL messaggio
description: Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- WM_POINTERWHEEL messaggi di input e notifiche del messaggio
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 93144125c21da2d29a0d71f56d8d865da4a07dda6adff2f25ce3528fca72b475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756529"
---
# <a name="wm_pointerwheel-message"></a>WM_POINTERWHEEL messaggio

Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e il delta della rotellina. Usare le macro seguenti per recuperare queste informazioni.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): delta della ruota come valore short con segno.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la posizione del punto del puntatore.

> [!Note]  
> Poiché l'indicatore di misura può contattare il dispositivo su un'area non semplice, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa. Quando possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.

 

Usare le macro seguenti per recuperare le coordinate fisiche dello schermo del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata x (punto orizzontale).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata y (punto verticale).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione elabora questo messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Per recuperare le unità di scorrimento della rotellina, usare **inputData** della [**struttura POINTER_INFO**](/previous-versions/windows/desktop/api) restituita chiamando la [**funzione GetPointerInfo.**](/previous-versions/windows/desktop/api) Questo campo contiene un valore con segno ed è espresso in un multiplo di **WHEEL_DELTA**. Un valore positivo indica una rotazione in avanti e un valore negativo indica una rotazione all'indietro.

Si noti che gli input della rotellina possono essere recapitati anche se il cursore del mouse si trova all'esterno della finestra dell'applicazione. I messaggi wheel vengono recapitati in modo molto simile agli input da tastiera. La finestra di stato attivo della coda di messaggi principale riceve i messaggi wheel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

