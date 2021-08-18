---
title: WM_POINTERDOWN messaggio
description: Pubblicato quando un puntatore contatta l'area client di una finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN messaggi di input e notifiche del messaggio
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
ms.openlocfilehash: fd2c5900cba4a66b4f7cf94f1df362ddc0f29f3d258b972b77ad63f3fd45a5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481982"
---
# <a name="wm_pointerdown-message"></a>WM_POINTERDOWN messaggio

Pubblicato quando un puntatore contatta l'area client di una finestra. Questo messaggio di input è destinato alla finestra sulla quale il puntatore si mette in contatto e il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere l'input per il puntatore fino a quando non interrompe il contatto.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene informazioni sul puntatore. Usare le macro seguenti per recuperare informazioni dal parametro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se questo messaggio rappresenta il primo input generato da un nuovo puntatore.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore durante la sua durata. Questo flag non è impostato nei messaggi che indicano che il puntatore ha un intervallo di rilevamento a sinistra
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto con l'area della finestra. Questo flag non è impostato nei messaggi che indicano un puntatore al passaggio del mouse.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica che questo puntatore è stato designato come primario.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione primaria.
    -   Ciò è analogo a un pulsante sinistro del mouse verso il basso.
    -   Un puntatore tocco avrà impostato questo valore quando è in contatto con la superficie del digitalizzatore.
    -   Un puntatore penna avrà questo set quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione secondaria.
    -   Ciò è analogo a un pulsante destro del mouse verso il basso.
    -   Un puntatore della penna avrà questo valore impostato quando è in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se sono presenti una o più azioni terziarie in base al tipo di puntatore; Le applicazioni che vogliono rispondere alle azioni terziarie devono recuperare informazioni specifiche per il tipo di puntatore per determinare quali pulsanti terziari vengono premuti. Ad esempio, un'applicazione può determinare gli stati dei pulsanti di una penna chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli stati dei pulsanti.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il puntatore specificato ha preso la quarta azione. Le applicazioni che vogliono rispondere a quarta azione devono recuperare informazioni specifiche del tipo di puntatore per determinare se è premuto il primo pulsante esteso del mouse (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**flag che**](pointer-flags-contants.md) indica se il puntatore specificato ha preso la quinta azione. Le applicazioni che vogliono rispondere a quinta azione devono recuperare informazioni specifiche del tipo di puntatore per determinare se è premuto il secondo pulsante esteso del mouse (XButton2).

    Per altri [**dettagli, vedere**](pointer-flags-contants.md) Flag puntatore.

    > [!Note]  
    > Un puntatore al passaggio del mouse non ha impostato nessuno dei flag del pulsante. Ciò è analogo a uno spostamento del mouse senza pulsanti del mouse verso il basso. Un'applicazione può determinare gli stati dei pulsanti di una penna al passaggio del mouse, ad esempio chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli stati dei pulsanti.

     

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

> \[! Importante\]  
> Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica WM_POINTERCAPTURECHANGED, [**in**](wm-pointercapturechanged.md) genere non riceve altre notifiche. Per questo motivo, è importante non fare ipotesi basate su WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER / [](wm-pointerup.md) [](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) uniforme.

 

Ogni puntatore ha un identificatore di puntatore univoco durante la sua durata. La durata di un puntatore inizia quando viene rilevato per la prima volta.

Viene [**WM_POINTERENTER**](wm-pointerenter.md) un messaggio di errore se viene rilevato un puntatore al passaggio del mouse. Se **WM_POINTERDOWN** viene rilevato un puntatore **non WM_POINTERENTER** mouse, viene generato un messaggio di errore.

Durante la sua durata, un puntatore può generare una serie [**di**](wm-pointerupdate.md) WM_POINTERUPDATE durante il passaggio del mouse o in contatto.

La durata di un puntatore termina quando non viene più rilevata. Verrà generato un [**WM_POINTERLEAVE**](wm-pointerleave.md) messaggio.

Quando un puntatore viene [**interrotto,**](pointer-flags-contants.md) POINTER_FLAG_CANCELED viene impostato .

Un [**WM_POINTERLEAVE**](wm-pointerleave.md) può essere generato anche quando un puntatore non acquisito si sposta all'esterno dei limiti di una finestra.

Per ottenere la posizione orizzontale e verticale di un puntatore, usare quanto segue:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Per convertire il parametro lParam in [**una struttura POINTS,**](/previous-versions//dd162808(v=vs.85)) usare la macro [**MAKEPOINTS.**](/windows/win32/api/wingdi/nf-wingdi-makepoints)

Per recuperare altre informazioni associate al messaggio, usare la [**funzione GetPointerInfo.**](/previous-versions/windows/desktop/api)

Per determinare gli stati dei tasti di modifica della tastiera associati a questo messaggio, usare la [**funzione GetKeyState.**](/windows/win32/api/winuser/nf-winuser-getkeystate) Ad esempio, per rilevare che è stato premuto il tasto ALT, controllare se GetKeyState(VK_MENU) &lt; 0.

Si noti che se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi [**WM_GESTURE**](../wintouch/wm-gesture.md) se la sequenza di input da questo e, possibilmente, altri puntatori viene riconosciuto come movimento. Se un movimento non viene riconosciuto, **DefWindowProc** può generare l'input del mouse.

Se un'applicazione utilizza in modo selettivo un input del puntatore e passa il resto a [**DefWindowProc,**](/windows/win32/api/winuser/nf-winuser-defwindowproca)il comportamento risultante non è definito.

Quando una finestra perde l'acquisizione di [](wm-pointercapturechanged.md) un puntatore e riceve la notifica WM_POINTERCAPTURECHANGED, in genere non riceve altre notifiche. È quindi importante che una finestra non presunzioni lo stato del puntatore, indipendentemente dal fatto che riceva notifiche DOWN/UP o ENTER/LEAVE abbinate in modo uniforme.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come usare [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)per recuperare le informazioni rilevanti associate al **messaggio WM_POINTERDOWN.**


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



Nell'esempio di codice seguente viene illustrato come [**usare GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) per recuperare l'ID del puntatore **dal WM_POINTERDOWN** messaggio.


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



L'esempio di codice seguente illustra come gestire diversi tipi di puntatore, ad esempio tocco, penna o dispositivi di puntamento predefiniti.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

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
