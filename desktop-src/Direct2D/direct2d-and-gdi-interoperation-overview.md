---
title: Cenni preliminari sull'interoperabilità di Direct2D e GDI
description: Descrive come usare Direct2D e GDI insieme.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, interoperatività GDI
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
- Direct3D, interoperabilità
- Interoperatività Direct3D,Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1f3be132aba742eb1df4b8a893dad245f851a0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631563"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Cenni preliminari sull'interoperabilità di Direct2D e GDI

Questo argomento descrive come usare Direct2D e [GDI](/windows/desktop/gdi/windows-gdi) insieme. Esistono due modi per combinare Direct2D con GDI: è possibile scrivere contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D oppure scrivere contenuto Direct2D in un contesto di dispositivo [GDI](/windows/desktop/gdi/device-contexts).

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Disegnare contenuto Direct2D in un contesto di dispositivo GDI](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, trasformazioni GDI e compilazioni in linguaggio da destra a sinistra di Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Disegnare contenuto GDI in una destinazione di rendering GDI-Compatible Direct2D](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

In questa panoramica si presuppone che si abbia familiarità con le operazioni di disegno Direct2D di base. Per un'esercitazione, vedere [l'avvio rapido di Direct2D.](direct2d-quickstart.md) Presuppone inoltre che l'utente abbia familiarità con le operazioni di disegno GDI.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Disegnare contenuto Direct2D in un contesto di dispositivo GDI

Per disegnare contenuto Direct2D in un controller di dominio GDI, si usa [**id2D1DCRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) Per creare una destinazione di rendering del controller di dominio, usare il [**metodo ID2D1Factory::CreateDCRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) Questo metodo accetta due parametri.

