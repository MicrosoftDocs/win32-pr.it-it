---
title: DPI e Device-Independent pixel
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Altre informazioni su: DPI e pixel Device-Independent pixel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9b3aebca97ac466f5158b07d1d976994030b4ba2c83b361a5d7a6d88b572fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388349"
---
# <a name="dpi-and-device-independent-pixels"></a>DPI e Device-Independent pixel

Per programmare in modo efficace Windows grafica, è necessario comprendere due concetti correlati:

-   Punti per pollice (DPI)
-   DIP (Device-Independent Pixel).

Si inizierà con DPI. Ciò richiederà una breve deviazione nella tipografia. Nella tipografia, le dimensioni del tipo vengono misurate in unità denominate *punti*. Un punto è uguale a 1/72 di pollice.

<dl> 1 pt = 1/72 pollice  
</dl>

> [!Note]  
> Questa è la definizione di desktop publishing di point. In una cronologia, la misura esatta di un punto è variata.

 

Ad esempio, un tipo di carattere a 12 punti è progettato per rientrare in una riga di testo di 1/6" (12/72). Ovviamente, questo non significa che ogni carattere nel tipo di carattere sia esattamente alto 1/6". In realtà, alcuni caratteri potrebbero essere più alti di 1/6". Ad esempio, in molti tipi di carattere il carattere Å è più alto dell'altezza nominale del tipo di carattere. Per essere visualizzato correttamente, il tipo di carattere richiede spazio aggiuntivo tra il testo. Questo spazio è denominato *iniziale.*

La figura seguente mostra un tipo di carattere a 72 punti. Le linee a tinta unita mostrano un rettangolo di selezione alto 1" intorno al testo. La linea tratteggiata è denominata *linea di base*. La maggior parte dei caratteri in un tipo di carattere si basa sulla linea di base. L'altezza del tipo di carattere include la parte sopra la linea di base *(l'ascent*) e la parte sotto la linea di base (la *discesa*). Nel tipo di carattere illustrato di seguito, l'ascent è di 56 punti e la discesa è di 16 punti.

![figura che mostra un tipo di carattere a 72 punti.](images/graphics11.png)

Per quanto riguarda lo schermo di un computer, tuttavia, la misurazione delle dimensioni del testo è problematica, perché i pixel non hanno tutte le stesse dimensioni. Le dimensioni di un pixel dipendono da due fattori: la risoluzione dello schermo e le dimensioni fisiche del monitor. Pertanto, i pollici fisici non sono una misura utile, perché non esiste una relazione fissa tra pollici e pixel fisici. I tipi di carattere vengono invece misurati in *unità* logiche. Un tipo di carattere a 72 punti è definito come un pollice logico di altezza. I pollici logici vengono quindi convertiti in pixel. Per molti anni, Windows usata la conversione seguente: Un pollice logico è uguale a 96 pixel. Usando questo fattore di scala, viene eseguito il rendering di un tipo di carattere di 72 punti con un'altezza di 96 pixel. Un tipo di carattere a 12 punti ha un'altezza di 16 pixel.

<dl> 12 punti = 12/72 pollice logico = 1/6 pollice logico = 96/6 pixel = 16 pixel  
</dl>

Questo fattore di scala è descritto come 96 punti per pollice (DPI). Il termine punti deriva dalla stampa, in cui i punti fisici dell'input penna vengono inseriti sulla carta. Per gli schermi del computer, sarebbe più preciso pronunciare 96 pixel per pollice logico, ma il termine DPI si è bloccato.

Poiché le dimensioni effettive dei pixel variano, il testo leggibile su un monitor potrebbe essere troppo piccolo su un altro monitor. Inoltre, le persone hanno preferenze diverse, alcune preferiscono un testo più grande. Per questo motivo, Windows consente all'utente di modificare l'impostazione DPI. Ad esempio, se l'utente imposta la visualizzazione su 144 DPI, un tipo di carattere a 72 punti ha un'altezza di 144 pixel. Le impostazioni DPI standard sono 100% (96 DPI), 125% (120 DPI) e 150% (144 DPI). L'utente può anche applicare un'impostazione personalizzata. A partire Windows 7, il valore DPI è un'impostazione per utente.

## <a name="dwm-scaling"></a>Ridimensionamento DWM

Se un programma non fa conto di DPI, i seguenti difetti potrebbero essere evidenti nelle impostazioni con valori DPI alti:

