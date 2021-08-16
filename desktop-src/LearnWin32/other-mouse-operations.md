---
title: Operazioni varie del mouse
description: Nelle sezioni precedenti sono stati illustrati i clic del mouse e lo spostamento del mouse. Ecco alcune altre operazioni che possono essere eseguite con il mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31877ab5a71819fa896fd1253e7391f9ed748dffff636ab9d3e8591669b7fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387967"
---
# <a name="miscellaneous-mouse-operations"></a>Operazioni varie del mouse

Nelle sezioni precedenti sono stati illustrati i clic del mouse e lo spostamento del mouse. Ecco alcune altre operazioni che possono essere eseguite con il mouse.

## <a name="dragging-ui-elements"></a>Trascinamento di elementi dell'interfaccia utente

Se l'interfaccia utente supporta il trascinamento di elementi dell'interfaccia utente, è necessario chiamare un'altra funzione nel gestore di messaggi con scorrimento del mouse: [**DragDetect.**](/windows/desktop/api/winuser/nf-winuser-dragdetect) La **funzione DragDetect** restituisce **TRUE se** l'utente avvia un movimento del mouse che deve essere interpretato come trascinamento. Il codice seguente illustra come usare questa funzione.


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



Ecco l'idea: quando un programma supporta il trascinamento della selezione, non si vuole che ogni clic del mouse venga interpretato come un trascinamento. In caso contrario, l'utente potrebbe trascinare accidentalmente un elemento quando intende semplicemente fare clic su di esso,ad esempio per selezionarlo. Tuttavia, se un mouse è particolarmente sensibile, può essere difficile mantenerlo perfettamente mentre si fa clic. Pertanto, Windows definisce una soglia di trascinamento di alcuni pixel. Quando l'utente preme il pulsante del mouse, non viene considerato un trascinamento a meno che il mouse non supera questa soglia. La [**funzione DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) verifica se questa soglia viene raggiunta. Se la funzione restituisce **TRUE,** è possibile interpretare il clic del mouse come un trascinamento. In caso contrario, non eseguire questa operazione.

> [!Note]  
> Se [**DragDetect restituisce**](/windows/desktop/api/winuser/nf-winuser-dragdetect) **FALSE,** Windows elimina il messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) quando l'utente rilascia il pulsante del mouse. Pertanto, non chiamare **DragDetect a** meno che il programma non sia attualmente in una modalità che supporta il trascinamento. Ad esempio, se è già selezionato un elemento trascinabile dell'interfaccia utente. Alla fine di questo modulo verrà visualizzato un esempio di codice più lungo che usa la **funzione DragDetect.**

 

## <a name="confining-the-cursor"></a>Limitazione del cursore

In alcuni casi può essere necessario limitare il cursore all'area client o a una parte dell'area client. La [**funzione ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) limita lo spostamento del cursore a un rettangolo specificato. Questo rettangolo è specificato in coordinate dello schermo, anziché coordinate client, quindi il punto (0, 0) indica l'angolo superiore sinistro dello schermo. Per convertire le coordinate client in coordinate dello schermo, chiamare la [**funzione ClientToScreen.**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen)

Il codice seguente limita il cursore all'area client della finestra.


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



