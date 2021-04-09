---
title: DPI e Device-Independent pixel
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Altre informazioni su: DPI e Device-Independent pixel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885305"
---
# <a name="dpi-and-device-independent-pixels"></a>DPI e Device-Independent pixel

Per programmare in modo efficace con la grafica di Windows, è necessario comprendere due concetti correlati:

-   Punti per pollice (DPI)
-   Pixel (DIP) indipendenti dal dispositivo.

Iniziamo con DPI. Questa operazione richiederà una breve deviazione nella tipografia. In tipografia la dimensione del tipo viene misurata in unità denominate *punti*. Un punto è uguale a 1/72 di pollice.

<dl> 1 PT = 1/72 pollice  
</dl>

> [!Note]  
> Si tratta della definizione di pubblicazione del desktop del punto. In passato, la misura esatta di un punto è cambiata.

 

Ad esempio, un tipo di carattere a 12 punti è progettato per adattarsi all'interno di una riga di testo di 1/6 "(12/72). Ovviamente, questo non significa che ogni carattere del tipo di carattere è esattamente 1/6 "Tall". Infatti, alcuni caratteri potrebbero essere più alti di 1/6 ". In molti tipi di carattere, ad esempio, il carattere Å è più alto dell'altezza nominale del tipo di carattere. Per la visualizzazione corretta, il tipo di carattere necessita di spazio aggiuntivo tra il testo. Questo spazio è denominato " *Leading*".

Nella figura seguente viene illustrato un tipo di carattere a 72 punti. Le linee continue mostrano un "rettangolo di delimitazione" di altezza intorno al testo. La linea tratteggiata è detta *baseline*. La maggior parte dei caratteri di un tipo di carattere nella linea di base. L'altezza del tipo di carattere include la parte sopra la linea di base (l' *ascesa*) e la parte sotto la linea di base (la *discesa*). Nel tipo di carattere riportato di seguito, l'ascesa è pari a 56 punti e la discesa è 16 punti.

![illustrazione che mostra un tipo di carattere a 72 punti.](images/graphics11.png)

Per quanto riguarda la visualizzazione di un computer, tuttavia, la misurazione delle dimensioni del testo è problematica, perché i pixel non hanno tutte le stesse dimensioni. Le dimensioni di un pixel dipendono da due fattori: la risoluzione dello schermo e le dimensioni fisiche del monitoraggio. Pertanto, i pollici fisici non sono una misura utile, perché non esiste una relazione fissa tra i pollici e i pixel fisici. I tipi di carattere vengono invece misurati in unità *logiche* . Un tipo di carattere a 72 punti viene definito come un pollice logico di altezza. I pollici logici vengono quindi convertiti in pixel. Per molti anni, Windows usava la seguente conversione: un pollice logico equivale a 96 pixel. Utilizzando questo fattore di scala, viene eseguito il rendering di un tipo di carattere a 72 punti come 96 pixel di altezza. Un tipo di carattere A 12 punti è di 16 pixel di altezza.

<dl> 12 punti = 12/72 pollice logico = 1/6 pollice logico = 96/6 pixel = 16 pixel  
</dl>

Questo fattore di scala viene descritto come 96 punti per pollice (DPI). I punti dei termini derivano dalla stampa, in cui i punti di input fisici vengono inseriti su carta. Per gli schermi dei computer, sarebbe più accurato indicare 96 pixel per ogni pollice logico, ma il termine DPI si è bloccato.

Poiché le dimensioni effettive dei pixel variano, il testo leggibile su un monitor potrebbe essere troppo piccolo su un altro monitor. Inoltre, le persone hanno preferenze diverse: alcune persone preferiscono un testo più grande. Per questo motivo, Windows consente all'utente di modificare l'impostazione DPI. Se, ad esempio, l'utente imposta la visualizzazione su 144 DPI, un tipo di carattere a 72 è 144 pixel di altezza. Le impostazioni DPI standard sono 100% (96 DPI), 125% (120 DPI) e 150% (144 DPI). L'utente può anche applicare un'impostazione personalizzata. A partire da Windows 7, DPI è un'impostazione per utente.

## <a name="dwm-scaling"></a>Ridimensionamento di DWM

Se un programma non tiene conto di DPI, i difetti seguenti potrebbero essere evidenti con impostazioni DPI elevate:

