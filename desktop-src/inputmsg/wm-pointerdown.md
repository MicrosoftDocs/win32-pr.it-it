---
title: Messaggio WM_POINTERDOWN
description: Inviato quando un puntatore fa contatto sull'area client di una finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDOWN
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
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120555"
---
# <a name="wm_pointerdown-message"></a>Messaggio WM_POINTERDOWN

Inviato quando un puntatore fa contatto sull'area client di una finestra. Questo messaggio di input è destinato alla finestra su cui il puntatore fa riferimento e il puntatore viene acquisito in modo implicito nella finestra, in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene informazioni sul puntatore. Usare le macro seguenti per recuperare le informazioni dal parametro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio rappresenta il primo input generato da un nuovo puntatore.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore durante la relativa durata. Questo flag non è impostato per i messaggi che indicano che il puntatore ha un intervallo di rilevamento a sinistra
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto con l'area della finestra. Questo flag non è impostato per i messaggi che indicano un puntatore al passaggio del mouse.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica che questo puntatore è stato designato come primario.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione primaria.
    -   Questo è analogo a un pulsante sinistro del mouse.
    -   Il puntatore a tocco avrà questo set quando sarà in contatto con la superficie del digitalizzatore.
    -   Un puntatore della penna avrà questo set quando sarà in contatto con la superficie del digitalizzatore senza pulsanti premuti.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione secondaria.
    -   Questo è analogo al pulsante destro del mouse.
    -   Il puntatore della penna avrà questo set quando sarà in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se sono presenti una o più azioni terziarie basate sul tipo di puntatore. le applicazioni che vogliono rispondere a azioni terziarie devono recuperare informazioni specifiche per il tipo di puntatore per determinare quali pulsanti di terziaria vengono premuti. Ad esempio, un'applicazione può determinare lo stato dei pulsanti di una penna chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli Stati dei pulsanti.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il puntatore specificato ha avuto una quarta azione. Le applicazioni che vogliono rispondere a quattro azioni devono recuperare informazioni specifiche del tipo di puntatore per determinare se viene premuto il primo pulsante del mouse esteso (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**flag**](pointer-flags-contants.md) che indica se il puntatore specificato ha avuto una quinta azione. Le applicazioni che vogliono rispondere a quinte azioni devono recuperare informazioni specifiche del tipo di puntatore per determinare se viene premuto il secondo pulsante del mouse esteso (XButton2).

    Per altri dettagli, vedere [**flag puntatore**](pointer-flags-contants.md) .

    > [!Note]  
    > Un puntatore al passaggio del mouse non ha alcun flag dei pulsanti impostato. Questa operazione è analoga a uno spostamento del mouse senza pulsanti del mouse. Un'applicazione può determinare lo stato dei pulsanti di una penna in sospeso, ad esempio chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli Stati dei pulsanti.

     

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

> \[! Importante\]  
> Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica di [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , in genere non riceverà altre notifiche. Per questo motivo, è importante non prendere in considerazione le ipotesi basate su WM_POINTERDOWN abbinate in modo uniforme  / [**WM_POINTERUP**](wm-pointerup.md) o [**WM_POINTERENTER**](wm-pointerenter.md) / notifiche [**WM_POINTERLEAVE**](wm-pointerleave.md) .

 

Ogni puntatore ha un identificatore univoco del puntatore durante la relativa durata. La durata di un puntatore inizia quando viene rilevata per la prima volta.

Viene generato un messaggio [**WM_POINTERENTER**](wm-pointerenter.md) se viene rilevato un puntatore al passaggio del mouse. Un messaggio di **WM_POINTERDOWN** seguito da un messaggio di **WM_POINTERENTER** viene generato se viene rilevato un puntatore senza passaggio del mouse.

Durante la sua durata, un puntatore può generare una serie di messaggi di [**WM_POINTERUPDATE**](wm-pointerupdate.md) mentre è in corso il passaggio del mouse o il contatto.

La durata di un puntatore termina quando non viene più rilevata. Viene generato un messaggio di [**WM_POINTERLEAVE**](wm-pointerleave.md) .

Quando un puntatore viene interrotto, viene impostato [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .

Un messaggio di [**WM_POINTERLEAVE**](wm-pointerleave.md) può essere generato anche quando un puntatore non acquisito si sposta all'esterno dei limiti di una finestra.

Per ottenere la posizione orizzontale e verticale di un puntatore, utilizzare quanto segue:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Per convertire il parametro lParam in una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) , usare la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) .

Per recuperare ulteriori informazioni associate al messaggio, utilizzare la funzione [**GetPointerInfo**](/previous-versions/windows/desktop/api) .

Per determinare gli Stati dei tasti di modifica della tastiera associati a questo messaggio, usare la funzione [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) . Ad esempio, per rilevare che è stato premuto il tasto ALT, controllare se GetKeyState (VK_MENU) &lt; 0.

Si noti che se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi di [**WM_GESTURE**](../wintouch/wm-gesture.md) se la sequenza di input da questo e, possibilmente, altri puntatori viene riconosciuta come un movimento. Se non viene riconosciuto un movimento, **DefWindowProc** potrebbe generare un input del mouse.

Se un'applicazione usa selettivamente un input del puntatore e passa il resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), il comportamento risultante non è definito.

Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica di [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , in genere non riceverà altre notifiche. Pertanto, è importante che una finestra non faccia supposizioni dello stato del puntatore, indipendentemente dal fatto che riceva le notifiche in modo uniforme o in uscita o in ingresso/uscita.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come utilizzare [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)per recuperare le informazioni rilevanti associate al messaggio **WM_POINTERDOWN** .


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



Nell'esempio di codice seguente viene illustrato come utilizzare [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) per recuperare l'ID del puntatore dal messaggio di **WM_POINTERDOWN** .


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



Nell'esempio di codice seguente viene illustrato come gestire tipi di puntatore diversi, ad esempio touch, Pen o dispositivi di puntamento predefiniti.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



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

[**Flag puntatore**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

