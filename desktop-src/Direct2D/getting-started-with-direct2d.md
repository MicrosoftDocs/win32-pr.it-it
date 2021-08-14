---
title: Guida introduttiva a Direct2D
description: Riepiloga i passaggi necessari per disegnare con Direct2D e fornisce codice di esempio.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Esempio di codice Direct2D,draw rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9c4f7ee6ca99feb3cf7169a59ce73ff3b8f8c62c08ddad88b9e5acf5d9a814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260067"
---
# <a name="direct2d-quickstart"></a>Guida introduttiva a Direct2D

Direct2D è un'API in modalità immediata e codice nativo per la creazione di grafica 2D. Questo argomento illustra come usare Direct2D all'interno di una tipica applicazione Win32 per disegnare in **un oggetto HWND.**

> [!Note]  
> Se si vuole creare un'app Windows Store che usa Direct2D, vedere l'argomento [Direct2D Quickstart for Windows 8.](direct2d-quickstart-with-device-context.md)

 

In questo argomento sono incluse le sezioni seguenti:

-   [Disegno di un rettangolo semplice](#drawing-a-simple-rectangle)
-   [Passaggio 1: Includere l'intestazione Direct2D](#step-1-include-direct2d-header)
-   [Passaggio 2: Creare un id2D1Factory](#step-2-create-an-id2d1factory)
-   [Passaggio 3: Creare un ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Passaggio 4: Creare un pennello](#step-4-create-a-brush)
-   [Passaggio 5: Disegnare il rettangolo](#step-5-draw-the-rectangle)
-   [Passaggio 6: Rilasciare le risorse](#step-6-release-resources)
-   [Creare una semplice applicazione Direct2D](#create-a-simple-direct2d-application)
-   [Argomenti correlati](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Disegno di un rettangolo semplice

Per disegnare un rettangolo usando [GDI,](/windows/desktop/gdi/windows-gdi)è possibile gestire il [**messaggio WM \_ PAINT,**](/windows/desktop/gdi/wm-paint) come illustrato nel codice seguente.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



Il codice per disegnare lo stesso rettangolo con Direct2D è simile: crea risorse di disegno, descrive una forma da disegnare, disegna la forma e quindi rilascia le risorse di disegno. Le sezioni seguenti descrivono in dettaglio ognuno di questi passaggi.

## <a name="step-1-include-direct2d-header"></a>Passaggio 1: Includere l'intestazione Direct2D

Oltre alle intestazioni necessarie per un'applicazione Win32, includere l'intestazione d2d1.h.

## <a name="step-2-create-an-id2d1factory"></a>Passaggio 2: Creare un id2D1Factory

Una delle prime operazioni che qualsiasi esempio Direct2D esegue è la creazione di [**un oggetto ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



[**L'interfaccia ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) è il punto di partenza per l'uso di Direct2D. usare **id2D1Factory per** creare risorse Direct2D.

Quando si crea una factory, è possibile specificare se è a thread singolo o a thread singolo. Per altre informazioni sulle factory multi-thread, vedere le osservazioni nella pagina di riferimento [**ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Questo esempio crea una factory a thread singolo.

In generale, l'applicazione deve creare la factory una sola volta e conservarla per tutta la durata dell'applicazione.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Passaggio 3: Creare un ID2D1HwndRenderTarget

Dopo aver creato una factory, usarla per creare una destinazione di rendering.


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



Una destinazione di rendering è un dispositivo che può eseguire operazioni di disegno e creare risorse di disegno dipendenti dal dispositivo, ad esempio pennelli. Diversi tipi di destinazioni di rendering eseguono il rendering in dispositivi diversi. Nell'esempio precedente viene utilizzato [**id2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), che esegue il rendering su una parte dello schermo.

Quando possibile, una destinazione di rendering usa la GPU per accelerare le operazioni di rendering e creare risorse di disegno. In caso contrario, la destinazione di rendering usa la CPU per elaborare le istruzioni di rendering e creare risorse. È possibile modificare questo comportamento usando i flag [**D2D1 \_ RENDER \_ TARGET \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) quando si crea la destinazione di rendering.

Il [**metodo CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) accetta tre parametri. Il primo parametro, uno struct [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) specifica le opzioni di visualizzazione remota, se forzare il rendering della destinazione di rendering nel software o nell'hardware e il valore DPI. Il codice in questo esempio usa la funzione helper [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) per accettare le proprietà predefinite della destinazione di rendering.

Il secondo parametro, uno struct [**D2D1 \_ HWND \_ RENDER TARGET \_ \_ PROPERTIES,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) specifica l'HWND di cui viene eseguito il rendering del contenuto, le dimensioni iniziali della destinazione di rendering (in pixel) e le relative opzioni di [**presentazione.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options)  In questo esempio viene utilizzata la funzione helper [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) per specificare HWND e le dimensioni iniziali. Usa le opzioni di presentazione predefinite.

Il terzo parametro è l'indirizzo del puntatore che riceve il riferimento alla destinazione di rendering.

Quando si crea una destinazione di rendering e l'accelerazione hardware è disponibile, si allocano risorse nella GPU del computer. Creando una destinazione di rendering una sola volta e mantenendola il più a lungo possibile, si ottengono vantaggi in termini di prestazioni. L'applicazione deve creare destinazioni di rendering una sola volta e tenerle per tutta la durata dell'applicazione o fino a quando non viene ricevuto l'errore [**D2DERR \_ RECREATE \_ TARGET.**](direct2d-error-codes.md) Quando viene visualizzato questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).

## <a name="step-4-create-a-brush"></a>Passaggio 4: Creare un pennello

Come una factory, una destinazione di rendering può creare risorse di disegno. In questo esempio la destinazione di rendering crea un pennello.


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



Un pennello è un oggetto che disegna un'area, ad esempio il tratto di una forma o il riempimento di una geometria. Il pennello in questo esempio disegna un'area con un colore a tinta unita predefinito, il nero.

Direct2D offre anche altri tipi di pennelli: pennelli sfumatura per disegnare sfumature lineari e radiali e un pennello bitmap per disegnare con bitmap e motivi.

Alcune API di disegno forniscono penna per disegnare contorni e pennelli per il riempimento delle forme. Direct2D è diverso: non fornisce un oggetto penna, ma usa un pennello per disegnare i contorni e riempire le forme. Quando si disegnano i contorni, usare [**l'interfaccia ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) con un pennello per controllare le operazioni di tracciamento del percorso.

Un pennello può essere usato solo con la destinazione di rendering che lo ha creato e con altre destinazioni di rendering nello stesso dominio di risorse. In generale, è consigliabile creare i pennelli una sola volta e conservarli per tutta la durata della destinazione di rendering che li ha creati. [**ID2D1SolidColorBrush è**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) l'eccezione solitaria; Poiché è relativamente economico creare, è possibile creare un **oggetto ID2D1SolidColorBrush** ogni volta che si disegna un frame, senza alcun impatto sulle prestazioni evidente. È anche possibile usare un singolo **oggetto ID2D1SolidColorBrush** e modificarne il colore ogni volta che lo si usa.

## <a name="step-5-draw-the-rectangle"></a>Passaggio 5: Disegnare il rettangolo

Usare quindi la destinazione di rendering per disegnare il rettangolo.


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



Il [**metodo DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accetta due parametri: il rettangolo da disegnare e il pennello da usare per disegnare il contorno del rettangolo. Facoltativamente, è anche possibile specificare le opzioni relative a larghezza del tratto, motivo tratteggiato, unione linea e estremità finale.

È necessario chiamare il [**metodo BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di eseguire qualsiasi comando di disegno ed è necessario chiamare il [**metodo EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver completato l'emissione dei comandi di disegno. Il **metodo EndDraw** restituisce un **HRESULT** che indica se i comandi di disegno hanno avuto esito positivo.

## <a name="step-6-release-resources"></a>Passaggio 6: Rilasciare le risorse

Quando non sono presenti altri fotogrammi da disegnare o quando viene visualizzato l'errore [**D2DERR \_ RECREATE \_ TARGET,**](direct2d-error-codes.md) rilasciare la destinazione di rendering e tutti i dispositivi creati.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Quando l'applicazione ha terminato di usare le risorse Direct2D (ad esempio quando sta per uscire), rilasciare la factory Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Creare una semplice applicazione Direct2D

Il codice in questo argomento illustra gli elementi di base di un'applicazione Direct2D. Per brevità, l'argomento omette il framework dell'applicazione e il codice di gestione degli errori caratteristica di un'applicazione ben scritta. Per una procedura dettagliata che illustra il codice completo per la creazione di una semplice applicazione Direct2D e illustra le procedure di progettazione consigliate, vedere Creazione di [un'applicazione Direct2D semplice.](direct2d-quickstart.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una semplice applicazione Direct2D](direct2d-quickstart.md)
</dt> </dl>

 

 