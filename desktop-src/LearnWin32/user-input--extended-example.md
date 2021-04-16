---
title: Esempio esteso di input utente
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104557271"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="cfa90-103">Input utente: esempio esteso</span><span class="sxs-lookup"><span data-stu-id="cfa90-103">User Input: Extended Example</span></span>

<span data-ttu-id="cfa90-104">È possibile combinare tutto ciò che è stato appreso sull'input dell'utente per creare un semplice programma di disegno.</span><span class="sxs-lookup"><span data-stu-id="cfa90-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="cfa90-105">Ecco uno screenshot del programma:</span><span class="sxs-lookup"><span data-stu-id="cfa90-105">Here is a screen shot of the program:</span></span>

![screenshot del programma di disegno](images/input03.png)

<span data-ttu-id="cfa90-107">L'utente può creare puntini di sospensione in diversi colori e selezionare, spostare o eliminare ellissi.</span><span class="sxs-lookup"><span data-stu-id="cfa90-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="cfa90-108">Per semplificare l'interfaccia utente, il programma non consente all'utente di selezionare i colori dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="cfa90-109">Al contrario, il programma scorre automaticamente un elenco predefinito di colori.</span><span class="sxs-lookup"><span data-stu-id="cfa90-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="cfa90-110">Il programma non supporta alcuna forma diversa dai puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="cfa90-111">Ovviamente, questo programma non vincerà alcun premio per il software grafico.</span><span class="sxs-lookup"><span data-stu-id="cfa90-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="cfa90-112">Tuttavia, è ancora un esempio utile per imparare da.</span><span class="sxs-lookup"><span data-stu-id="cfa90-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="cfa90-113">È possibile scaricare il codice sorgente completo da [esempio di disegno semplice](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="cfa90-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="cfa90-114">In questa sezione vengono illustrate solo alcune novità.</span><span class="sxs-lookup"><span data-stu-id="cfa90-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="cfa90-115">I puntini di sospensione sono rappresentati nel programma da una struttura che contiene i dati dell'ellisse ([**d2d1 \_ ellisse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e il colore ([**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="cfa90-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="cfa90-116">La struttura definisce inoltre due metodi: un metodo per creare l'ellisse e un metodo per eseguire l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="cfa90-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


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



<span data-ttu-id="cfa90-117">Il programma usa lo stesso pennello a tinta unita per disegnare il riempimento e il contorno per ogni ellisse, modificando il colore in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="cfa90-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="cfa90-118">In Direct2D, la modifica del colore di un pennello a tinta unita è un'operazione efficiente.</span><span class="sxs-lookup"><span data-stu-id="cfa90-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="cfa90-119">Quindi, l'oggetto pennello a tinta unita supporta un metodo [**Secolor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="cfa90-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="cfa90-120">I puntini di sospensione vengono archiviati in un contenitore **elenco** STL:</span><span class="sxs-lookup"><span data-stu-id="cfa90-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="cfa90-121">**il \_ ptr condiviso** è una classe di puntatore intelligente che è stata aggiunta a C++ in TR1 e formalizzata in C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="cfa90-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="cfa90-122">Visual Studio 2010 aggiunge il supporto **per \_ PT r condiviso** e altre funzionalità di C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="cfa90-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="cfa90-123">Per ulteriori informazioni, vedere la pagina relativa all' [esplorazione delle nuove funzionalità C++ e MFC in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="cfa90-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="cfa90-124">Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="cfa90-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="cfa90-125">Il programma prevede tre modalità:</span><span class="sxs-lookup"><span data-stu-id="cfa90-125">The program has three modes:</span></span>

-   <span data-ttu-id="cfa90-126">Modalità di estrazione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-126">Draw mode.</span></span> <span data-ttu-id="cfa90-127">L'utente può creare nuovi ellissi.</span><span class="sxs-lookup"><span data-stu-id="cfa90-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="cfa90-128">Modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-128">Selection mode.</span></span> <span data-ttu-id="cfa90-129">L'utente può selezionare un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="cfa90-130">Modalità di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="cfa90-130">Drag mode.</span></span> <span data-ttu-id="cfa90-131">L'utente può trascinare un'ellisse selezionata.</span><span class="sxs-lookup"><span data-stu-id="cfa90-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="cfa90-132">L'utente può passare dalla modalità di estrazione alla modalità di selezione e viceversa usando gli stessi tasti di scelta rapida descritti nelle [tabelle dei tasti di scelta rapida](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cfa90-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="cfa90-133">Dalla modalità di selezione, il programma passa alla modalità di trascinamento se l'utente fa clic su un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="cfa90-134">Torna alla modalità di selezione quando l'utente rilascia il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="cfa90-135">La selezione corrente viene archiviata come iteratore nell'elenco di ellissi.</span><span class="sxs-lookup"><span data-stu-id="cfa90-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="cfa90-136">Il metodo helper `MainWindow::Selection` restituisce un puntatore all'ellisse selezionata oppure il valore **nullptr** se non è presente alcuna selezione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


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



<span data-ttu-id="cfa90-137">Nella tabella seguente sono riepilogati gli effetti dell'input del mouse in ognuna delle tre modalità.</span><span class="sxs-lookup"><span data-stu-id="cfa90-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="cfa90-138">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="cfa90-138">Mouse Input</span></span>      | <span data-ttu-id="cfa90-139">Modalità di estrazione</span><span class="sxs-lookup"><span data-stu-id="cfa90-139">Draw Mode</span></span>                                          | <span data-ttu-id="cfa90-140">Modalità di selezione</span><span class="sxs-lookup"><span data-stu-id="cfa90-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="cfa90-141">Modalità di trascinamento</span><span class="sxs-lookup"><span data-stu-id="cfa90-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="cfa90-142">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="cfa90-142">Left button down</span></span> | <span data-ttu-id="cfa90-143">Impostare l'acquisizione del mouse e iniziare a creare una nuova ellisse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="cfa90-144">Rilascia la selezione corrente ed esegue un hit test.</span><span class="sxs-lookup"><span data-stu-id="cfa90-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="cfa90-145">Se viene raggiunta un'ellisse, Acquisisci il cursore, seleziona l'ellisse e passa alla modalità di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="cfa90-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="cfa90-146">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-146">No action.</span></span>                 |
| <span data-ttu-id="cfa90-147">Spostamento del mouse</span><span class="sxs-lookup"><span data-stu-id="cfa90-147">Mouse move</span></span>       | <span data-ttu-id="cfa90-148">Se il pulsante sinistro è inattivo, ridimensionare l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="cfa90-149">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="cfa90-150">Spostare l'ellisse selezionata.</span><span class="sxs-lookup"><span data-stu-id="cfa90-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="cfa90-151">Pulsante a sinistra in alto</span><span class="sxs-lookup"><span data-stu-id="cfa90-151">Left button up</span></span>   | <span data-ttu-id="cfa90-152">Arresta il disegno dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="cfa90-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="cfa90-153">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="cfa90-154">Passa alla modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="cfa90-155">Il metodo seguente nella `MainWindow` classe gestisce i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="cfa90-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


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



<span data-ttu-id="cfa90-156">Le coordinate del mouse vengono passate a questo metodo in pixel, quindi convertite in DIP.</span><span class="sxs-lookup"><span data-stu-id="cfa90-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="cfa90-157">È importante non confondere queste due unità.</span><span class="sxs-lookup"><span data-stu-id="cfa90-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="cfa90-158">Ad esempio, la funzione [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa i pixel, ma il disegno e l'hit testing usano DIP.</span><span class="sxs-lookup"><span data-stu-id="cfa90-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="cfa90-159">La regola generale è che le funzioni correlate all'input di Windows o del mouse utilizzano pixel, mentre Direct2D e DirectWrite utilizzano DIP.</span><span class="sxs-lookup"><span data-stu-id="cfa90-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="cfa90-160">Testare sempre il programma con impostazioni DPI elevate e ricordarsi di contrassegnare il programma come compatibile con DPI.</span><span class="sxs-lookup"><span data-stu-id="cfa90-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="cfa90-161">Per ulteriori informazioni, vedere [dpi e Device-Independent pixel](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="cfa90-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="cfa90-162">Ecco il codice che gestisce i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="cfa90-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


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



<span data-ttu-id="cfa90-163">La logica per ridimensionare un'ellisse è stata descritta in precedenza, nella sezione [esempio: disegno dei cerchi](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa90-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="cfa90-164">Si noti inoltre la chiamata a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="cfa90-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="cfa90-165">In questo modo si garantisce che la finestra venga ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="cfa90-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="cfa90-166">Il codice seguente gestisce i messaggi [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="cfa90-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


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



<span data-ttu-id="cfa90-167">Come si può notare, i gestori di messaggi per l'input del mouse hanno tutti il codice di diramazione, a seconda della modalità corrente.</span><span class="sxs-lookup"><span data-stu-id="cfa90-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="cfa90-168">Si tratta di un progetto accettabile per questo programma piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="cfa90-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="cfa90-169">Tuttavia, potrebbe diventare rapidamente troppo complesso se vengono aggiunte nuove modalità.</span><span class="sxs-lookup"><span data-stu-id="cfa90-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="cfa90-170">Per un programma più ampio, un'architettura MVC (Model-View-Controller) potrebbe essere una progettazione migliore.</span><span class="sxs-lookup"><span data-stu-id="cfa90-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="cfa90-171">In questo tipo di architettura, il *controller*, che gestisce l'input dell'utente, è separato dal *modello*, che gestisce i dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cfa90-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="cfa90-172">Quando il programma commuta le modalità, il cursore cambia per fornire commenti e suggerimenti all'utente.</span><span class="sxs-lookup"><span data-stu-id="cfa90-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


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



<span data-ttu-id="cfa90-173">Infine, ricordarsi di impostare il cursore quando la finestra riceve un messaggio di [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="cfa90-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="cfa90-174">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="cfa90-174">Summary</span></span>

<span data-ttu-id="cfa90-175">In questo modulo si è appreso come gestire l'input del mouse e della tastiera; come definire i tasti di scelta rapida; e come aggiornare l'immagine del cursore in modo da riflettere lo stato corrente del programma.</span><span class="sxs-lookup"><span data-stu-id="cfa90-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 