-   Elementi dell'interfaccia utente ritagliati.
-   Layout non corretto.
-   Bitmap e icone pixelate.
-   Coordinate del mouse non corrette, che possono influire sull'hit testing, sul trascinamento della selezione e così via.

Per garantire che i programmi meno recenti funzionino con impostazioni con valori DPI elevati, DWM implementa un fallback utile. Se un programma non è contrassegnato come in grado di riconoscere DPI, DWM ridimensiona l'intera interfaccia utente in modo che corrisponda all'impostazione DPI. Ad esempio, con 144 DPI, l'interfaccia utente viene ridimensionata del 150%, inclusi testo, grafica, controlli e dimensioni delle finestre. Se il programma crea una finestra di 500 × 500, la finestra viene effettivamente visualizzata come 750 × 750 pixel e il contenuto della finestra viene ridimensionato di conseguenza.

Questo comportamento significa che i programmi meno recenti "funzionano solo" con le impostazioni con valori DPI alti. Tuttavia, il ridimensionamento ha anche un aspetto leggermente sfocato, perché il ridimensionamento viene applicato dopo che la finestra è stata disegnata.

## <a name="dpi-aware-applications"></a>DPI-Aware applicazioni

Per evitare il ridimensionamento DWM, un programma può contrassegnarsi come in grado di riconoscere DPI. Questo indica al DWM di non eseguire alcun ridimensionamento DPI automatico. Tutte le nuove applicazioni devono essere progettate per essere in grado di riconoscere DPI, perché la sensibilità DPI migliora l'aspetto dell'interfaccia utente con impostazioni DPI superiori.

Un programma si dichiara in grado di riconoscere DPI tramite il manifesto dell'applicazione. Un *manifesto* è semplicemente un file XML che descrive una DLL o un'applicazione. Il manifesto è in genere incorporato nel file eseguibile, anche se può essere fornito come file separato. Un manifesto contiene informazioni quali le dipendenze dll, il livello di privilegio richiesto e la versione di Windows per cui è stato progettato il programma.

Per dichiarare che il programma è in grado di riconoscere DPI, includere le informazioni seguenti nel manifesto.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

L'elenco illustrato di seguito è solo un manifesto parziale, ma Visual Studio linker genera automaticamente il resto del manifesto. Per includere un manifesto parziale nel progetto, seguire questa procedura in Visual Studio.

1.  Nel menu **Project** fare clic su **Proprietà**.
2.  Nel riquadro sinistro espandere **Proprietà** di configurazione , Espandere Strumento **Manifesto**, quindi fare clic su Input **e output**.
3.  Nella casella **di testo File manifesto** aggiuntivi digitare il nome del file manifesto e quindi fare clic su **OK.**

Contrassegnando il programma come in grado di riconoscere DPI, si indica al DWM di non ridimensionare la finestra dell'applicazione. Se ora si crea una finestra di 500 × 500, la finestra occuperà 500 × 500 pixel, indipendentemente dall'impostazione DPI dell'utente.

## <a name="gdi-and-dpi"></a>GDI e DPI

Il disegno GDI è misurato in pixel. Ciò significa che se il programma è contrassegnato come in grado di riconoscere DPI e si chiede a GDI di disegnare un rettangolo di 200 × 100, il rettangolo risultante sarà di 200 pixel di larghezza e 100 pixel di altezza sullo schermo. Tuttavia, le dimensioni dei caratteri GDI vengono ridimensionate in base all'impostazione DPI corrente. In altre parole, se si crea un tipo di carattere a 72 punti, le dimensioni del tipo di carattere saranno di 96 pixel con 96 DPI, ma di 144 pixel a 144 DPI. Ecco un tipo di carattere a 72 punti di cui viene eseguito il rendering a 144 DPI con GDI.

![diagramma che mostra il ridimensionamento del tipo di carattere dpi in gdi.](images/graphics12.png)

Se l'applicazione è in grado di riconoscere DPI e si usa GDI per il disegno, ridimensionare tutte le coordinate di disegno in modo che corrispondano al valore DPI.

## <a name="direct2d-and-dpi"></a>Direct2D e DPI

