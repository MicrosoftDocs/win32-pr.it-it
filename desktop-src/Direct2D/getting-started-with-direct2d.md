---
title: Avvio rapido di Direct2D
description: Vengono riepilogati i passaggi necessari per creare con Direct2D e viene fornito codice di esempio.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, esempio di codice rettangolo di richiamo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117803"
---
# <a name="direct2d-quickstart"></a>Avvio rapido di Direct2D

Direct2D è un'API in modalità immediata e di codice nativo per la creazione di immagini 2D. In questo argomento viene illustrato come utilizzare Direct2D all'interno di una tipica applicazione Win32 per creare un oggetto **HWND**.

> [!Note]  
> Se si vuole creare un'app di Windows Store che usa Direct2D, vedere l'argomento [avvio rapido di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md) .

 

In questo argomento sono incluse le sezioni seguenti:

-   [Disegno di un rettangolo semplice](#drawing-a-simple-rectangle)
-   [Passaggio 1: includere l'intestazione Direct2D](#step-1-include-direct2d-header)
-   [Passaggio 2: creare un ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Passaggio 3: creare un ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Passaggio 4: creare un pennello](#step-4-create-a-brush)
-   [Passaggio 5: creare il rettangolo](#step-5-draw-the-rectangle)
-   [Passaggio 6: rilasciare le risorse](#step-6-release-resources)
-   [Creare un'applicazione Direct2D semplice](#create-a-simple-direct2d-application)
-   [Argomenti correlati](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Disegno di un rettangolo semplice

Per disegnare un rettangolo utilizzando [GDI](/windows/desktop/gdi/windows-gdi), è possibile gestire il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) , come illustrato nel codice seguente.


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



Il codice per disegnare lo stesso rettangolo con Direct2D è simile: crea risorse di disegno, descrive una forma da disegnare, disegna la forma, quindi rilascia le risorse di disegno. Le sezioni seguenti descrivono ognuno di questi passaggi in dettaglio.

## <a name="step-1-include-direct2d-header"></a>Passaggio 1: includere l'intestazione Direct2D

Oltre alle intestazioni necessarie per un'applicazione Win32, includere l'intestazione d2d1. h.

## <a name="step-2-create-an-id2d1factory"></a>Passaggio 2: creare un ID2D1Factory

Uno dei primi elementi di un esempio Direct2D è creare un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



L'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) è il punto di partenza per l'utilizzo di Direct2D; usare un **ID2D1Factory** per creare risorse Direct2D.

Quando si crea una factory, è possibile specificare se è a thread multipli o a thread singolo. Per ulteriori informazioni sulle Factory multithread, vedere la sezione Osservazioni nella pagina di riferimento di [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory). In questo esempio viene creata una factory a thread singolo.

In generale, l'applicazione deve creare la Factory una volta e conservarla per la durata dell'applicazione.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Passaggio 3: creare un ID2D1HwndRenderTarget

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



Una destinazione di rendering è un dispositivo che può eseguire operazioni di disegno e creare risorse di disegno dipendenti dal dispositivo, ad esempio i pennelli. Diversi tipi di destinazioni di rendering eseguono il rendering in dispositivi diversi. Nell'esempio precedente viene usato un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), che esegue il rendering in una parte dello schermo.

Quando possibile, una destinazione di rendering usa la GPU per accelerare le operazioni di rendering e creare risorse di disegno. In caso contrario, la destinazione di rendering utilizza la CPU per elaborare le istruzioni di rendering e creare risorse. È possibile modificare questo comportamento usando i flag del [**\_ tipo di \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) quando si crea la destinazione di rendering.

Il metodo [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) accetta tre parametri. Il primo parametro, uno struct delle [**\_ proprietà della \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , specifica le opzioni di visualizzazione remote, se forzare il rendering della destinazione di rendering sul software o sull'hardware e sul valore dpi. Il codice in questo esempio usa la funzione helper [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) per accettare le proprietà di destinazione di rendering predefinite.

Il secondo parametro, uno struct delle [**proprietà della \_ \_ \_ destinazione \_ di rendering HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , specifica l' **HWND** a cui viene eseguito il rendering del contenuto, le dimensioni iniziali della destinazione di rendering (in pixel) e le relative [**Opzioni di presentazione**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options). In questo esempio viene usata la funzione helper [**D2D1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) per specificare HWND e dimensioni iniziali. Usa le opzioni di presentazione predefinite.

Il terzo parametro è l'indirizzo del puntatore che riceve il riferimento alla destinazione di rendering.

Quando si crea una destinazione di rendering e l'accelerazione hardware è disponibile, è necessario allocare risorse sulla GPU del computer. Creando una destinazione di rendering una volta e mantenendola il più a lungo possibile, si ottengono vantaggi in termini di prestazioni. L'applicazione deve creare le destinazioni di rendering una sola volta e mantenerle per la durata dell'applicazione o fino a quando non viene ricevuto l'errore di [**\_ \_ destinazione D2DERR ricreate**](direct2d-error-codes.md) . Quando si riceve questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).

## <a name="step-4-create-a-brush"></a>Passaggio 4: creare un pennello

Analogamente a una factory, una destinazione di rendering può creare risorse di disegno. In questo esempio, la destinazione di rendering crea un pennello.


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



Un pennello è un oggetto che disegna un'area, ad esempio il tratto di una forma o il riempimento di una geometria. Il pennello in questo esempio disegna un'area con un colore a tinta unita predefinito (nero).

Direct2D fornisce anche altri tipi di pennelli: pennelli sfumatura per il disegno di sfumature lineari e radiali e un pennello bitmap per la verniciatura con bitmap e pattern.

Alcune API di disegno forniscono penne per il disegno di strutture e pennelli per la compilazione di forme. Direct2D è diverso: non fornisce un oggetto Pen ma usa un pennello per il disegno di strutture e riempimento di forme. Quando si disegnano le strutture, usare l'interfaccia [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) con un pennello per controllare le operazioni di traccia del percorso.

Un pennello può essere usato solo con la destinazione di rendering che lo ha creato e con altre destinazioni di rendering nello stesso dominio delle risorse. In generale, è consigliabile creare pennelli una volta e conservarli per la durata della destinazione di rendering che li ha creati. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) è l'eccezione Lone; Poiché è relativamente economico creare, è possibile creare un **ID2D1SolidColorBrush** ogni volta che si crea un frame, senza alcun impatto significativo sulle prestazioni. È anche possibile usare un solo **ID2D1SolidColorBrush** e modificarne il colore ogni volta che viene usato.

## <a name="step-5-draw-the-rectangle"></a>Passaggio 5: creare il rettangolo

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



Il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accetta due parametri: il rettangolo da disegnare e il pennello da usare per disegnare il contorno del rettangolo. Facoltativamente, è anche possibile specificare le opzioni Larghezza tratto, motivo trattino, join a linee e estremità.

È necessario chiamare il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di eseguire qualsiasi comando di disegno ed è necessario chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver eseguito i comandi di disegno. Il metodo **EndDraw** restituisce un valore **HRESULT** che indica se i comandi di disegno hanno avuto esito positivo.

## <a name="step-6-release-resources"></a>Passaggio 6: rilasciare le risorse

Quando non sono più presenti frame da disegnare o quando si riceve l'errore [**D2DERR \_ ricrea \_ destinazione**](direct2d-error-codes.md) , rilasciare la destinazione di rendering e tutti i dispositivi creati.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Quando l'applicazione ha terminato di usare le risorse Direct2D, ad esempio quando sta per uscire, rilascia la factory Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Creare un'applicazione Direct2D semplice

Il codice in questo argomento illustra gli elementi di base di un'applicazione Direct2D. Per brevità, l'argomento omette il Framework dell'applicazione e il codice di gestione degli errori caratteristico di un'applicazione ben scritta. Per una procedura dettagliata più dettagliata che mostra il codice completo per la creazione di un'applicazione Direct2D semplice e illustra le procedure consigliate per la progettazione, vedere [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione Direct2D semplice](direct2d-quickstart.md)
</dt> </dl>

 

 