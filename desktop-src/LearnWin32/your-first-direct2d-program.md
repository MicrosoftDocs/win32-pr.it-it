---
title: Il primo programma Direct2D
description: Si creerà ora il primo programma Direct2D. Il programma non esegue alcun'operazione di fantasia \ 8212; disegna semplicemente un cerchio che riempie l'area client della finestra. Questo programma introduce tuttavia molti concetti essenziali di Direct2D.
ms.assetid: 940cc5e4-2952-4714-bf32-c611a965f819
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb7b9b4a81b9e3767f9d53d0c5872b170772c1cb60b4a74c599401de342ee05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754391"
---
# <a name="your-first-direct2d-program"></a>Il primo programma Direct2D

Si creerà ora il primo programma Direct2D. Il programma non esegue nulla di sofisticato, ma disegna semplicemente un cerchio che riempie l'area client della finestra. Questo programma introduce tuttavia molti concetti essenziali di Direct2D.

![screenshot del programma circle.](images/graphics08.png)

Ecco l'elenco di codice per il programma Circle. Il programma usa nuovamente la `BaseWindow` classe definita nell'argomento Gestione dello stato [dell'applicazione](managing-application-state-.md). Negli argomenti successivi il codice verrà esaminato in dettaglio.


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





È possibile scaricare il progetto completo Visual Studio da [Direct2D Circle Sample](direct2d-circle-sample.md).

## <a name="the-d2d1-namespace"></a>Spazio dei nomi D2D1

Lo **spazio dei nomi D2D1** contiene funzioni e classi helper. Non fanno esclusivamente parte dell'API Direct2D, è possibile programmare Direct2D senza usarle, ma consentono di semplificare il codice. Lo **spazio dei nomi D2D1** contiene:

-   Classe [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) per la costruzione di valori di colore.
-   [**Matrice3x2F per**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) la costruzione di matrici di trasformazione.
-   Set di funzioni per inizializzare le strutture Direct2D.

In questo modulo verranno visualizzati esempi dello spazio dei **nomi D2D1.**

## <a name="next"></a>Prossima

[Destinazioni di rendering, dispositivi e risorse](render-targets--devices--and-resources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di cerchio Direct2D](direct2d-circle-sample.md)
</dt> </dl>

 

 