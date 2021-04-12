---
title: Primo programma Direct2D
description: Viene ora creato il primo programma Direct2D. Il programma non esegue alcuna operazione, \ 8212; disegna semplicemente un cerchio che riempie l'area client della finestra. Questo programma introduce tuttavia molti concetti di Direct2D essenziali.
ms.assetid: 940cc5e4-2952-4714-bf32-c611a965f819
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445f98c5dc6a6e5d1aa91d913010cb406a67992
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398913"
---
# <a name="your-first-direct2d-program"></a><span data-ttu-id="9e3c9-105">Primo programma Direct2D</span><span class="sxs-lookup"><span data-stu-id="9e3c9-105">Your First Direct2D Program</span></span>

<span data-ttu-id="9e3c9-106">Viene ora creato il primo programma Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-106">Let's create our first Direct2D program.</span></span> <span data-ttu-id="9e3c9-107">Il programma non esegue alcuna operazione, bensì disegna semplicemente un cerchio che riempie l'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-107">The program does not do anything fancy — it just draws a circle that fills the client area of the window.</span></span> <span data-ttu-id="9e3c9-108">Questo programma introduce tuttavia molti concetti di Direct2D essenziali.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-108">But this program introduces many essential Direct2D concepts.</span></span>

![screenshot del programma Circle.](images/graphics08.png)

<span data-ttu-id="9e3c9-110">Ecco il listato di codice per il programma Circle.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-110">Here is the code listing for the Circle program.</span></span> <span data-ttu-id="9e3c9-111">Il programma usa nuovamente la `BaseWindow` classe definita nell'argomento [gestione dello stato dell'applicazione](managing-application-state-.md).</span><span class="sxs-lookup"><span data-stu-id="9e3c9-111">The program re-uses the `BaseWindow` class that was defined in the topic [Managing Application State](managing-application-state-.md).</span></span> <span data-ttu-id="9e3c9-112">Negli argomenti successivi il codice viene esaminato in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-112">Later topics will examine the code in detail.</span></span>


```C++
#include <windows.h>
#include <d2d1.h>
#pragma comment(lib, "d2d1")

#include "basewin.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

class MainWindow : public BaseWindow<MainWindow>
{
    ID2D1Factory            *pFactory;
    ID2D1HwndRenderTarget   *pRenderTarget;
    ID2D1SolidColorBrush    *pBrush;
    D2D1_ELLIPSE            ellipse;

    void    CalculateLayout();
    HRESULT CreateGraphicsResources();
    void    DiscardGraphicsResources();
    void    OnPaint();
    void    Resize();

public:

    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL)
    {
    }

    PCWSTR  ClassName() const { return L"Circle Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};

// Recalculate drawing layout when the size of the window changes.

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

HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}

void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}

void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}

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

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Circle", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;

    case WM_DESTROY:
        DiscardGraphicsResources();
        SafeRelease(&pFactory);
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        OnPaint();
        return 0;



    case WM_SIZE:
        Resize();
        return 0;
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```





<span data-ttu-id="9e3c9-113">È possibile scaricare il progetto di Visual Studio completo dall' [esempio del cerchio Direct2D](direct2d-circle-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9e3c9-113">You can download the complete Visual Studio project from [Direct2D Circle Sample](direct2d-circle-sample.md).</span></span>

## <a name="the-d2d1-namespace"></a><span data-ttu-id="9e3c9-114">Spazio dei nomi D2D1</span><span class="sxs-lookup"><span data-stu-id="9e3c9-114">The D2D1 Namespace</span></span>

<span data-ttu-id="9e3c9-115">Lo spazio dei nomi **d2d1** contiene le funzioni e le classi helper.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-115">The **D2D1** namespace contains helper functions and classes.</span></span> <span data-ttu-id="9e3c9-116">Che non fanno parte dell'API Direct2D: è possibile programmare Direct2D senza utilizzarle, ma consentono di semplificare il codice.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-116">These are not strictly part of the Direct2D API — you can program Direct2D without using them — but they help simplify your code.</span></span> <span data-ttu-id="9e3c9-117">Lo spazio dei nomi **d2d1** contiene:</span><span class="sxs-lookup"><span data-stu-id="9e3c9-117">The **D2D1** namespace contains:</span></span>

-   <span data-ttu-id="9e3c9-118">Classe [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) per la costruzione di valori di colore.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-118">A [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class for constructing color values.</span></span>
-   <span data-ttu-id="9e3c9-119">[**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) per la costruzione di matrici di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-119">A [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) for constructing transformation matrices.</span></span>
-   <span data-ttu-id="9e3c9-120">Set di funzioni per inizializzare le strutture Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9e3c9-120">A set of functions to initialize Direct2D structures.</span></span>

<span data-ttu-id="9e3c9-121">In questo modulo vengono visualizzati esempi dello spazio dei nomi **d2d1** .</span><span class="sxs-lookup"><span data-stu-id="9e3c9-121">You will see examples of the **D2D1** namespace throughout this module.</span></span>

## <a name="next"></a><span data-ttu-id="9e3c9-122">Prossima</span><span class="sxs-lookup"><span data-stu-id="9e3c9-122">Next</span></span>

[<span data-ttu-id="9e3c9-123">Destinazioni di rendering, dispositivi e risorse</span><span class="sxs-lookup"><span data-stu-id="9e3c9-123">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)

## <a name="related-topics"></a><span data-ttu-id="9e3c9-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e3c9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e3c9-125">Esempio di cerchio Direct2D</span><span class="sxs-lookup"><span data-stu-id="9e3c9-125">Direct2D Circle Sample</span></span>](direct2d-circle-sample.md)
</dt> </dl>

 

 