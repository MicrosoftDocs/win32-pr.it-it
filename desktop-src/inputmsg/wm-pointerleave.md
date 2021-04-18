---
title: Messaggio WM_POINTERLEAVE
description: Inviato a una finestra quando un puntatore lascia un intervallo di rilevamento sulla finestra (hover) o quando un puntatore si sposta all'esterno dei limiti della finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERLEAVE
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
ms.openlocfilehash: 2ee58fd74f266d067f6211e156d984a3b3d1c477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302070"
---
# <a name="wm_pointerleave-message"></a>Messaggio WM_POINTERLEAVE

Inviato a una finestra quando un puntatore lascia un intervallo di rilevamento sulla finestra (hover) o quando un puntatore si sposta all'esterno dei limiti della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene l'identificatore del puntatore e informazioni aggiuntive. Usare le macro seguenti per recuperare queste informazioni.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica se il messaggio è stato generato da un puntatore che non ha un intervallo di rilevamento sinistro. Questo flag non viene impostato quando il puntatore esce dall'intervallo di rilevamento della finestra.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto. Questo flag non è impostato per un puntatore nell'intervallo di rilevamento (hover).

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

La notifica **WM_POINTERLEAVE** può essere utilizzata da una finestra per modificare la modalità o arrestare eventuali commenti e suggerimenti dell'utente mentre il puntatore è posizionato sull'area della finestra.

Questa notifica viene inviata solo alla finestra che sta ricevendo l'input per il puntatore. Nella tabella seguente sono elencate alcune delle situazioni in cui viene inviata la notifica.



| Azione                                        | Flag impostati                                                         | Notifiche inviate a                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Un puntatore al passaggio del mouse attraversa i limiti della finestra. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Finestra al di fuori del cui limite è stato spostato il puntatore.  |
| Un puntatore esce dall'intervallo di rilevamento.        | N/D                                                               | Finestra per la quale il puntatore lascia l'intervallo di rilevamento. |



 

> \[! Importante\]  
> Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica di [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , in genere non riceverà altre notifiche. Per questo motivo, è importante non prendere in considerazione le ipotesi basate su WM_POINTERDOWN abbinate in modo uniforme [](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md) o [**WM_POINTERENTER**](wm-pointerenter.md) / notifiche **WM_POINTERLEAVE** .

 

Se il contatto viene mantenuto con il digitalizzatore di input e il puntatore si sposta all'esterno della finestra, **WM_POINTERLEAVE** non viene generato. **WM_POINTERLEAVE** viene generato solo quando un puntatore al passaggio del mouse supera i limiti della finestra o il contatto viene terminato.

**WM_POINTERLEAVE** viene inserito nella coda dei messaggi inviati se l'input viene originato da un dispositivo mouse.

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

**Riferimento**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

