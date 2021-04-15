---
title: Messaggio WM_POINTERWHEEL
description: Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERWHEEL
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
ms.openlocfilehash: ad1177b2e92e47ca40c745e6cd5f1ea2cf259215
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476138"
---
# <a name="wm_pointerwheel-message"></a>Messaggio WM_POINTERWHEEL

Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e il Delta della rotellina. Usare le macro seguenti per recuperare queste informazioni.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): Delta della rotellina come valore short con segno.

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

Se l'applicazione elabora il messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Per recuperare le unità di scorrimento della rotellina, usare il **inputData** archiviato della struttura [**POINTER_INFO**](/previous-versions/windows/desktop/api) restituita chiamando la funzione [**GetPointerInfo**](/previous-versions/windows/desktop/api) . Questo campo contiene un valore con segno ed è espresso in un multiplo di **WHEEL_DELTA**. Un valore positivo indica una rotazione in avanti e un valore negativo indica una rotazione indietro.

Si noti che gli input della rotellina possono essere recapitati anche se il cursore del mouse si trova all'esterno della finestra dell'applicazione. I messaggi della rotellina vengono recapitati in modo molto simile agli input da tastiera. La finestra di stato attivo della coda di messaggi foregournd riceve i messaggi della rotellina.

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

 