Direct2D esegue automaticamente il ridimensionamento in base all'impostazione DPI. In Direct2D le coordinate vengono misurate in unità denominate DIP *(Device Independent Pixel).* Un DIP è definito come 1/96 di *pollice* logico. In Direct2D tutte le operazioni di disegno vengono specificate in DIP e quindi ridimensionate in base all'impostazione DPI corrente.



| Impostazione DPI | Dimensioni DIP    |
|-------------|-------------|
| 96          | 1 pixel     |
| 120         | 1,25 pixel |
| 144         | 1,5 pixel  |



 

Ad esempio, se l'impostazione DPI dell'utente è 144 DPI e si chiede a Direct2D di disegnare un rettangolo di 200 × 100, il rettangolo sarà di 300 × 150 pixel fisici. Inoltre, la DirectWrite misura le dimensioni dei caratteri in DIP anziché nei punti. Per creare un tipo di carattere a 12 punti, specificare 16 DIP (12 punti = 1/6 pollice logico = 96/6 DIP). Quando il testo viene disegnato sullo schermo, Direct2D converte i DIP in pixel fisici. Il vantaggio di questo sistema è che le unità di misura sono coerenti sia per il testo che per il disegno, indipendentemente dall'impostazione DPI corrente.

Attenzione: le coordinate del mouse e della finestra sono ancora espresse in pixel fisici, non in DIP. Ad esempio, se si elabora il [**messaggio WM \_ LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) la posizione del mouse verso il basso viene specificata in pixel fisici. Per disegnare un punto in tale posizione, è necessario convertire le coordinate pixel in DIP.

## <a name="converting-physical-pixels-to-dips"></a>Conversione di pixel fisici in DIP

La conversione da pixel fisici a DIP usa la formula seguente.

<dl> DIP = pixel / (DPI/96.0)  
</dl>

Per ottenere l'impostazione DPI, chiamare il [**metodo ID2D1Factory::GetDesktopDpi.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) Il valore DPI viene restituito come due valori a virgola mobile, uno per l'asse x e uno per l'asse y. In teoria, questi valori possono differire. Calcolare un fattore di scala separato per ogni asse.


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



Ecco un modo alternativo per ottenere l'impostazione DPI se non si usa Direct2D:


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
> In Windows 10 versione 1903, [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) è deprecato e la raccomandazione è [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) per le app di Windows Store [**o GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) per le app desktop. Se si vuole comunque usarlo, eliminare il messaggio di errore del compilatore scrivendo la riga [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) subito prima della chiamata [**ID2D1Factory::GetDesktopDpi.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) Anche se non è consigliabile, è possibile impostare la consapevolezza DPI predefinita a livello di codice usando [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext). Dopo aver creato una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata. Se si imposta la modalità di riconoscimento DPI predefinito del processo a livello di codice, è necessario chiamare l'API corrispondente prima che siano stati creati HWND. Per informazioni, vedere [Impostazione del riconoscimento DPI predefinito per un processo](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).

## <a name="resizing-the-render-target"></a>Ridimensionamento della destinazione di rendering

Se le dimensioni della finestra cambiano, è necessario ridimensionare la destinazione di rendering in modo che corrisponda. Nella maggior parte dei casi, è anche necessario aggiornare il layout e ridisegnare la finestra. Il codice seguente illustra questi passaggi.


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



La [**funzione GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) ottiene le nuove dimensioni dell'area client, in pixel fisici (non DIP). Il [**metodo ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) aggiorna le dimensioni della destinazione di rendering, specificate anche in pixel. La [**funzione InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) forza il ridisegno aggiungendo l'intera area client all'area di aggiornamento della finestra. Vedere [Disegno della finestra](painting-the-window.md)nel modulo 1.

Con l'aumentare o la riduzione della finestra, in genere è necessario ricalcolare la posizione degli oggetti di disegno. Nel programma circle, ad esempio, il raggio e il punto centrale devono essere aggiornati:


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



Il [**metodo ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) restituisce le dimensioni della destinazione di rendering in DIP (non in pixel), che è l'unità appropriata per il calcolo del layout. Esiste un metodo strettamente correlato, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), che restituisce le dimensioni in pixel fisici. Per una destinazione di rendering **HWND,** questo valore corrisponde alle dimensioni restituite da [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect). Tenere tuttavia presente che il disegno viene eseguito in DIP, non in pixel.

## <a name="next"></a>Prossima

[Uso del colore in Direct2D](using-color-in-direct2d.md)

 

 
