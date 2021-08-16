---
title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018
---

# <a name="user-input-extended-example"></a>Input utente: esempio esteso

Si combinano tutti gli elementi appresi sull'input dell'utente per creare un semplice programma di disegno. Ecco una schermata del programma:

![Screenshot del programma di disegno](images/input03.png)

L'utente può disegnare puntini di sospensione in diversi colori e selezionare, spostare o eliminare puntini di sospensione. Per mantenere l'interfaccia utente semplice, il programma non consente all'utente di selezionare i colori dei puntini di sospensione. Al contrario, il programma scorre automaticamente un elenco predefinito di colori. Il programma non supporta forme diverse da puntini di sospensione. Ovviamente, questo programma non riceverà alcun premi per il software di grafica. Tuttavia, è comunque un esempio utile da cui imparare. È possibile scaricare il codice sorgente completo da [Simple Drawing Sample](simple-drawing-sample.md). Questa sezione illustra solo alcune evidenziazioni.

I puntini di sospensione sono rappresentati nel programma da una struttura che contiene i dati dei puntini di sospensione ([**D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e il colore ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). La struttura definisce anche due metodi: un metodo per disegnare l'ellisse e un metodo per eseguire l'hit testing.


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



Il programma usa lo stesso pennello a tinta unita per disegnare il riempimento e il contorno per ogni ellisse, modificando il colore in base alle esigenze. In Direct2D la modifica del colore di un pennello a tinta unita è un'operazione efficiente. L'oggetto pennello a tinta unita supporta quindi un [**metodo SetColor.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)

I puntini di sospensione vengono archiviati in un **contenitore** elenco STL:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **shared \_ ptr** è una classe di puntatore intelligente aggiunta a C++ in TR1 e formalizzata in C++0x. Visual Studio 2010 aggiunge il supporto per **\_ pt** r condiviso e altre funzionalità di C++0x. Per altre informazioni, vedere [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

 

Il programma ha tre modalità:

-   Modalità di disegno. L'utente può disegnare nuovi puntini di sospensione.
-   Modalità di selezione. L'utente può selezionare un ellisse.
-   Modalità di trascinamento. L'utente può trascinare un ellisse selezionato.

L'utente può passare dalla modalità di disegno alla modalità di selezione usando gli stessi tasti di scelta rapida descritti in [Tabelle dei tasti di scelta rapida.](accelerator-tables.md) Dalla modalità di selezione, il programma passa alla modalità di trascinamento se l'utente fa clic su un ellisse. Torna alla modalità di selezione quando l'utente rilascia il pulsante del mouse. La selezione corrente viene archiviata come iteratore nell'elenco di puntini di sospensione. Il metodo helper `MainWindow::Selection` restituisce un puntatore all'ellisse selezionata oppure il valore **nullptr** se non è presente alcuna selezione.


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



La tabella seguente riepiloga gli effetti dell'input del mouse in ognuna delle tre modalità.



| Mouse Input      | Modalità disegno                                          | Modalità di selezione                                                                                                                               | Modalità di trascinamento                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Pulsante sinistro verso il basso | Impostare mouse capture e iniziare a disegnare un nuovo ellisse. | Rilasciare la selezione corrente ed eseguire un hit test. Se viene raggiunto un ellisse, acquisire il cursore, selezionare l'ellisse e passare alla modalità di trascinamento. | Nessuna azione.                 |
| Spostamento del mouse       | Se il pulsante sinistro è in basso, ridimensionare l'ellisse.    | Nessuna azione.                                                                                                                                   | Spostare l'ellisse selezionata. |
| Pulsante sinistro verso l'alto   | Interrompere il disegno dell'ellisse.                          | Nessuna azione.                                                                                                                                   | Passare alla modalità di selezione.  |



 

Il metodo seguente nella classe `MainWindow` gestisce i messaggi WM [**\_ LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown)


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



Le coordinate del mouse vengono passate a questo metodo in pixel e quindi convertite in DIP. È importante non confondere queste due unità. Ad esempio, la [**funzione DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa i pixel, mentre per il disegno e l'hit testing vengono utilizzati i DIP. La regola generale è che le funzioni correlate alle finestre o all'input del mouse usano i pixel, mentre Direct2D e DirectWrite usare DIP. Testare sempre il programma con un'impostazione DPI elevata e ricordare di contrassegnare il programma come in grado di riconoscere DPI. Per altre informazioni, vedere [DPI e Device-Independent Pixel.](dpi-and-device-independent-pixels.md)

Ecco il codice che gestisce i [**messaggi WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove)


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



La logica per ridimensionare un'ellisse è stata descritta in precedenza, nella sezione [Esempio: Disegno di cerchi](mouse-movement.md). Si noti anche la chiamata a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Ciò garantisce che la finestra sia ridisegnata. Il codice seguente gestisce i [**messaggi WM \_ LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup)


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



Come si può vedere, i gestori di messaggi per l'input del mouse hanno tutti codice di diramazione, a seconda della modalità corrente. Si tratta di una progettazione accettabile per questo programma piuttosto semplice. Tuttavia, potrebbe diventare rapidamente troppo complesso se vengono aggiunte nuove modalità. Per un programma più grande, un'architettura model-view-controller (MVC) potrebbe essere una progettazione migliore. In questo tipo di architettura, il *controller*, che gestisce l'input dell'utente, è separato dal modello *,* che gestisce i dati dell'applicazione.

Quando il programma cambia modalità, il cursore cambia per fornire feedback all'utente.


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



Infine, ricordarsi di impostare il cursore quando la finestra riceve un [**messaggio WM \_ SETCURSOR:**](/windows/desktop/menurc/wm-setcursor)


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>Riepilogo

In questo modulo si è appreso come gestire l'input del mouse e della tastiera. come definire i tasti di scelta rapida; e come aggiornare l'immagine del cursore per riflettere lo stato corrente del programma.

 

 
