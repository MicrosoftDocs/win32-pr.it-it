---
title: Panoramica delle destinazioni di rendering
description: Vengono descritti i diversi tipi di destinazioni di rendering Direct2D e il modo in cui utilizzarli.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinazioni di rendering
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963210"
---
# <a name="render-targets-overview"></a>Panoramica delle destinazioni di rendering

Una destinazione di rendering è una risorsa che eredita dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Una destinazione di rendering crea risorse per il disegno e l'esecuzione di operazioni di disegno effettive. Questo argomento descrive i diversi tipi di destinazioni di rendering Direct2D e come usarli.

-   [Destinazioni di rendering](#render-targets-overview)
    -   [Funzionalità di destinazione di rendering](#render-target-features)
    -   [Risorse di destinazione di rendering](#render-target-resources)
    -   [Disegno di comandi](#drawing-commands)
    -   [Gestione degli errori](#error-handling)
-   [Esempio: rendering del contenuto in una finestra](#example-render-content-to-a-window)

## <a name="render-targets"></a>Destinazioni di rendering

Una destinazione di rendering è una risorsa che eredita dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Una destinazione di rendering crea risorse per il disegno e l'esecuzione di operazioni di disegno effettive. Esistono diversi tipi di destinazioni di rendering che è possibile utilizzare per eseguire il rendering della grafica nei modi seguenti:

-   Gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) eseguono il rendering del contenuto in una finestra.
-   Gli oggetti [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) eseguono il rendering in un contesto di dispositivo GDI.
-   Gli oggetti di destinazione di rendering bitmap eseguono il rendering del contenuto in una bitmap fuori schermo.
-   DXGI rendering degli oggetti di destinazione rendering in una superficie DXGI per l'uso con Direct3D.

Poiché una destinazione di rendering è associata a un particolare dispositivo di rendering, si tratta di una risorsa dipendente dal dispositivo e smette di funzionare se il dispositivo viene rimosso.

### <a name="render-target-features"></a>Funzionalità di destinazione di rendering

È possibile specificare se una destinazione di rendering utilizza l'accelerazione hardware e se viene eseguito il rendering di una visualizzazione remota da un computer locale o remoto. Le destinazioni di rendering possono essere impostate per il rendering con alias o con alias. Per il rendering di scene con un numero elevato di primitive, uno sviluppatore può anche eseguire il rendering di grafica 2D in modalità con alias e utilizzare l'anti-aliasing di D3D multisample per ottenere una maggiore scalabilità.

Le destinazioni di rendering possono inoltre raggruppare le operazioni di disegno in livelli rappresentati dall'interfaccia [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . I livelli sono utili per raccogliere le operazioni di disegno da comporre insieme durante il rendering di un frame. Per alcuni scenari, può trattarsi di un'alternativa utile per eseguire il rendering in una destinazione di rendering bitmap e quindi riutilizzare il contenuto della bitmap, perché i costi di allocazione per i livelli sono inferiori rispetto a quelli di un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Le destinazioni di rendering possono creare nuove destinazioni di rendering compatibili con se stesse, che risulta utile per il rendering intermedio all'esterno dello schermo, mantenendo al tempo stesso le varie proprietà di destinazione di rendering impostate nell'oggetto originale.

È anche possibile eseguire il rendering usando GDI in una destinazione di rendering Direct2D chiamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in una destinazione di rendering per [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), che contiene metodi [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) che possono essere usati per recuperare un contesto di dispositivo GDI. Il rendering tramite GDI è possibile solo se la destinazione di rendering è stata creata con il flag di [**utilizzo della destinazione di rendering d2d1 impostato su \_ \_ \_ \_ GDI \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Questa operazione è utile per le applicazioni che eseguono principalmente il rendering con Direct2D ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI. Per ulteriori informazioni, vedere [Cenni preliminari sull'interoperatività Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Risorse di destinazione di rendering

Analogamente a una factory, una destinazione di rendering può creare risorse di disegno. Tutte le risorse create da una destinazione di rendering sono risorse dipendenti dal dispositivo, proprio come la destinazione di rendering. Una destinazione di rendering può creare i tipi di risorse seguenti:

-   Bitmap
-   Pennelli
-   Livelli
-   Mesh

### <a name="drawing-commands"></a>Disegno di comandi

Per eseguire il rendering del contenuto, usare i metodi di disegno della destinazione di rendering. Prima di iniziare a disegnare, chiamare il metodo [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Al termine del disegno, chiamare il metodo [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Tra queste chiamate, si usano i metodi Draw e Fill per eseguire il rendering delle risorse di disegno. La maggior parte dei metodi di disegno e riempimento accetta una forma, ovvero una primitiva o una geometria, e un pennello per riempire o delineare la forma.

Le destinazioni di rendering forniscono metodi per il ritaglio, l'applicazione di maschere di opacità e la trasformazione dello spazio delle coordinate.

Direct2D usa un sistema di coordinate a sinistra: i valori positivi dell'asse x procedono verso destra e i valori positivi dell'asse y procedono verso il basso.

### <a name="error-handling"></a>Gestione degli errori

I comandi di disegno della destinazione di rendering non indicano se l'operazione richiesta è stata eseguita correttamente. Per determinare se sono presenti errori di disegno, chiamare il metodo [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) della destinazione di rendering o il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) per ottenere un valore **HRESULT**.

## <a name="example-render-content-to-a-window"></a>Esempio: rendering del contenuto in una finestra

Nell'esempio seguente viene usato il metodo [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) per creare un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



Nell'esempio seguente viene usato [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) per creare testo nella finestra.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



Il codice è stato omesso da questo esempio.

 

 