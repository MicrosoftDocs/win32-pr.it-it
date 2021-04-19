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
# <a name="mouse-movement"></a><span data-ttu-id="5c5a0-103">Spostamento del mouse</span><span class="sxs-lookup"><span data-stu-id="5c5a0-103">Mouse Movement</span></span>

<span data-ttu-id="5c5a0-104">Quando il mouse viene spostato, Windows invia un messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="5c5a0-105">Per impostazione predefinita, **WM \_ MOUSEMOVE** passa alla finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="5c5a0-106">È possibile eseguire l'override di questo comportamento *acquisendo* il mouse, descritto nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="5c5a0-107">Il messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) contiene gli stessi parametri dei messaggi per i clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="5c5a0-108">I 16 bit più bassi di *lParam* contengono la coordinata x e i successivi 16 bit contengono la coordinata y.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="5c5a0-109">Usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per decomprimere le coordinate da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="5c5a0-110">Il parametro *wParam* contiene un operatore OR bit per bit di flag, che indica lo stato degli altri **pulsanti del mouse** oltre ai tasti MAIUSC e CTRL.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="5c5a0-111">Il codice seguente ottiene le coordinate del mouse da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="5c5a0-112">Tenere presente che queste coordinate sono espresse in pixel, non in pixel indipendenti dal dispositivo (DIP).</span><span class="sxs-lookup"><span data-stu-id="5c5a0-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="5c5a0-113">Più avanti in questo argomento verrà esaminato il codice che esegue la conversione tra le due unità.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="5c5a0-114">Una finestra può anche ricevere un messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se la posizione del cursore cambia rispetto alla finestra.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="5c5a0-115">Se, ad esempio, il cursore è posizionato su una finestra e l'utente nasconde la finestra, la finestra riceve i messaggi di **WM \_ MOUSEMOVE** anche se il mouse non è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="5c5a0-116">Una conseguenza di questo comportamento è che le coordinate del mouse potrebbero non essere modificate tra i messaggi di **WM \_ MOUSEMOVE** .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="5c5a0-117">Acquisizione del movimento del mouse all'esterno della finestra</span><span class="sxs-lookup"><span data-stu-id="5c5a0-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="5c5a0-118">Per impostazione predefinita, una finestra smette di ricevere messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se il mouse viene spostato oltre il bordo dell'area client.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="5c5a0-119">Tuttavia, per alcune operazioni, potrebbe essere necessario tenere traccia della posizione del mouse oltre questo punto.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="5c5a0-120">Un programma di disegno, ad esempio, potrebbe consentire all'utente di trascinare il rettangolo di selezione oltre il bordo della finestra, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![illustrazione dell'acquisizione del mouse.](images/input01.png)

<span data-ttu-id="5c5a0-122">Per ricevere i messaggi di spostamento del mouse oltre il bordo della finestra, chiamare la funzione [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="5c5a0-123">Dopo la chiamata a questa funzione, la finestra continuerà a ricevere i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) per il periodo di tempo in cui l'utente deve contenere almeno un pulsante del mouse, anche se il mouse si sposta all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="5c5a0-124">La finestra di acquisizione deve essere la finestra in primo piano e una sola finestra può essere la finestra di acquisizione alla volta.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="5c5a0-125">Per rilasciare il mouse capture, chiamare la funzione [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="5c5a0-126">In genere si usa [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) e [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="5c5a0-127">Quando l'utente preme il pulsante sinistro del mouse, chiamare [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) per avviare l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="5c5a0-128">Rispondere ai messaggi di spostamento del mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="5c5a0-129">Quando l'utente rilascia il pulsante sinistro del mouse, chiamare [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span><span class="sxs-lookup"><span data-stu-id="5c5a0-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="5c5a0-130">Esempio: disegno di cerchi</span><span class="sxs-lookup"><span data-stu-id="5c5a0-130">Example: Drawing Circles</span></span>

