---
title: Guida introduttiva di Direct2D per Windows 8
description: Riepiloga i passaggi necessari per disegnare con Direct2D per Windows 8 e fornisce codice di esempio. Direct2D è un'API di codice nativo per la creazione di grafica 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, esempio di codice per disegnare un rettangolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406144"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Guida introduttiva di Direct2D per Windows 8

Direct2D è un'API in modalità immediata a codice nativo per la creazione di grafica 2D. Questo argomento illustra come usare Direct2D per disegnare in un oggetto [**Windows::UI::Core::CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)

In questo argomento sono incluse le sezioni seguenti:

-   [Disegno di un rettangolo semplice](#drawing-a-simple-rectangle)
-   [Passaggio 1: Includere l'intestazione Direct2D](#step-1-include-direct2d-header)
-   [Passaggio 2: Creare un oggetto ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Passaggio 3: Creare id2D1Device e ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Passaggio 4: Creare un pennello](#step-4-create-a-brush)
-   [Passaggio 5: Disegnare il rettangolo](#step-5-draw-the-rectangle)
-   [Codice di esempio](#example-code)

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



Il codice per disegnare lo stesso rettangolo con Direct2D è simile: crea risorse di disegno, descrive una forma da disegnare, disegna la forma, quindi rilascia le risorse di disegno. Le sezioni seguenti descrivono in dettaglio ognuno di questi passaggi.

## <a name="step-1-include-direct2d-header"></a>Passaggio 1: Includere l'intestazione Direct2D

Oltre alle intestazioni necessarie per l'applicazione, includere le intestazioni d2d1.h e d2d1 \_ 1.h.

## <a name="step-2-create-an-id2d1factory1"></a>Passaggio 2: Creare un oggetto ID2D1Factory1

Una delle prime operazioni che qualsiasi esempio direct2D esegue è la creazione di [**id2D1Factory1.**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



[**L'interfaccia ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) è il punto di partenza per l'uso di Direct2D; usare **id2D1Factory1** per creare risorse Direct2D.

Quando si crea una factory, è possibile specificare se è multi-thread o a thread singolo. Per altre informazioni sulle factory multi-thread, vedere le osservazioni nella pagina di riferimento [**di ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Questo esempio crea una factory a thread singolo.

In generale, l'applicazione deve creare la factory una sola volta e conservarla per tutta la durata dell'applicazione.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Passaggio 3: Creare id2D1Device e ID2D1DeviceContext

Dopo aver creato una factory, usarla per creare un dispositivo Direct2D e quindi usare il dispositivo per creare un contesto di dispositivo Direct2D. Per creare questi oggetti Direct2D, è necessario disporre di un dispositivo [**Direct3D 11,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) di un [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)e di una [**catena di scambio DXGI.**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) Per informazioni sulla creazione dei prerequisiti [necessari,](devices-and-device-contexts.md) vedere Dispositivi e contesti di dispositivo.


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Un contesto di dispositivo è un dispositivo che può eseguire operazioni di disegno e creare risorse di disegno dipendenti dal dispositivo, ad esempio i pennelli. Si usa anche il contesto di dispositivo per collegare un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a una superficie DXGI da usare come destinazione di rendering. Il rendering del contesto di dispositivo può essere eseguito in tipi diversi di destinazioni.

Il codice qui dichiara le proprietà per bitmap che si collegano a una catena di scambio DXGI di cui viene eseguito il rendering in [**un oggetto CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow) Il [**metodo ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) ottiene una superficie Direct2D dalla superficie DXGI. In questo modo viene eseguito il rendering di qualsiasi elemento di cui viene eseguito il rendering nell'oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) di destinazione sulla superficie della catena di scambio.

Dopo aver creato la superficie Direct2D, usa il metodo [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) per impostarla come destinazione di rendering attiva.


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>Passaggio 4: Creare un pennello

Analogamente a una factory, un contesto di dispositivo può creare risorse di disegno. In questo esempio il contesto di dispositivo crea un pennello.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Un pennello è un oggetto che disegna un'area, ad esempio il tratto di una forma o il riempimento di una geometria. Il pennello in questo esempio disegna un'area con un colore a tinta unita predefinito, il nero.

Direct2D offre anche altri tipi di pennelli: pennelli sfumatura per disegnare sfumature lineari e radiali, un [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) pennello [**bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per il disegno con bitmap e pattern e a partire da Windows 8, un pennello immagine per disegnare con un'immagine sottoposta a rendering.

Alcune API di disegno forniscono penne per disegnare contorni e pennelli per il riempimento delle forme. Direct2D è diverso: non fornisce un oggetto penna, ma usa un pennello per disegnare i contorni e riempire le forme. Quando si disegnano i contorni, usare l'interfaccia [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) o Windows 8 partire [**dall'interfaccia ID2D1StrokeStyle1,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) con un pennello per controllare le operazioni di selezione del percorso.

Un pennello può essere usato solo con la destinazione di rendering che lo ha creato e con altre destinazioni di rendering nello stesso dominio di risorse. In generale, è consigliabile creare i pennelli una sola volta e conservarli per tutta la durata della destinazione di rendering che li ha creati. [**ID2D1SolidColorBrush è**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) l'unica eccezione. Poiché è relativamente conveniente da creare, è possibile creare un **oggetto ID2D1SolidColorBrush** ogni volta che si disegna un frame, senza alcun impatto notevole sulle prestazioni. È anche possibile usare un singolo **oggetto ID2D1SolidColorBrush** e modificarne il colore o l'opacità ogni volta che lo si usa.

## <a name="step-5-draw-the-rectangle"></a>Passaggio 5: Disegnare il rettangolo

Usare quindi il contesto di dispositivo per disegnare il rettangolo.


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



Il [**metodo DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accetta due parametri: il rettangolo da disegnare e il pennello da usare per disegnare il contorno del rettangolo. Facoltativamente, è anche possibile specificare le opzioni relative a spessore tratto, motivo trattino, join di linee e estremità finale.

È necessario chiamare il [**metodo BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di eseguire qualsiasi comando di disegno ed è necessario chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver completato l'emissione dei comandi di disegno. Il **metodo EndDraw** restituisce un **HRESULT** che indica se i comandi di disegno sono riusciti. Se l'operazione non riesce, la funzione helper ThrowIfFailed genererà un'eccezione.

Il [**metodo IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) scambia la superficie del buffer con l'oggetto sulla superficie dello schermo per visualizzare il risultato.

## <a name="example-code"></a>Codice di esempio

Il codice in questo argomento illustra gli elementi di base di un'applicazione Direct2D. Per brevità, l'argomento omette il framework applicazione e il codice di gestione degli errori caratteristica di un'applicazione ben scritta.

 

 