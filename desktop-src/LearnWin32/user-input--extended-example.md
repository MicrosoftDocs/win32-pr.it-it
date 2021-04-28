---
<span data-ttu-id="17886-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 31/05/2018</span><span class="sxs-lookup"><span data-stu-id="17886-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="user-input-extended-example"></a><span data-ttu-id="17886-102">Input utente: esempio esteso</span><span class="sxs-lookup"><span data-stu-id="17886-102">User Input: Extended Example</span></span>

<span data-ttu-id="17886-103">Si combinano tutti gli elementi appresi sull'input dell'utente per creare un semplice programma di disegno.</span><span class="sxs-lookup"><span data-stu-id="17886-103">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="17886-104">Ecco una schermata del programma:</span><span class="sxs-lookup"><span data-stu-id="17886-104">Here is a screen shot of the program:</span></span>

![Screenshot del programma di disegno](images/input03.png)

<span data-ttu-id="17886-106">L'utente può disegnare puntini di sospensione in diversi colori e selezionare, spostare o eliminare i puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="17886-106">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="17886-107">Per mantenere l'interfaccia utente semplice, il programma non consente all'utente di selezionare i colori dei puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="17886-107">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="17886-108">Al contrario, il programma scorre automaticamente un elenco predefinito di colori.</span><span class="sxs-lookup"><span data-stu-id="17886-108">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="17886-109">Il programma non supporta forme diverse da puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="17886-109">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="17886-110">Ovviamente, questo programma non riceverà alcun premi per il software di grafica.</span><span class="sxs-lookup"><span data-stu-id="17886-110">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="17886-111">Tuttavia, è comunque un esempio utile da cui imparare.</span><span class="sxs-lookup"><span data-stu-id="17886-111">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="17886-112">È possibile scaricare il codice sorgente completo da [Simple Drawing Sample](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="17886-112">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="17886-113">Questa sezione illustra solo alcune evidenziazioni.</span><span class="sxs-lookup"><span data-stu-id="17886-113">This section will just cover some highlights.</span></span>