-   Elementi dell'interfaccia utente ritagliati.
-   Layout non corretto.
-   Bitmap e icone pixel.
-   Coordinate del mouse non corrette, che possono influire sull'hit test, il trascinamento della selezione e così via.

Per assicurarsi che i programmi meno recenti funzionino con impostazioni DPI elevate, DWM implementa un utile fallback. Se un programma non è contrassegnato come DPI compatibile, DWM ridimensiona l'intera interfaccia utente in modo che corrisponda all'impostazione DPI. Ad esempio, a 144 DPI, l'interfaccia utente viene ridimensionata del 150%, inclusi testo, elementi grafici, controlli e dimensioni della finestra. Se il programma crea una finestra 500 × 500, la finestra viene effettivamente visualizzata come 750 × 750 pixel e il contenuto della finestra viene ridimensionato di conseguenza.

Questo comportamento indica che i programmi meno recenti "semplicemente funzionano" con impostazioni DPI elevate. Tuttavia, il ridimensionamento determina anche un aspetto sfocato, perché il ridimensionamento viene applicato dopo che la finestra è stata disegnata.

## <a name="dpi-aware-applications"></a>Applicazioni DPI-Aware

Per evitare il ridimensionamento di DWM, un programma può contrassegnarsi come compatibile con DPI. In questo modo si indica a DWM di non eseguire alcun ridimensionamento DPI automatico. Tutte le nuove applicazioni devono essere progettate in modo da essere compatibili con DPI, perché la consapevolezza DPI migliora l'aspetto dell'interfaccia utente con impostazioni DPI più elevate.

Un programma dichiara autonomamente il riconoscimento DPI tramite il manifesto dell'applicazione. Un *manifesto* è semplicemente un file XML che descrive una dll o un'applicazione. Il manifesto è in genere incorporato nel file eseguibile, sebbene possa essere fornito come file separato. Un manifesto contiene informazioni quali le dipendenze DLL, il livello di privilegio richiesto e la versione di Windows per cui è stato progettato il programma.

Per dichiarare che il programma è compatibile con DPI, includere nel manifesto le informazioni seguenti.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

L'elenco riportato di seguito è solo un manifesto parziale, ma il linker di Visual Studio genera automaticamente il resto del manifesto. Per includere un manifesto parziale nel progetto, seguire questa procedura in Visual Studio.

1.  Scegliere **Proprietà** dal menu **progetto** .
2.  Nel riquadro sinistro espandere Proprietà di **configurazione**, espandere **strumento Manifesto**, quindi fare clic su **input e output**.
3.  Nella casella di testo **file manifesto aggiuntivi** Digitare il nome del file manifesto, quindi fare clic su **OK**.

Contrassegnando il programma come compatibile con DPI, si indica a DWM di non ridimensionare la finestra dell'applicazione. A questo punto, se si crea una finestra 500 × 500, la finestra occuperà 500 × 500 pixel, indipendentemente dall'impostazione DPI dell'utente.

## <a name="gdi-and-dpi"></a>GDI e DPI

Il disegno GDI viene misurato in pixel. Ciò significa che se il programma è contrassegnato come compatibile con DPI e si chiede a GDI di creare un rettangolo 200 × 100, il rettangolo risultante sarà 200 pixel di larghezza e 100 pixel di altezza sullo schermo. Tuttavia, le dimensioni dei tipi di carattere GDI vengono ridimensionate all'impostazione DPI corrente. In altre parole, se si crea un tipo di carattere a 72 punti, la dimensione del tipo di carattere sarà 96 pixel a 96 DPI, ma 144 pixel a 144 DPI. Di seguito è riportato un tipo di carattere a 72 punti sottoposto a rendering a 144 DPI con GDI.

![diagramma che mostra il ridimensionamento del tipo di carattere dpi in GDI.](images/graphics12.png)

Se l'applicazione è compatibile con DPI e si usa GDI per il disegno, ridimensionare tutte le coordinate del disegno in modo che corrispondano al valore DPI.

## <a name="direct2d-and-dpi"></a>Direct2D e DPI

Direct2D esegue automaticamente il ridimensionamento in base all'impostazione DPI. In Direct2D le coordinate sono misurate in unità denominate DIP ( *device independent pixel* ). Un DIP viene definito come 1/1/96 di un pollice *logico* . In Direct2D tutte le operazioni di disegno vengono specificate in DIP e quindi ridimensionate all'impostazione DPI corrente.