Il primo parametro, una [**struttura D2D1 \_ RENDER TARGET \_ \_ PROPERTIES,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) specifica le informazioni su rendering, comunicazione remota, DPI, formato pixel e utilizzo. Per consentire alla destinazione di rendering del controller di dominio di funzionare con GDI, impostare il formato [DXGI su DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) e la modalità alfa su [**D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o **D2D1 \_ ALPHA MODE \_ \_ IGNORE.**

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



Nel codice precedente *m \_ pD2DFactory* è un puntatore a [**id2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pDCRT* è un puntatore a [**id2D1DCRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)

Prima di poter eseguire il rendering con la destinazione di rendering del controller di dominio, è necessario usare il relativo [**metodo BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) per associarlo a un controller di dominio GDI. Questa operazione viene apportata ogni volta che si usa un controller di dominio diverso o le dimensioni dell'area che si desidera disegnare per le modifiche.

Il [**metodo BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) accetta due parametri, *hDC* e *pSubRect.* Il *parametro hDC* fornisce un handle al contesto di dispositivo che riceve l'output della destinazione di rendering. Il *parametro pSubRect* è un rettangolo che descrive la parte del contesto di dispositivo in cui viene eseguito il rendering del contenuto. La destinazione di rendering del controller di dominio aggiorna le dimensioni in modo che corrisponda all'area del contesto di dispositivo descritta da *pSubRect*, in caso di modifica delle dimensioni.

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
<col  />
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



Dopo aver associato la destinazione di rendering del controller di dominio a un controller di dominio, è possibile usarla per disegnare. Il codice seguente disegna contenuto Direct2D e GDI usando un controller di dominio.


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



Questo codice produce output come illustrato nella figura seguente (sono stati aggiunti callout per evidenziare la differenza tra il rendering Direct2D e GDI).

![illustrazione di due grafici circolari di cui viene eseguito il rendering con direct2d e gdi](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, trasformazioni GDI e compilazioni in linguaggio da destra a sinistra di Windows

Quando si usa [**un ID2D1DCRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)esegue il rendering del contenuto Direct2D in una bitmap interna e quindi esegue il rendering della bitmap nel controller di dominio con GDI.

È possibile per GDI applicare una trasformazione GDI (tramite il metodo [**SetWorldTransform)**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) o un altro effetto allo stesso controller di dominio usato dalla destinazione di rendering, nel qual caso GDI trasforma la bitmap prodotta da Direct2D. L'uso di una trasformazione GDI per trasformare il contenuto Direct2D può ridurre la qualità visiva dell'output, perché si sta trasformando una bitmap per cui sono già stati calcolati l'antialiasing e il posizionamento dei subpixel.

Si supponga, ad esempio, di usare la destinazione di rendering per disegnare una scena che contiene geometrie e testo con antialias. Se si usa una trasformazione GDI per applicare una trasformazione di scala al controller di dominio e ridimensionare la scena in modo che sia 10 volte più grande, si otterranno pixelizzazione e bordi frastagliati. Se, tuttavia, si applicasse una trasformazione simile usando Direct2D, la qualità visiva della scena non verrebbe compromessa.

In alcuni casi, potrebbe non essere ovvio che GDI sta eseguendo un'elaborazione aggiuntiva che potrebbe ridurre la qualità del contenuto Direct2D. Ad esempio, in una compilazione da destra a sinistra (RTL) di Windows, il contenuto sottoposto a rendering da [**id2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) potrebbe essere invertito orizzontalmente quando GDI lo copia nella destinazione. Il fatto che il contenuto sia effettivamente invertito dipende dalle impostazioni correnti del controller di dominio.

A seconda del tipo di contenuto di cui viene eseguito il rendering, è possibile impedire l'inversione. Se il contenuto Direct2D include testo ClearType, questa inversione degraderà la qualità del testo.

È possibile controllare il comportamento di rendering RTL usando la funzione GDI [**SetLayout.**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) Per evitare il mirroring, chiamare la funzione GDI **SetLayout** e specificare **LAYOUT \_ BITMAPORIENTATIONPRESERVED** come unico valore per il secondo parametro (non combinarlo con **LAYOUT \_ RTL**), come illustrato nell'esempio seguente:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Disegnare contenuto GDI in una destinazione di rendering GDI-Compatible Direct2D

La sezione precedente descrive come scrivere contenuto Direct2D in un controller di dominio GDI. È anche possibile scrivere contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D. Questo approccio è utile per le applicazioni che eseguono principalmente il rendering con Direct2D, ma hanno un modello di estendibilità o altro contenuto legacy che richiede la possibilità di eseguire il rendering con GDI.

Per eseguire il rendering del contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D, usare [**id2D1GdiInteropRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)che fornisce l'accesso a un contesto di dispositivo in grado di accettare chiamate di disegno GDI. A differenza di altre interfacce, un **oggetto ID2D1GdiInteropRenderTarget** non viene creato direttamente. Usare invece il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di un'istanza di destinazione di rendering esistente. Nel codice seguente viene illustrato come eseguire questa operazione:


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



Nel codice precedente *m \_ pD2DFactory* è un puntatore a [**id2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pGDIRT* è un puntatore a [**id2D1GdiInteropRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)

Si noti che il flag [**D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) viene specificato durante la creazione della destinazione di rendering compatibile con GDI Hwnd. Se è necessario un formato pixel, usare [DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM.](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Se è necessaria una modalità alfa, usare [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o **D2D1 \_ ALPHA MODE \_ \_ IGNORE**.

Si noti che [**il metodo QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ha sempre esito positivo. Per verificare se i metodi dell'interfaccia [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funzioneranno per una determinata destinazione di rendering, creare una proprietà DI DESTINAZIONE DI RENDERING [**D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) che specifichi la compatibilità GDI e il formato pixel appropriato, quindi chiamare il metodo [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) della destinazione di rendering per verificare se la destinazione di rendering è compatibile con GDI.

L'esempio seguente illustra come disegnare un grafico a torta (contenuto GDI) nella destinazione di rendering compatibile con GDI Hwnd.


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



Il codice restituisce grafici come illustrato nella figura seguente con callout per evidenziare la differenza di qualità del rendering. Il grafico a torta destro (contenuto GDI) ha una qualità di rendering inferiore rispetto al grafico a torta a sinistra (contenuto Direct2D). Ciò è dovuto al fatto che Direct2D è in grado di eseguire il rendering con l'antialiasing

![illustrazione di due grafici circolari di cui viene eseguito il rendering in una destinazione di rendering compatibile con gdi direct2d](images/gdicontentind2d.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**PROPRIETÀ DELLA DESTINAZIONE DI RENDERING D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[Contesti di dispositivo GDI](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[GDI SDK](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 
