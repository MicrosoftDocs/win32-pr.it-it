---
title: WM_NCPOINTERDOWN messaggio
description: Pubblicato quando un puntatore contatta l'area non client di una finestra.
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- WM_NCPOINTERDOWN messaggi di input e notifiche
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
ms.openlocfilehash: 419af1c613c979d30f479fc0739cd82f01b538f9ff4d3caa63839af8a40b0caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036059"
---
# <a name="wm_ncpointerdown-message"></a>WM_NCPOINTERDOWN messaggio

Pubblicato quando un puntatore contatta l'area non client di una finestra. Il messaggio è destinato alla finestra su cui il puntatore contatta. Il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere input per il puntatore fino a quando non interrompe il contatto.

Se una finestra ha acquisito questo puntatore, questo messaggio non viene pubblicato. Al contrario, [**viene WM_POINTERDOWN**](wm-pointerdown.md) nella finestra che ha acquisito questo puntatore.

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e informazioni aggiuntive. Usare le macro seguenti per recuperare queste informazioni.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valore dell'hit test restituito dall'elaborazione [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la posizione del punto del puntatore.

> [!Note]  
> Poiché il puntatore può contattare il dispositivo su un'area non semplice, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa. Quando possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.

 

Usare le macro seguenti per recuperare le coordinate fisiche dello schermo del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata x (punto orizzontale).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata y (punto verticale).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può eseguire una o più azioni di sistema a seconda del risultato dell'hit test incluso nel messaggio. In genere, le applicazioni non devono gestire questo messaggio.

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

 

