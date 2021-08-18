---
title: WM_POINTERUP messaggio
description: Pubblicato quando un puntatore che ha effettuato il contatto sull'area client di una finestra interrompe il contatto.
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- WM_POINTERUP messaggi di input e notifiche
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5bf811501d189abef127e2b191e159518654650bf569cd2abdad42d7471eb1d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756799"
---
# <a name="wm_pointerup-message"></a>WM_POINTERUP messaggio

Pubblicato quando un puntatore che ha effettuato il contatto sull'area client di una finestra interrompe il contatto. Questo messaggio di input è destinato alla finestra sulla quale il puntatore effettua il contatto e il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere messaggi di **input, inclusa** la notifica WM_POINTERUP per il puntatore fino a quando non interrompe il contatto.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene informazioni sul puntatore. Usare le macro seguenti per recuperare informazioni dal parametro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se questo messaggio rappresenta il primo input generato da un nuovo puntatore.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore durante la durata. Questo flag non è impostato sui messaggi che indicano che il puntatore ha un intervallo di rilevamento a sinistra
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto con la superficie della finestra. Questo flag non è impostato sui messaggi che indicano un puntatore al passaggio del mouse.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica che questo puntatore è stato designato come primario.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione primaria.
    -   Questo è analogo a un pulsante sinistro del mouse verso il basso.
    -   Un puntatore tocco avrà questo set quando è in contatto con la superficie del digitalizzatore.
    -   Un puntatore a penna avrà questo set quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione secondaria.
    -   Questo è analogo a un pulsante destro del mouse verso il basso.
    -   Un puntatore a penna avrà questo set quando è in contatto con la superficie del digitalizzatore con il pulsante pentola premuto.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se sono presenti una o più azioni terziarie in base al tipo di puntatore. Le applicazioni che vogliono rispondere alle azioni terziarie devono recuperare informazioni specifiche per il tipo di puntatore per determinare quali pulsanti terziari vengono premuti. Ad esempio, un'applicazione può determinare gli stati dei pulsanti di una penna chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli stati del pulsante.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il puntatore specificato ha preso la quarta azione. Le applicazioni che vogliono rispondere a quarta azione devono recuperare informazioni specifiche per il tipo di puntatore per determinare se viene premuto il primo pulsante del mouse esteso (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag [**che**](pointer-flags-contants.md) indica se il puntatore specificato ha preso la quinta azione. Le applicazioni che vogliono rispondere a quinta azione devono recuperare informazioni specifiche per il tipo di puntatore per determinare se viene premuto il secondo pulsante del mouse esteso (XButton2).

    Per [**altri dettagli, vedere Flag**](pointer-flags-contants.md) puntatore.

    > [!Note]  
    > Per un puntatore al passaggio del mouse non è impostato nessuno dei flag del pulsante. Questo è analogo a uno spostamento del mouse senza pulsanti del mouse verso il basso. Un'applicazione può determinare gli stati dei pulsanti di una penna al passaggio del mouse, ad esempio chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli stati del pulsante.

     

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

> \[! Importante\]  
> Quando una finestra perde l'acquisizione di [](wm-pointercapturechanged.md) un puntatore e riceve la notifica WM_POINTERCAPTURECHANGED, in genere non riceverà altre notifiche. Per questo motivo, è importante non fare ipotesi in base [](wm-pointerdown.md)alle notifiche di WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER /  [](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) uniforme.

 

Ogni puntatore ha un identificatore di puntatore univoco durante la sua durata. La durata di un puntatore inizia quando viene rilevato per la prima volta.

Se [**viene rilevato un puntatore**](wm-pointerenter.md) al passaggio del mouse, viene generato un messaggio WM_POINTERENTER messaggio di errore. Un [**WM_POINTERDOWN**](wm-pointerdown.md) seguito da un messaggio **WM_POINTERENTER** viene generato se viene rilevato un puntatore non al passaggio del mouse.

Durante la durata, un puntatore può generare una serie di WM_POINTERUPDATE [**durante**](wm-pointerupdate.md) il passaggio del mouse o in contatto.

La durata di un puntatore termina quando non viene più rilevata. Verrà generato un [**messaggio WM_POINTERLEAVE**](wm-pointerleave.md) messaggio.

Quando un puntatore viene [**interrotto,**](pointer-flags-contants.md) POINTER_FLAG_CANCELED impostato.

Un [**WM_POINTERLEAVE**](wm-pointerleave.md) può essere generato anche quando un puntatore non acquisito si sposta all'esterno dei limiti di una finestra.

Per ottenere la posizione orizzontale e verticale di un puntatore, usare quanto segue:

Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



La [**macro MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) può essere usata anche per convertire il parametro lParam in una [**struttura POINTS.**](/previous-versions//dd162808(v=vs.85))

La [**funzione GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) può essere usata per determinare gli stati dei tasti di modifica della tastiera associati a questo messaggio. Ad esempio, per rilevare che il tasto ALT è stato premuto, controllare se **GetKeyState**(VK_MENU) &lt; 0.

Se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi [**WM_GESTURE**](../wintouch/wm-gesture.md)se la sequenza di input da questo e, possibilmente, altri puntatori viene riconosciuta come movimento. Se un movimento non viene riconosciuto, **DefWindowProc** può generare l'input del mouse.

Se un'applicazione utilizza in modo selettivo un input del puntatore e passa il resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), il comportamento risultante non è definito.

Usare la [**funzione GetPointerInfo**](/previous-versions/windows/desktop/api) per recuperare altre informazioni correlate a questo messaggio.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come recuperare la posizione x e y del puntatore associato a questo messaggio.


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



Nell'esempio di codice seguente viene illustrato come ottenere l'ID puntatore associato a questo messaggio.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



Nell'esempio di codice seguente viene illustrato come gestire tipi di puntatore diversi associati a questo messaggio.


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
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
    if (!GetPointerPenInfo(pointerId, &penInfo))
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
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



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
