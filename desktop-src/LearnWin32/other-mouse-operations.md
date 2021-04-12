---
title: Operazioni del mouse varie
description: Nelle sezioni precedenti sono stati discussi i clic del mouse e il movimento del mouse. Di seguito sono riportate alcune altre operazioni che possono essere eseguite con il mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337383"
---
# <a name="miscellaneous-mouse-operations"></a>Operazioni del mouse varie

Nelle sezioni precedenti sono stati discussi i clic del mouse e il movimento del mouse. Di seguito sono riportate alcune altre operazioni che possono essere eseguite con il mouse.

## <a name="dragging-ui-elements"></a>Trascinamento di elementi dell'interfaccia utente

Se l'interfaccia utente supporta il trascinamento di elementi dell'interfaccia utente, è necessario chiamare un'altra funzione nel gestore di messaggi del mouse: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). La funzione **DragDetect** restituisce **true** se l'utente avvia un movimento del mouse da interpretare come trascinamento. Il codice seguente illustra come usare questa funzione.


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



Ecco l'idea: quando un programma supporta il trascinamento della selezione, non è necessario che ogni clic del mouse venga interpretato come un trascinamento. In caso contrario, l'utente potrebbe trascinare accidentalmente qualcosa quando ha semplicemente intenzione di fare clic su di esso, ad esempio per selezionarlo. Tuttavia, se il mouse è particolarmente sensibile, può essere difficile mantenere il mouse ancora in modo ottimale quando si fa clic. Windows definisce pertanto una soglia di trascinamento di pochi pixel. Quando l'utente preme il pulsante del mouse, non viene considerato un trascinamento, a meno che il mouse non superi questa soglia. La funzione [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) verifica se questa soglia viene raggiunta. Se la funzione restituisce **true**, è possibile interpretare il clic del mouse come un trascinamento. In caso contrario, non.

> [!Note]  
> Se [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) restituisce **false**, Windows elimina il messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) quando l'utente rilascia il pulsante del mouse. Pertanto, non chiamare **DragDetect** , a meno che il programma non sia attualmente in una modalità che supporta il trascinamento. Se, ad esempio, un elemento dell'interfaccia utente trascinabile è già selezionato. Alla fine di questo modulo, verrà visualizzato un esempio di codice più lungo che usa la funzione **DragDetect** .

 

## <a name="confining-the-cursor"></a>Limitazione del cursore

In alcuni casi potrebbe essere necessario limitare il cursore all'area client o a una parte dell'area client. La funzione [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) limita lo spostamento del cursore a un rettangolo specificato. Questo rettangolo viene specificato nelle coordinate dello schermo, anziché nelle coordinate client, quindi il punto (0, 0) indica l'angolo superiore sinistro dello schermo. Per tradurre le coordinate client nelle coordinate dello schermo, chiamare la funzione [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).

Il codice seguente consente di limitare il cursore all'area client della finestra.


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



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) accetta una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) , ma [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) accetta una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) . Un rettangolo viene definito dai punti superiore sinistro e inferiore destro. È possibile limitare il cursore a qualsiasi area rettangolare, incluse le aree all'esterno della finestra, ma la limitazione del cursore all'area client è un modo tipico per usare la funzione. La limitazione del cursore a un'area completamente esterna alla finestra potrebbe essere insolita e gli utenti probabilmente lo percepiranno come un bug.

Per rimuovere la restrizione, chiamare [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) con il valore **null**.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Eventi di rilevamento del mouse: passaggio del mouse e uscita

Per impostazione predefinita, altri due messaggi del mouse sono disabilitati, ma possono essere utili per alcune applicazioni:

-   [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): il cursore è posizionato sull'area client per un periodo di tempo fisso.
-   [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): il cursore ha lasciato l'area client.

Per abilitare questi messaggi, chiamare la funzione [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



La struttura [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contiene i parametri per la funzione. Il membro **dwFlags** della struttura contiene flag di bit che specificano i messaggi di rilevamento a cui si è interessati. È possibile scegliere di ottenere sia [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) che [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), come illustrato qui, o solo uno dei due. Il membro **dwHoverTime** specifica la durata del passaggio del mouse prima che il sistema generi un messaggio hover. Questo valore è espresso in millisecondi. Per **\_ impostazione predefinita, il valore predefinito di hover** indica l'utilizzo dell'impostazione predefinita del sistema.

Dopo aver ottenuto uno dei messaggi richiesti, la funzione [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) viene reimpostata. Per ottenere un altro messaggio di rilevamento, è necessario chiamarlo di nuovo. Tuttavia, è necessario attendere fino al successivo messaggio di spostamento del mouse prima di chiamare di nuovo **TrackMouseEvent** . In caso contrario, è possibile che la finestra venga sovraccaricata con i messaggi di rilevamento. Ad esempio, se il mouse viene spostato, il sistema continuerà a generare un flusso di messaggi [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) mentre il mouse è stazionario. In realtà non si vuole un altro messaggio **WM \_ MOUSEHOVER** fino a quando il mouse si sposta in un altro punto e si passa nuovamente.

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



Nell'esempio seguente viene illustrato come utilizzare questa classe nella routine della finestra.


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

Per completezza, di seguito è illustrata una funzione che esegue una query sul sistema per il timeout predefinito del passaggio del mouse.


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



Se l'utente ruota la rotellina del mouse, la finestra con lo stato attivo riceve un messaggio [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) . Il parametro *wParam* di questo messaggio contiene un valore integer denominato *Delta* che misura la distanza con cui è stata ruotata la rotellina. Il Delta USA unità arbitrarie, in cui 120 unità è definita come rotazione necessaria per eseguire una "azione". Naturalmente, la definizione di un'azione dipende dal programma. Se ad esempio si usa la rotellina del mouse per scorrere il testo, ogni 120 unità di rotazione scorrerà una riga di testo.

Il segno del Delta indica la direzione di rotazione:

-   Positivo: ruotare in orizzontale, lontano dall'utente.
-   Negativo: ruotare indietro verso l'utente.

Il valore del Delta viene inserito in *wParam* insieme ad alcuni flag aggiuntivi. Usare la macro [**get \_ Wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) per ottenere il valore del Delta.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Se la rotellina del mouse ha una risoluzione elevata, il valore assoluto del Delta potrebbe essere minore di 120. In tal caso, se è opportuno che l'azione venga eseguita con incrementi più piccoli, è possibile farlo. Ad esempio, il testo potrebbe scorrere in base a incrementi di meno di una riga. In caso contrario, accumulare il Delta totale finché la rotellina non ruota abbastanza per eseguire l'azione. Archiviare il Delta non usato in una variabile e quando si accumulano 120 unità (positive o negative), eseguire l'azione.

## <a name="next"></a>Prossima

[Input da tastiera](keyboard-input.md)

 

 