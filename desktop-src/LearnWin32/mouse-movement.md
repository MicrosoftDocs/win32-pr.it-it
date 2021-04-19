---
title: Spostamento del mouse
description: Spostamento del mouse
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320228"
---
# <a name="mouse-movement"></a>Spostamento del mouse

Quando il mouse viene spostato, Windows invia un messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Per impostazione predefinita, **WM \_ MOUSEMOVE** passa alla finestra che contiene il cursore. È possibile eseguire l'override di questo comportamento *acquisendo* il mouse, descritto nella sezione successiva.

Il messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) contiene gli stessi parametri dei messaggi per i clic del mouse. I 16 bit più bassi di *lParam* contengono la coordinata x e i successivi 16 bit contengono la coordinata y. Usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per decomprimere le coordinate da *lParam*. Il parametro *wParam* contiene un operatore OR bit per bit di flag, che indica lo stato degli altri **pulsanti del mouse** oltre ai tasti MAIUSC e CTRL. Il codice seguente ottiene le coordinate del mouse da *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Tenere presente che queste coordinate sono espresse in pixel, non in pixel indipendenti dal dispositivo (DIP). Più avanti in questo argomento verrà esaminato il codice che esegue la conversione tra le due unità.

Una finestra può anche ricevere un messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se la posizione del cursore cambia rispetto alla finestra. Se, ad esempio, il cursore è posizionato su una finestra e l'utente nasconde la finestra, la finestra riceve i messaggi di **WM \_ MOUSEMOVE** anche se il mouse non è stato spostato. Una conseguenza di questo comportamento è che le coordinate del mouse potrebbero non essere modificate tra i messaggi di **WM \_ MOUSEMOVE** .

## <a name="capturing-mouse-movement-outside-the-window"></a>Acquisizione del movimento del mouse all'esterno della finestra

Per impostazione predefinita, una finestra smette di ricevere messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se il mouse viene spostato oltre il bordo dell'area client. Tuttavia, per alcune operazioni, potrebbe essere necessario tenere traccia della posizione del mouse oltre questo punto. Un programma di disegno, ad esempio, potrebbe consentire all'utente di trascinare il rettangolo di selezione oltre il bordo della finestra, come illustrato nel diagramma seguente.

![illustrazione dell'acquisizione del mouse.](images/input01.png)

Per ricevere i messaggi di spostamento del mouse oltre il bordo della finestra, chiamare la funzione [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) . Dopo la chiamata a questa funzione, la finestra continuerà a ricevere i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) per il periodo di tempo in cui l'utente deve contenere almeno un pulsante del mouse, anche se il mouse si sposta all'esterno della finestra. La finestra di acquisizione deve essere la finestra in primo piano e una sola finestra può essere la finestra di acquisizione alla volta. Per rilasciare il mouse capture, chiamare la funzione [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .

In genere si usa [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) e [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) nel modo seguente.

1.  Quando l'utente preme il pulsante sinistro del mouse, chiamare [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) per avviare l'acquisizione del mouse.
2.  Rispondere ai messaggi di spostamento del mouse.
3.  Quando l'utente rilascia il pulsante sinistro del mouse, chiamare [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).

## <a name="example-drawing-circles"></a>Esempio: disegno di cerchi

Si estenderà il programma Circle dal [modulo 3](module-3---windows-graphics.md) consentendo all'utente di creare un cerchio con il mouse. Iniziare con il programma di [esempio del cerchio Direct2D](direct2d-circle-sample.md) . Il codice in questo esempio verrà modificato per aggiungere un disegno semplice. In primo luogo, aggiungere una nuova variabile membro alla `MainWindow` classe.


```C++
    D2D1_POINT_2F           ptMouse;
```



Questa variabile archivia la posizione del mouse mentre l'utente trascina il mouse. Nel `MainWindow` Costruttore inizializzare le variabili *ellisse* e *ptMouse* .


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



Rimuovere il corpo del `MainWindow::CalculateLayout` metodo. non è necessario per questo esempio.


```C++
    void    CalculateLayout() { }
```



Dichiarare quindi i gestori dei messaggi per i messaggi di sinistra, di sinistra e di spostamento del mouse.


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



Le coordinate del mouse vengono fornite in pixel fisici, ma Direct2D prevede i DIP (device independent pixel). Per gestire correttamente le impostazioni a DPI elevato, è necessario tradurre le coordinate dei pixel in DIP. Per ulteriori informazioni su DPI, vedere [dpi e Device-Independent pixel](dpi-and-device-independent-pixels.md). Nel codice seguente viene illustrata una classe helper che converte i pixel in DIP.


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



Chiamare `DPIScale::Initialize` nel gestore [**WM \_ create**](/windows/desktop/winmsg/wm-create) dopo aver creato l'oggetto factory Direct2D.


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



Per ottenere le coordinate del mouse in DIP dai messaggi del mouse, procedere come segue:

1.  Usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per ottenere le coordinate dei pixel. Queste macro sono definite in WindowsX. h, quindi ricordarsi di includere l'intestazione nel progetto.
2.  Chiamare `DPIScale::PixelsToDipsX` e `DPIScale::PixelsToDipsY` per convertire i pixel in DIP.

A questo punto aggiungere i gestori di messaggi alla routine della finestra.


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



Infine, implementare i gestori di messaggi stessi.

### <a name="left-button-down"></a>Pulsante sinistro

Per il pulsante sinistro, eseguire le operazioni seguenti:

1.  Chiamare [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) per avviare l'acquisizione del mouse.
2.  Archiviare la posizione del clic del mouse nella variabile *ptMouse* . Questa posizione definisce l'angolo superiore sinistro del rettangolo di delimitazione per l'ellisse.
3.  Reimposta la struttura ellisse.
4.  Chiamare [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Questa funzione forza la ridisegnare la finestra.


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>Spostamento del mouse

Per il messaggio di spostamento del mouse, controllare se il pulsante sinistro del mouse è premuto. In caso contrario, ricalcolare l'ellisse e ridisegnare la finestra. In Direct2D, un'ellisse è definita dal punto centrale e dai raggi x e y. Si vuole creare un'ellisse che corrisponda al rettangolo di selezione definito dal puntatore del mouse (*ptMouse*) e alla posizione corrente del cursore (*x*, *y*), in modo che sia necessario un po' di aritmetica per trovare la larghezza, l'altezza e la posizione dell'ellisse.

Il codice seguente ricalcola l'ellisse e quindi chiama [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) per ridisegnare la finestra.

![Diagramma che mostra un'ellisse con raggi x e y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a>Pulsante a sinistra in alto

Per il messaggio di pulsante a sinistra, è sufficiente chiamare [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) per rilasciare il mouse capture.


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>Prossima

[Altre operazioni del mouse](other-mouse-operations.md)

 

 