[**ClipCursor accetta**](/windows/desktop/api/winuser/nf-winuser-clipcursor) una [**struttura RECT,**](/previous-versions//dd162897(v=vs.85)) mentre [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) accetta una [**struttura POINT.**](/previous-versions//dd162805(v=vs.85)) Un rettangolo è definito dai relativi punti in alto a sinistra e in basso a destra. È possibile limitare il cursore a qualsiasi area rettangolare, incluse le aree esterne alla finestra, ma limitare il cursore all'area client è un modo tipico per usare la funzione . Il confini del cursore in un'area completamente esterna alla finestra sarebbe insolito e gli utenti probabilmente lo percepirebbero come un bug.

Per rimuovere la restrizione, [**chiamare ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) con il valore **NULL**.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Eventi di rilevamento del mouse: passaggio del mouse e spostamento

Altri due messaggi del mouse sono disabilitati per impostazione predefinita, ma possono essere utili per alcune applicazioni:

-   [**WM \_ MOUSEHOVER:**](/windows/desktop/inputdev/wm-mousehover)il cursore è stato posizionato sull'area client per un periodo di tempo fisso.
-   [**WM \_ MOUSELEAVE:**](/windows/desktop/inputdev/wm-mouseleave)il cursore ha lasciato l'area client.

Per abilitare questi messaggi, chiamare la [**funzione TrackMouseEvent.**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent)


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



La [**struttura TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contiene i parametri per la funzione. Il **membro dwFlags della** struttura contiene flag di bit che specificano i messaggi di rilevamento a cui si è interessati. È possibile scegliere di ottenere [**sia \_ MOUSEHOVER WM**](/windows/desktop/inputdev/wm-mousehover) che [**WM \_ MOUSELEAVE,**](/windows/desktop/inputdev/wm-mouseleave)come illustrato di seguito, o solo uno dei due. Il **membro dwHoverTime** specifica per quanto tempo il mouse deve passare il mouse prima che il sistema generi un messaggio al passaggio del mouse. Questo valore è espresso in millisecondi. La costante **HOVER \_ DEFAULT indica** l'uso dell'impostazione predefinita di sistema.

Dopo aver visualizzato uno dei messaggi richiesti, la funzione [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) viene reimpostata. È necessario chiamarlo nuovamente per ottenere un altro messaggio di rilevamento. Tuttavia, è necessario attendere fino al successivo messaggio di spostamento del mouse prima di chiamare **nuovamente TrackMouseEvent.** In caso contrario, la finestra potrebbe essere piena di messaggi di rilevamento. Ad esempio, se il mouse è al passaggio del mouse, il sistema continuerà a generare un flusso di messaggi [**\_ WM MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) mentre il mouse è zionario. In realtà non si vuole un altro messaggio **\_ MOUSEHOVER WM** fino a quando il mouse non si sposta in un'altra posizione e non si passa di nuovo al mouse.

Ecco una piccola classe helper che è possibile usare per gestire gli eventi di rilevamento del mouse.


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



Nell'esempio seguente viene illustrato come usare questa classe nella routine della finestra.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



Gli eventi di rilevamento del mouse richiedono un'ulteriore elaborazione da parte del sistema, quindi lasciarli disabilitati se non sono necessari.

Per completezza, ecco una funzione che esegue una query sul sistema per il timeout del passaggio del mouse predefinito.


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a>Rotellina del mouse

La funzione seguente controlla se è presente una rotellina del mouse.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Se l'utente ruota la rotellina del mouse, la finestra con lo stato attivo riceve un messaggio [**\_ WM MOUSEWHEEL.**](/windows/desktop/inputdev/wm-mousewheel) Il *parametro wParam* di questo messaggio contiene un valore intero denominato *delta* che misura la distanza di rotazione della rotellina. Il delta usa unità arbitrarie, dove 120 unità sono definite come la rotazione necessaria per eseguire un'"azione". Naturalmente, la definizione di un'azione dipende dal programma. Ad esempio, se si usa la rotellina del mouse per scorrere il testo, ogni 120 unità di rotazione scorrerebbe una riga di testo.

Il segno del delta indica la direzione di rotazione:

-   Positivo: ruotare in avanti, lontano dall'utente.
-   Negativo: ruota indietro, verso l'utente.

Il valore del delta viene inserito in *wParam* insieme ad alcuni flag aggiuntivi. Usare la macro [**GET \_ WHEEL DELTA \_ \_ WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) per ottenere il valore del delta.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Se la rotellina del mouse ha una risoluzione elevata, il valore assoluto del delta potrebbe essere minore di 120. In tal caso, se è opportuno che l'azione si verifichi con incrementi più piccoli, è possibile farlo. Ad esempio, il testo potrebbe scorrere di incrementi inferiori a una riga. In caso contrario, accumulare il delta totale fino a quando la ruota della ruota è sufficiente per eseguire l'azione. Archiviare il delta inutilizzato in una variabile e, quando si accumulano 120 unità (positive o negative), eseguire l'azione.

## <a name="next"></a>Prossima

[Input da tastiera](keyboard-input.md)

 

 