<span data-ttu-id="17886-114">I puntini di sospensione sono rappresentati nel programma da una struttura che contiene i dati dei puntini di sospensione ([**D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e il colore ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="17886-114">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="17886-115">La struttura definisce anche due metodi: un metodo per disegnare l'ellisse e un metodo per eseguire l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="17886-115">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



<span data-ttu-id="17886-116">Il programma usa lo stesso pennello a tinta unita per disegnare il riempimento e il contorno per ogni ellisse, modificando il colore in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="17886-116">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="17886-117">In Direct2D la modifica del colore di un pennello a tinta unita è un'operazione efficiente.</span><span class="sxs-lookup"><span data-stu-id="17886-117">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="17886-118">L'oggetto pennello a tinta unita supporta quindi un [**metodo SetColor.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)</span><span class="sxs-lookup"><span data-stu-id="17886-118">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="17886-119">I puntini di sospensione vengono archiviati in un **contenitore** elenco STL:</span><span class="sxs-lookup"><span data-stu-id="17886-119">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="17886-120">**shared \_ ptr** è una classe di puntatore intelligente aggiunta a C++ in TR1 e formalizzata in C++0x.</span><span class="sxs-lookup"><span data-stu-id="17886-120">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="17886-121">Visual Studio 2010 aggiunge il supporto per **\_ pt** r condiviso e altre funzionalità di C++0x.</span><span class="sxs-lookup"><span data-stu-id="17886-121">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="17886-122">Per altre informazioni, vedere [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="17886-122">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="17886-123">Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="17886-123">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="17886-124">Il programma ha tre modalità:</span><span class="sxs-lookup"><span data-stu-id="17886-124">The program has three modes:</span></span>

-   <span data-ttu-id="17886-125">Modalità di disegno.</span><span class="sxs-lookup"><span data-stu-id="17886-125">Draw mode.</span></span> <span data-ttu-id="17886-126">L'utente può disegnare nuovi puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="17886-126">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="17886-127">Modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="17886-127">Selection mode.</span></span> <span data-ttu-id="17886-128">L'utente può selezionare un ellisse.</span><span class="sxs-lookup"><span data-stu-id="17886-128">The user can select an ellipse.</span></span>
-   <span data-ttu-id="17886-129">Modalità di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="17886-129">Drag mode.</span></span> <span data-ttu-id="17886-130">L'utente può trascinare un ellisse selezionato.</span><span class="sxs-lookup"><span data-stu-id="17886-130">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="17886-131">L'utente può passare dalla modalità di disegno alla modalità di selezione usando gli stessi tasti di scelta rapida descritti in [Tabelle dei tasti di scelta rapida.](accelerator-tables.md)</span><span class="sxs-lookup"><span data-stu-id="17886-131">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="17886-132">Dalla modalità di selezione, il programma passa alla modalità di trascinamento se l'utente fa clic su un ellisse.</span><span class="sxs-lookup"><span data-stu-id="17886-132">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="17886-133">Torna alla modalità di selezione quando l'utente rilascia il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="17886-133">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="17886-134">La selezione corrente viene archiviata come iteratore nell'elenco di puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="17886-134">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="17886-135">Il metodo helper `MainWindow::Selection` restituisce un puntatore all'ellisse selezionata oppure il valore **nullptr** se non è presente alcuna selezione.</span><span class="sxs-lookup"><span data-stu-id="17886-135">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



<span data-ttu-id="17886-136">La tabella seguente riepiloga gli effetti dell'input del mouse in ognuna delle tre modalità.</span><span class="sxs-lookup"><span data-stu-id="17886-136">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="17886-137">Mouse Input</span><span class="sxs-lookup"><span data-stu-id="17886-137">Mouse Input</span></span>      | <span data-ttu-id="17886-138">Modalità disegno</span><span class="sxs-lookup"><span data-stu-id="17886-138">Draw Mode</span></span>                                          | <span data-ttu-id="17886-139">Modalità di selezione</span><span class="sxs-lookup"><span data-stu-id="17886-139">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="17886-140">Modalità di trascinamento</span><span class="sxs-lookup"><span data-stu-id="17886-140">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="17886-141">Pulsante sinistro in basso</span><span class="sxs-lookup"><span data-stu-id="17886-141">Left button down</span></span> | <span data-ttu-id="17886-142">Impostare mouse capture e iniziare a disegnare una nuova ellisse.</span><span class="sxs-lookup"><span data-stu-id="17886-142">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="17886-143">Rilasciare la selezione corrente ed eseguire un hit test.</span><span class="sxs-lookup"><span data-stu-id="17886-143">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="17886-144">Se viene raggiunto un'ellisse, acquisire il cursore, selezionare l'ellisse e passare alla modalità di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="17886-144">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="17886-145">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="17886-145">No action.</span></span>                 |
| <span data-ttu-id="17886-146">Spostamento del mouse</span><span class="sxs-lookup"><span data-stu-id="17886-146">Mouse move</span></span>       | <span data-ttu-id="17886-147">Se il pulsante sinistro è in basso, ridimensionare i puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="17886-147">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="17886-148">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="17886-148">No action.</span></span>                                                                                                                                   | <span data-ttu-id="17886-149">Spostare i puntini di sospensione selezionati.</span><span class="sxs-lookup"><span data-stu-id="17886-149">Move the selected ellipse.</span></span> |
| <span data-ttu-id="17886-150">Pulsante sinistro in alto</span><span class="sxs-lookup"><span data-stu-id="17886-150">Left button up</span></span>   | <span data-ttu-id="17886-151">Interrompere il disegno dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="17886-151">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="17886-152">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="17886-152">No action.</span></span>                                                                                                                                   | <span data-ttu-id="17886-153">Passare alla modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="17886-153">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="17886-154">Il metodo seguente nella classe `MainWindow` gestisce i messaggi WM [**\_ LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown)</span><span class="sxs-lookup"><span data-stu-id="17886-154">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



<span data-ttu-id="17886-155">Le coordinate del mouse vengono passate a questo metodo in pixel e quindi convertite in DIP.</span><span class="sxs-lookup"><span data-stu-id="17886-155">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="17886-156">È importante non confondere queste due unità.</span><span class="sxs-lookup"><span data-stu-id="17886-156">It is important not to confuse these two units.</span></span> <span data-ttu-id="17886-157">Ad esempio, la [**funzione DragDetect usa**](/windows/desktop/api/winuser/nf-winuser-dragdetect) i pixel, mentre il disegno e l'hit testing usano i DIP.</span><span class="sxs-lookup"><span data-stu-id="17886-157">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="17886-158">La regola generale è che le funzioni correlate alle finestre o all'input del mouse usano pixel, mentre Direct2D e DirectWrite usano DIP.</span><span class="sxs-lookup"><span data-stu-id="17886-158">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="17886-159">Testare sempre il programma con un'impostazione con valori DPI elevati e ricordarsi di contrassegnare il programma come in grado di riconoscere DPI.</span><span class="sxs-lookup"><span data-stu-id="17886-159">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="17886-160">Per altre informazioni, vedere [DPI e pixel Device-Independent pixel.](dpi-and-device-independent-pixels.md)</span><span class="sxs-lookup"><span data-stu-id="17886-160">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="17886-161">Ecco il codice che gestisce i [**messaggi WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove)</span><span class="sxs-lookup"><span data-stu-id="17886-161">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="17886-162">La logica per ridimensionare un'ellisse è stata descritta in precedenza, nella [sezione Esempio: Disegno di cerchi](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="17886-162">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="17886-163">Si noti anche la chiamata a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="17886-163">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="17886-164">Ciò garantisce che la finestra sia ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="17886-164">This makes sure that the window is repainted.</span></span> <span data-ttu-id="17886-165">Il codice seguente gestisce i [**messaggi WM \_ LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup)</span><span class="sxs-lookup"><span data-stu-id="17886-165">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



<span data-ttu-id="17886-166">Come si può vedere, i gestori di messaggi per l'input del mouse hanno tutti codice di diramazione, a seconda della modalità corrente.</span><span class="sxs-lookup"><span data-stu-id="17886-166">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="17886-167">Si tratta di una progettazione accettabile per questo programma piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="17886-167">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="17886-168">Tuttavia, potrebbe diventare rapidamente troppo complesso se vengono aggiunte nuove modalità.</span><span class="sxs-lookup"><span data-stu-id="17886-168">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="17886-169">Per un programma più grande, un'architettura model-view-controller (MVC) potrebbe essere una progettazione migliore.</span><span class="sxs-lookup"><span data-stu-id="17886-169">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="17886-170">In questo tipo di architettura, il *controller*, che gestisce l'input dell'utente, è separato dal modello *,* che gestisce i dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17886-170">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="17886-171">Quando il programma cambia modalità, il cursore cambia per fornire feedback all'utente.</span><span class="sxs-lookup"><span data-stu-id="17886-171">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



<span data-ttu-id="17886-172">Infine, ricordarsi di impostare il cursore quando la finestra riceve un [**messaggio WM \_ SETCURSOR:**](/windows/desktop/menurc/wm-setcursor)</span><span class="sxs-lookup"><span data-stu-id="17886-172">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="17886-173">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="17886-173">Summary</span></span>

<span data-ttu-id="17886-174">In questo modulo si è appreso come gestire l'input tramite mouse e tastiera. come definire i tasti di scelta rapida; e come aggiornare l'immagine del cursore per riflettere lo stato corrente del programma.</span><span class="sxs-lookup"><span data-stu-id="17886-174">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 
