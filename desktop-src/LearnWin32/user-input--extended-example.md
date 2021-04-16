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
# <a name="user-input-extended-example"></a>Input utente: esempio esteso

È possibile combinare tutto ciò che è stato appreso sull'input dell'utente per creare un semplice programma di disegno. Ecco uno screenshot del programma:

![screenshot del programma di disegno](images/input03.png)

L'utente può creare puntini di sospensione in diversi colori e selezionare, spostare o eliminare ellissi. Per semplificare l'interfaccia utente, il programma non consente all'utente di selezionare i colori dell'ellisse. Al contrario, il programma scorre automaticamente un elenco predefinito di colori. Il programma non supporta alcuna forma diversa dai puntini di sospensione. Ovviamente, questo programma non vincerà alcun premio per il software grafico. Tuttavia, è ancora un esempio utile per imparare da. È possibile scaricare il codice sorgente completo da [esempio di disegno semplice](simple-drawing-sample.md). In questa sezione vengono illustrate solo alcune novità.

I puntini di sospensione sono rappresentati nel programma da una struttura che contiene i dati dell'ellisse ([**d2d1 \_ ellisse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e il colore ([**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). La struttura definisce inoltre due metodi: un metodo per creare l'ellisse e un metodo per eseguire l'hit testing.


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



Il programma usa lo stesso pennello a tinta unita per disegnare il riempimento e il contorno per ogni ellisse, modificando il colore in base alle esigenze. In Direct2D, la modifica del colore di un pennello a tinta unita è un'operazione efficiente. Quindi, l'oggetto pennello a tinta unita supporta un metodo [**Secolor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .

I puntini di sospensione vengono archiviati in un contenitore **elenco** STL:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **il \_ ptr condiviso** è una classe di puntatore intelligente che è stata aggiunta a C++ in TR1 e formalizzata in C + + 0x. Visual Studio 2010 aggiunge il supporto **per \_ PT r condiviso** e altre funzionalità di C + + 0x. Per ulteriori informazioni, vedere la pagina relativa all' [esplorazione delle nuove funzionalità C++ e MFC in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

 

Il programma prevede tre modalità:

-   Modalità di estrazione. L'utente può creare nuovi ellissi.
-   Modalità di selezione. L'utente può selezionare un'ellisse.
-   Modalità di trascinamento. L'utente può trascinare un'ellisse selezionata.

L'utente può passare dalla modalità di estrazione alla modalità di selezione e viceversa usando gli stessi tasti di scelta rapida descritti nelle [tabelle dei tasti di scelta rapida](accelerator-tables.md). Dalla modalità di selezione, il programma passa alla modalità di trascinamento se l'utente fa clic su un'ellisse. Torna alla modalità di selezione quando l'utente rilascia il pulsante del mouse. La selezione corrente viene archiviata come iteratore nell'elenco di ellissi. Il metodo helper `MainWindow::Selection` restituisce un puntatore all'ellisse selezionata oppure il valore **nullptr** se non è presente alcuna selezione.


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



Nella tabella seguente sono riepilogati gli effetti dell'input del mouse in ognuna delle tre modalità.



| Input del mouse      | Modalità di estrazione                                          | Modalità di selezione                                                                                                                               | Modalità di trascinamento                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Pulsante sinistro | Impostare l'acquisizione del mouse e iniziare a creare una nuova ellisse. | Rilascia la selezione corrente ed esegue un hit test. Se viene raggiunta un'ellisse, Acquisisci il cursore, seleziona l'ellisse e passa alla modalità di trascinamento. | Nessuna azione.                 |
| Spostamento del mouse       | Se il pulsante sinistro è inattivo, ridimensionare l'ellisse.    | Nessuna azione.                                                                                                                                   | Spostare l'ellisse selezionata. |
| Pulsante a sinistra in alto   | Arresta il disegno dell'ellisse.                          | Nessuna azione.                                                                                                                                   | Passa alla modalità di selezione.  |



 

Il metodo seguente nella `MainWindow` classe gestisce i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .


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



Le coordinate del mouse vengono passate a questo metodo in pixel, quindi convertite in DIP. È importante non confondere queste due unità. Ad esempio, la funzione [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa i pixel, ma il disegno e l'hit testing usano DIP. La regola generale è che le funzioni correlate all'input di Windows o del mouse utilizzano pixel, mentre Direct2D e DirectWrite utilizzano DIP. Testare sempre il programma con impostazioni DPI elevate e ricordarsi di contrassegnare il programma come compatibile con DPI. Per ulteriori informazioni, vedere [dpi e Device-Independent pixel](dpi-and-device-independent-pixels.md).

Ecco il codice che gestisce i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .


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



La logica per ridimensionare un'ellisse è stata descritta in precedenza, nella sezione [esempio: disegno dei cerchi](mouse-movement.md). Si noti inoltre la chiamata a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). In questo modo si garantisce che la finestra venga ridisegnata. Il codice seguente gestisce i messaggi [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .


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



Come si può notare, i gestori di messaggi per l'input del mouse hanno tutti il codice di diramazione, a seconda della modalità corrente. Si tratta di un progetto accettabile per questo programma piuttosto semplice. Tuttavia, potrebbe diventare rapidamente troppo complesso se vengono aggiunte nuove modalità. Per un programma più ampio, un'architettura MVC (Model-View-Controller) potrebbe essere una progettazione migliore. In questo tipo di architettura, il *controller*, che gestisce l'input dell'utente, è separato dal *modello*, che gestisce i dati dell'applicazione.

Quando il programma commuta le modalità, il cursore cambia per fornire commenti e suggerimenti all'utente.


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



Infine, ricordarsi di impostare il cursore quando la finestra riceve un messaggio di [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) :


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

In questo modulo si è appreso come gestire l'input del mouse e della tastiera; come definire i tasti di scelta rapida; e come aggiornare l'immagine del cursore in modo da riflettere lo stato corrente del programma.

 

 