<span data-ttu-id="5c5a0-131">Si estenderà il programma Circle dal [modulo 3](module-3---windows-graphics.md) consentendo all'utente di creare un cerchio con il mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="5c5a0-132">Iniziare con il programma di [esempio del cerchio Direct2D](direct2d-circle-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="5c5a0-133">Il codice in questo esempio verrà modificato per aggiungere un disegno semplice.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="5c5a0-134">In primo luogo, aggiungere una nuova variabile membro alla `MainWindow` classe.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="5c5a0-135">Questa variabile archivia la posizione del mouse mentre l'utente trascina il mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="5c5a0-136">Nel `MainWindow` Costruttore inizializzare le variabili *ellisse* e *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="5c5a0-137">Rimuovere il corpo del `MainWindow::CalculateLayout` metodo. non è necessario per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="5c5a0-138">Dichiarare quindi i gestori dei messaggi per i messaggi di sinistra, di sinistra e di spostamento del mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="5c5a0-139">Le coordinate del mouse vengono fornite in pixel fisici, ma Direct2D prevede i DIP (device independent pixel).</span><span class="sxs-lookup"><span data-stu-id="5c5a0-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="5c5a0-140">Per gestire correttamente le impostazioni a DPI elevato, è necessario tradurre le coordinate dei pixel in DIP.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="5c5a0-141">Per ulteriori informazioni su DPI, vedere [dpi e Device-Independent pixel](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="5c5a0-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="5c5a0-142">Nel codice seguente viene illustrata una classe helper che converte i pixel in DIP.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


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



<span data-ttu-id="5c5a0-143">Chiamare `DPIScale::Initialize` nel gestore [**WM \_ create**](/windows/desktop/winmsg/wm-create) dopo aver creato l'oggetto factory Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


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



<span data-ttu-id="5c5a0-144">Per ottenere le coordinate del mouse in DIP dai messaggi del mouse, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="5c5a0-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="5c5a0-145">Usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per ottenere le coordinate dei pixel.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="5c5a0-146">Queste macro sono definite in WindowsX. h, quindi ricordarsi di includere l'intestazione nel progetto.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="5c5a0-147">Chiamare `DPIScale::PixelsToDipsX` e `DPIScale::PixelsToDipsY` per convertire i pixel in DIP.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="5c5a0-148">A questo punto aggiungere i gestori di messaggi alla routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-148">Now add the message handlers to your window procedure.</span></span>


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



<span data-ttu-id="5c5a0-149">Infine, implementare i gestori di messaggi stessi.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="5c5a0-150">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="5c5a0-150">Left Button Down</span></span>

<span data-ttu-id="5c5a0-151">Per il pulsante sinistro, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c5a0-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="5c5a0-152">Chiamare [**secapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) per avviare l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="5c5a0-153">Archiviare la posizione del clic del mouse nella variabile *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="5c5a0-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="5c5a0-154">Questa posizione definisce l'angolo superiore sinistro del rettangolo di delimitazione per l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="5c5a0-155">Reimposta la struttura ellisse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="5c5a0-156">Chiamare [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="5c5a0-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="5c5a0-157">Questa funzione forza la ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="5c5a0-158">Spostamento del mouse</span><span class="sxs-lookup"><span data-stu-id="5c5a0-158">Mouse Move</span></span>

<span data-ttu-id="5c5a0-159">Per il messaggio di spostamento del mouse, controllare se il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="5c5a0-160">In caso contrario, ricalcolare l'ellisse e ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="5c5a0-161">In Direct2D, un'ellisse è definita dal punto centrale e dai raggi x e y.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="5c5a0-162">Si vuole creare un'ellisse che corrisponda al rettangolo di selezione definito dal puntatore del mouse (*ptMouse*) e alla posizione corrente del cursore (*x*, *y*), in modo che sia necessario un po' di aritmetica per trovare la larghezza, l'altezza e la posizione dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="5c5a0-163">Il codice seguente ricalcola l'ellisse e quindi chiama [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) per ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

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



### <a name="left-button-up"></a><span data-ttu-id="5c5a0-165">Pulsante a sinistra in alto</span><span class="sxs-lookup"><span data-stu-id="5c5a0-165">Left Button Up</span></span>

<span data-ttu-id="5c5a0-166">Per il messaggio di pulsante a sinistra, è sufficiente chiamare [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) per rilasciare il mouse capture.</span><span class="sxs-lookup"><span data-stu-id="5c5a0-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="5c5a0-167">Prossima</span><span class="sxs-lookup"><span data-stu-id="5c5a0-167">Next</span></span>

[<span data-ttu-id="5c5a0-168">Altre operazioni del mouse</span><span class="sxs-lookup"><span data-stu-id="5c5a0-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 