| Impostazione DPI | Dimensioni DIP    |
|-------------|-------------|
| 96          | 1 pixel     |
| 120         | 1,25 pixel |
| 144         | 1,5 pixel  |



 

Se, ad esempio, l'impostazione DPI dell'utente è 144 DPI e si chiede a Direct2D di creare un rettangolo 200 × 100, il rettangolo sarà 300 × 150 pixel fisici. DirectWrite, inoltre, misura le dimensioni dei caratteri in DIP, anziché in punti. Per creare un tipo di carattere a 12 punti, specificare 16 DIP (12 punti = 1/6 Logical inch = 96/6 DIP). Quando il testo viene disegnato sullo schermo, Direct2D converte i dip in pixel fisici. Il vantaggio di questo sistema è che le unità di misura sono coerenti sia per il testo che per il disegno, indipendentemente dall'impostazione DPI corrente.

Una parola di attenzione: le coordinate del mouse e della finestra vengono ancora fornite in pixel fisici, non in DIP. Ad esempio, se si elabora il messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , la posizione del mouse viene specificata in pixel fisici. Per creare un punto in quella posizione, è necessario convertire le coordinate dei pixel in DIP.

## <a name="converting-physical-pixels-to-dips"></a>Conversione di pixel fisici in DIP

La conversione da pixel fisici a dip usa la formula seguente.

<dl> DIP = pixel/(DPI/96.0)  
</dl>

Per ottenere l'impostazione DPI, chiamare il metodo [**ID2D1Factory:: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) . Il valore DPI viene restituito come due valori a virgola mobile, uno per l'asse x e uno per l'asse y. In teoria, questi valori possono variare. Calcolare un fattore di scala separato per ogni asse.


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



Ecco un metodo alternativo per ottenere l'impostazione DPI se non si usa Direct2D:


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> In Windows 10 la versione 1903,  [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) è deprecata e la raccomandazione è [**DisplayInformation:: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) per le app di Windows Store o [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) per le app desktop. Se si vuole comunque usarlo, non visualizzare più il messaggio di errore del compilatore scrivendo la riga [**#pragma avviso (Elimina: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) immediatamente prima della chiamata a [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) . Sebbene non sia consigliato, è possibile impostare la consapevolezza DPI predefinita a livello di codice usando [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext). Una volta creata una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata. Se si imposta la modalità di riconoscimento DPI predefinita del processo a livello di codice, è necessario chiamare l'API corrispondente prima che siano stati creati HWND. Per informazioni, vedere [impostazione della consapevolezza DPI predefinita per un processo](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).

## <a name="resizing-the-render-target"></a>Ridimensionamento della destinazione di rendering

Se le dimensioni della finestra cambiano, è necessario ridimensionare la destinazione di rendering in modo che corrisponda. Nella maggior parte dei casi, sarà necessario aggiornare anche il layout e ridisegnare la finestra. Nel codice seguente vengono illustrati questi passaggi.


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



La funzione [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) ottiene la nuova dimensione dell'area client, in pixel fisici (non DIP). Il metodo [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) aggiorna la dimensione della destinazione di rendering, specificata anche in pixel. La funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) forza un ridisegno aggiungendo l'intera area client all'area di aggiornamento della finestra. (Vedere [disegnare la finestra](painting-the-window.md), nel modulo 1).

Quando la finestra si espande o si riduce, in genere è necessario ricalcolare la posizione degli oggetti da creare. Ad esempio, nel programma Circle è necessario aggiornare il raggio e il punto centrale:


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



Il metodo [**ID2D1RenderTarget:: GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) restituisce le dimensioni della destinazione di rendering in DIP (non pixel), che è l'unità appropriata per il calcolo del layout. Esiste un metodo strettamente correlato, [**ID2D1RenderTarget:: GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), che restituisce le dimensioni in pixel fisici. Per una destinazione di rendering **HWND** , questo valore corrisponde alle dimensioni restituite da [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect). Tenere tuttavia presente che il disegno viene eseguito in DIP, non in pixel.

## <a name="next"></a>Prossima

[Uso del colore in Direct2D](using-color-in-direct2d.md)

 

 
