---
title: WM_POINTERLEAVE messaggio
description: Inviato a una finestra quando un puntatore lascia l'intervallo di rilevamento sulla finestra (passaggio del mouse) o quando un puntatore si sposta all'esterno dei limiti della finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- WM_POINTERLEAVE messaggi di input e notifiche del messaggio
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 519e354aa43cf31d0a2477aec2f50a1405b7c4a254f2641497229c14f55d4679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964231"
---
# <a name="wm_pointerleave-message"></a>WM_POINTERLEAVE messaggio

Inviato a una finestra quando un puntatore lascia l'intervallo di rilevamento sulla finestra (passaggio del mouse) o quando un puntatore si sposta all'esterno dei limiti della finestra.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e informazioni aggiuntive. Usare le macro seguenti per recuperare queste informazioni.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica se il messaggio è stato generato da un puntatore che non ha un intervallo di rilevamento a sinistra. Questo flag non viene impostato quando il puntatore esce dall'intervallo di rilevamento della finestra.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto. Questo flag non è impostato per un puntatore nell'intervallo di rilevamento (passaggio del mouse).

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

Se un'applicazione elabora questo messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

La **WM_POINTERLEAVE** può essere usata da una finestra per modificare la modalità o arrestare qualsiasi feedback per l'utente mentre il puntatore si trova sull'area della finestra.

Questa notifica viene inviata solo alla finestra che riceve l'input per il puntatore. Nella tabella seguente sono elencate alcune delle situazioni in cui viene inviata la notifica.



| Azione                                        | Flag impostati                                                         | Notifiche inviate a                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Un puntatore al passaggio del mouse attraversa i limiti della finestra. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Finestra all'esterno del cui limite il puntatore è stato spostato.  |
| Un puntatore esce dall'intervallo di rilevamento.        | N/A                                                               | Finestra per cui l'indicatore di misura lascia l'intervallo di rilevamento. |



 

> \[! Importante\]  
> Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica WM_POINTERCAPTURECHANGED, [**in**](wm-pointercapturechanged.md) genere non riceve altre notifiche. Per questo motivo, è importante non fare ipotesi basate su [](wm-pointerdown.md)WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER / [](wm-pointerup.md) [](wm-pointerenter.md) / **WM_POINTERLEAVE** uniforme.

 

Se il contatto viene mantenuto con il digitalizzatore di input e il puntatore si sposta **all'esterno** della finestra, WM_POINTERLEAVE non viene generato. **WM_POINTERLEAVE** viene generato solo quando un puntatore al passaggio del mouse supera i limiti della finestra o il contatto viene terminato.

**WM_POINTERLEAVE** viene inviato alla coda di messaggi inviati se l'input è originato da un dispositivo mouse.

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

**Riferimento**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

