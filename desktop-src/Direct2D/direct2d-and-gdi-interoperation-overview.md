---
title: Panoramica dell'interoperabilità di Direct2D e GDI
description: Viene descritto come usare Direct2D e GDI insieme.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, interoperatività GDI
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
- Direct3D, interoperabilità
- Direct3D, interoperatività Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729663"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Panoramica dell'interoperabilità di Direct2D e GDI

In questo argomento viene descritto come utilizzare contemporaneamente Direct2D e [GDI](/windows/desktop/gdi/windows-gdi) . Esistono due modi per combinare Direct2D con GDI: è possibile scrivere contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D oppure scrivere contenuto Direct2D in un [contesto di dispositivo GDI (DC)](/windows/desktop/gdi/device-contexts).

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Creare contenuto Direct2D in un contesto di dispositivo GDI](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, le trasformazioni GDI e le compilazioni del linguaggio da destra a sinistra di Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Disegnare contenuto GDI in una destinazione di rendering GDI-Compatible Direct2D](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

In questa panoramica si presuppone che l'utente abbia familiarità con le operazioni di disegno Direct2D di base. Per un'esercitazione, vedere la [Guida introduttiva di Direct2D](direct2d-quickstart.md). Si presuppone inoltre che l'utente abbia familiarità con le operazioni di disegno GDI.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Creare contenuto Direct2D in un contesto di dispositivo GDI

Per creare contenuto Direct2D in un controller di dominio GDI, usare un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Per creare una destinazione di rendering del controller di dominio, usare il metodo [**ID2D1Factory:: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) . Questo metodo accetta due parametri.

Il primo parametro, una struttura delle [**\_ proprietà della \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , specifica il rendering, la comunicazione remota, il formato dpi, il formato pixel e le informazioni sull'utilizzo. Per abilitare la destinazione di rendering del controller di dominio per l'utilizzo con GDI, impostare il formato DXGI su [DXGI \_ Format \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) e la modalità Alpha su [**d2d1 \_ Alpha Mode \_ \_ premoltiplicated**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o **d2d1 \_ Alpha \_ mode \_ Ignore**.

Il secondo parametro è l'indirizzo del puntatore che riceve il riferimento alla destinazione di rendering del controller di dominio.

Il codice seguente crea una destinazione di rendering del controller di dominio.


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



Nel codice precedente, *m \_ pD2DFactory* è un puntatore a un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pDCRT* è un puntatore a un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).

Prima di poter eseguire il rendering con la destinazione di rendering del controller di dominio, è necessario utilizzare il relativo metodo [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) per associarlo a un controller di dominio GDI. Questa operazione viene eseguita ogni volta che si utilizza un controller di dominio diverso o la dimensione dell'area che si desidera creare per le modifiche.

Il metodo [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) accetta due parametri, *HDC* e *pSubRect*. Il parametro *HDC* fornisce un handle per il contesto di dispositivo che riceve l'output della destinazione di rendering. Il parametro *pSubRect* è un rettangolo che descrive la parte del contesto di dispositivo in cui viene eseguito il rendering del contenuto. La destinazione del rendering del controller di dominio aggiorna le dimensioni in modo che corrispondano all'area del contesto del dispositivo descritta da *pSubRect*, qualora cambi la dimensione.

Il codice seguente associa un controller di dominio a una destinazione di rendering del controller di dominio.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



Dopo aver associato la destinazione di rendering del controller di dominio a un controller di dominio, è possibile usarla per disegnare. Il codice seguente disegna il contenuto Direct2D e GDI utilizzando un controller di dominio.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Questo codice produce output come illustrato nella figura seguente (sono stati aggiunti callout per evidenziare la differenza tra il rendering di Direct2D e GDI).

![illustrazione di due grafici circolari sottoposti a rendering con Direct2D e GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, le trasformazioni GDI e le compilazioni del linguaggio da destra a sinistra di Windows

Quando si usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), viene eseguito il rendering del contenuto Direct2D in una bitmap interna, quindi il rendering della bitmap viene eseguito nel controller di dominio con GDI.

GDI può applicare una trasformazione GDI (tramite il metodo [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) o un altro effetto allo stesso DC usato dalla destinazione di rendering, nel qual caso GDI trasforma la bitmap prodotta da Direct2D. L'uso di una trasformazione GDI per trasformare il contenuto Direct2D può compromettere la qualità visiva dell'output, perché si sta trasformando una bitmap per cui è già stato calcolato l'anti-aliasing e il posizionamento dei subpixel.

Si supponga, ad esempio, di usare la destinazione di rendering per disegnare una scena che contiene geometrie e testo con anti-aliasing. Se si usa una trasformazione GDI per applicare una trasformazione di ridimensionamento al controller di dominio e si ridimensiona la scena in modo che sia 10 volte più grande, verranno visualizzati i bordi di pixelzzazione e frastagliati. Se, tuttavia, è stata applicata una trasformazione simile mediante Direct2D, la qualità visiva della scena non sarebbe peggiorata.

In alcuni casi, potrebbe non essere evidente che GDI sta eseguendo un'elaborazione aggiuntiva che potrebbe peggiorare la qualità del contenuto Direct2D. Ad esempio, in una build di Windows da destra a sinistra (RTL), il contenuto di cui è stato eseguito il rendering da un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) potrebbe essere invertito orizzontalmente quando GDI lo copia nella destinazione. Se il contenuto è effettivamente invertito dipende dalle impostazioni correnti del controller di dominio.

A seconda del tipo di contenuto di cui viene eseguito il rendering, potrebbe essere necessario impedire l'inversione. Se il contenuto Direct2D include il testo ClearType, questa inversione ridurrà la qualità del testo.

È possibile controllare il comportamento di rendering RTL utilizzando la funzione GDI di [**selayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) . Per evitare il mirroring, chiamare la funzione GDI di **selayout** e specificare **layout \_ BITMAPORIENTATIONPRESERVED** come unico valore per il secondo parametro (non combinarlo con **layout \_ RTL**), come illustrato nell'esempio seguente:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Disegnare contenuto GDI in una destinazione di rendering GDI-Compatible Direct2D

Nella sezione precedente viene descritto come scrivere contenuto Direct2D in un controller di dominio GDI. È anche possibile scrivere contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D. Questo approccio è utile per le applicazioni che eseguono principalmente il rendering con Direct2D ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI.

Per eseguire il rendering del contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D, usare [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), che fornisce l'accesso a un contesto di dispositivo che può accettare chiamate di disegnare GDI. A differenza di altre interfacce, non viene creato direttamente un oggetto **ID2D1GdiInteropRenderTarget** . Usare invece il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di un'istanza di destinazione di rendering esistente. Nel codice seguente viene illustrato come eseguire questa operazione:


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



Nel codice precedente, *m \_ pD2DFactory* è un puntatore a un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pGDIRT* è un puntatore a un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).

Si noti che durante la creazione della destinazione di rendering compatibile con GDI GDI viene specificato il flag di [**\_ utilizzo della destinazione di rendering \_ \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Se è necessario un formato pixel, usare [DXGI \_ Format \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Se è richiesta una modalità Alpha, utilizzare la modalità [**\_ alfa d2d1 \_ \_ premoltiplicata**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o la **\_ modalità d2d1 Alpha \_ \_ Ignore**.

Si noti che il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ha sempre esito positivo. Per verificare se i metodi dell'interfaccia [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funzioneranno per una determinata destinazione di rendering, creare [**una \_ \_ \_ proprietà di destinazione di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) che specifichi la compatibilità GDI e il formato pixel appropriato, quindi chiamare il metodo IsValid della destinazione di rendering per verificare se la destinazione di rendering è compatibile con GDI. [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties))

Nell'esempio seguente viene illustrato come creare un grafico a torta (contenuto GDI) nella destinazione di rendering compatibile con GDI di HWND.


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



Il codice restituisce i grafici come illustrato nella figura seguente con i callout per evidenziare la differenza di qualità del rendering. Il grafico a torta a destra (contenuto GDI) ha una qualità di rendering inferiore rispetto al grafico a torta a sinistra (contenuto Direct2D). Questo perché Direct2D è in grado di eseguire il rendering con l'anti-aliasing

![illustrazione di due grafici circolari sottoposti a rendering in una destinazione di rendering compatibile con GDI Direct2D](images/gdicontentind2d.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Factory:: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**\_Proprietà di \_ destinazione di rendering d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[Contesti di dispositivo GDI](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[SDK PER GDI](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 