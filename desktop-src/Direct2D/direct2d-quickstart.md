---
title: Creazione di un'applicazione Direct2D semplice
description: Viene illustrato il processo di creazione di una finestra che esegue il rendering del contenuto Direct2D.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, esercitazione
- Direct2D, procedura dettagliata
- Direct2D, creazione di applicazioni
- Direct2D, applicazioni
- applicazioni per Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559920"
---
# <a name="creating-a-simple-direct2d-application"></a>Creazione di un'applicazione Direct2D semplice

In questo argomento viene illustrato il processo di creazione della classe DemoApp, che crea una finestra e utilizza Direct2D per creare una griglia e due rettangoli. In questa esercitazione si apprenderà come creare risorse Direct2D e creare forme di base. Si apprenderà anche come strutturare l'applicazione per migliorare le prestazioni riducendo al minimo la creazione di risorse.

Per seguire l'esercitazione, è possibile usare Microsoft Visual Studio 2008 per creare un progetto Win32 e quindi sostituire il codice nell'intestazione principale dell'applicazione e nel file cpp con il codice descritto in questa esercitazione.

> [!Note]  
> Se si vuole creare un'app di Windows Store che usa Direct2D, vedere l'argomento [avvio rapido di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md) .

 

Per una panoramica delle interfacce che è possibile usare per creare contenuto Direct2D, vedere [Cenni preliminari sull'API Direct2D](the-direct2d-api.md).

Questa esercitazione contiene le parti seguenti:

-   [Parte 1: creare l'intestazione DemoApp](#part-1-create-the-demoapp-header)
-   [Parte 2: implementare l'infrastruttura della classe](#part-2-implement-the-class-infrastructure)
-   [Parte 3: creare risorse Direct2D](#part-3-create-direct2d-resources)
-   [Parte 4: rendering del contenuto Direct2D](#part-4-render-direct2d-content)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

Al termine, la classe DemoApp produce l'output mostrato nella figura seguente.

![illustrazione di due rettangoli sullo sfondo di una griglia](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>Parte 1: creare l'intestazione DemoApp

In questo passaggio si configura l'applicazione per l'uso di Direct2D aggiungendo le intestazioni e le macro necessarie. Si dichiarano inoltre i metodi e i membri dati che verranno usati nelle parti successive di questa esercitazione.

1.  Nel file di intestazione dell'applicazione includere le seguenti intestazioni di uso frequente.
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  Dichiarare funzioni aggiuntive per rilasciare le interfacce e le macro per la gestione degli errori e il recupero dell'indirizzo di base del modulo.
```C++
    template<class Interface>
    inline void SafeRelease(
        Interface **ppInterfaceToRelease
        )
    {
        if (*ppInterfaceToRelease != NULL)
        {
            (*ppInterfaceToRelease)->Release();

            (*ppInterfaceToRelease) = NULL;
        }
    }


    #ifndef Assert
    #if defined( DEBUG ) || defined( _DEBUG )
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  Dichiarare i metodi per l'inizializzazione della classe, la creazione e l'eliminazione di risorse, la gestione del ciclo di messaggi, il rendering del contenuto e la procedura di Windows.
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  Dichiarare i puntatori per un oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , un oggetto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e due oggetti [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) come membri della classe.
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>Parte 2: implementare l'infrastruttura della classe

In questa parte si implementano il costruttore e il distruttore DemoApp, i metodi di inizializzazione e di ciclo dei messaggi e la funzione WinMain. La maggior parte di questi metodi ha un aspetto identico a quelli presenti in qualsiasi altra applicazione Win32. L'unica eccezione è il metodo Initialize, che chiama il metodo CreateDeviceIndependentResources (definito nella parte successiva) che crea diverse risorse Direct2D.

1.  Nel file di implementazione della classe implementare il costruttore e il distruttore della classe. Il costruttore deve inizializzare i membri in **null**. Il distruttore deve rilasciare tutte le interfacce archiviate come membri della classe.
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  Implementare il metodo DemoApp:: RunMessageLoop che converte e invia i messaggi.
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  Implementare il metodo Initialize che crea la finestra, la Mostra e chiama il metodo DemoApp:: CreateDeviceIndependentResources. Implementare il metodo CreateDeviceIndependentResources nella sezione successiva.
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
                WS_OVERLAPPEDWINDOW,
                CW_USEDEFAULT,
                CW_USEDEFAULT,
                static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
                static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
                NULL,
                NULL,
                HINST_THISCOMPONENT,
                this
                );
            hr = m_hwnd ? S_OK : E_FAIL;
            if (SUCCEEDED(hr))
            {
                ShowWindow(m_hwnd, SW_SHOWNORMAL);
                UpdateWindow(m_hwnd);
            }
        }

        return hr;
    }
```

    

4.  Creare il metodo WinMain che funge da punto di ingresso dell'applicazione. Inizializzare un'istanza della classe DemoApp e iniziare il relativo ciclo di messaggi.
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
        // unlikely event that HeapSetInformation fails.
        HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

        if (SUCCEEDED(CoInitialize(NULL)))
        {
            {
                DemoApp app;

                if (SUCCEEDED(app.Initialize()))
                {
                    app.RunMessageLoop();
                }
            }
            CoUninitialize();
        }

        return 0;
    }
```

    

## <a name="part-3-create-direct2d-resources"></a>Parte 3: creare risorse Direct2D

In questa parte vengono create le risorse Direct2D utilizzate per il progetto. Direct2D fornisce due tipi di risorse: risorse indipendenti dal dispositivo che possono durare per la durata dell'applicazione e risorse dipendenti dal dispositivo. Le risorse dipendenti dal dispositivo sono associate a un particolare dispositivo di rendering e smetteranno di funzionare se il dispositivo è stato rimosso.

1.  Implementare il metodo DemoApp:: CreateDeviceIndependentResources. Nel metodo creare un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), una risorsa indipendente dal dispositivo, per la creazione di altre risorse Direct2D. Usare il membro della classe **m \_ pDirect2DdFactory** per archiviare la factory.
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  Implementare il metodo DemoApp:: CreateDeviceResources. Questo metodo crea le risorse dipendenti dal dispositivo della finestra, una destinazione di rendering e due pennelli. Recuperare le dimensioni dell'area client e creare un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) della stessa dimensione che esegue il rendering nell'elemento **HWND** della finestra. Archiviare la destinazione di rendering nel membro della classe **m \_ pRenderTarget** .
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  Usare la destinazione di rendering per creare una [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) grigia e un **ID2D1SolidColorBrush** blu fiordaliso.
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  Poiché questo metodo verrà chiamato ripetutamente, aggiungere un'istruzione if per verificare se la destinazione di rendering (**m \_ pRenderTarget** ) esiste già. Il codice seguente illustra il metodo CreateDeviceResources completo.
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  Implementare il metodo DemoApp::D iscardDeviceResources. In questo metodo rilasciare la destinazione di rendering e i due pennelli creati nel metodo DemoApp:: CreateDeviceResources.
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>Parte 4: rendering del contenuto Direct2D

In questa parte si implementa la routine di Windows, il metodo OnRender che dipinge il contenuto e il metodo OnResize che regola la dimensione della destinazione di rendering quando la finestra viene ridimensionata.

1.  Implementare il metodo DemoApp:: WndProc per gestire i messaggi della finestra. Per il messaggio di [**\_ dimensioni WM**](../winmsg/wm-size.md) , chiamare il metodo demoApp:: OnResize e passargli la nuova larghezza e altezza. Per i messaggi [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , chiamare il metodo demoApp:: OnRender per disegnare la finestra. Implementare i metodi OnRender e OnResize nei passaggi successivi.
```C++
    LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
    {
        LRESULT result = 0;

        if (message == WM_CREATE)
        {
            LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
            DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

            ::SetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA,
                reinterpret_cast<LONG_PTR>(pDemoApp)
                );

            result = 1;
        }
        else
        {
            DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
                ::GetWindowLongPtrW(
                    hwnd,
                    GWLP_USERDATA
                    )));

            bool wasHandled = false;

            if (pDemoApp)
            {
                switch (message)
                {
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
                    break;
                }
            }

            if (!wasHandled)
            {
                result = DefWindowProc(hwnd, message, wParam, lParam);
            }
        }

        return result;
    }
    
```

    

2.  Implementare il metodo DemoApp:: OnRender. Per prima cosa, creare un **HRESULT**. Chiamare quindi il metodo CreateDeviceResource. Questo metodo viene chiamato ogni volta che la finestra viene disegnata. Si ricordi che nel passaggio 4 della parte 3 è stata aggiunta un'istruzione **if** per impedire al metodo di eseguire qualsiasi operazione se la destinazione di rendering esiste già.
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  Verificare che il metodo CreateDeviceResource sia stato completato. In caso contrario, non eseguire alcun disegno.
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  All'interno dell'istruzione **if** appena creata, avviare il disegno chiamando il metodo BeginDraw della destinazione di rendering. Impostare la trasformazione della destinazione di rendering sulla matrice di identità e deselezionare la finestra.
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  Recuperare le dimensioni dell'area di disegno.
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  Disegnare uno sfondo della griglia usando un ciclo **for** e il metodo [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) della destinazione di rendering per disegnare una serie di righe.
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  Creare due primitive rettangolari centrate sullo schermo.
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  Usare il metodo [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) della destinazione di rendering per disegnare l'interno del primo rettangolo con il pennello grigio.
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  Usare il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) della destinazione di rendering per disegnare la struttura del secondo rettangolo con il pennello blu fiordaliso.
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. Chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) della destinazione di rendering. Il metodo **EndDraw** restituisce un valore **HRESULT** per indicare se le operazioni di disegno sono state completate correttamente. Chiudere l'istruzione **if** iniziata nel passaggio 3.
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. Controllare **HRESULT** restituito da [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Se indica che è necessario ricreare la destinazione di rendering, chiamare il metodo DemoApp::D iscardDeviceResources per rilasciarlo; verrà ricreato la volta successiva che la finestra riceverà un messaggio [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) o [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. Restituire **HRESULT** e chiudere il metodo.
```C++
        return hr;
    }
```

    

13. Implementare il metodo DemoApp:: OnResize in modo da ridimensionare la destinazione di rendering alla nuova dimensione della finestra.
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

L'esercitazione è stata completata.

> [!Note]  
> Per usare Direct2D, verificare che l'applicazione includa il file di intestazione d2d1. h e venga compilato con la libreria d2d1. lib. È possibile trovare d2d1. h e d2d1. lib in [Windows Software Development Kit (SDK) per Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

 

## <a name="summary"></a>Riepilogo

In questa esercitazione si è appreso come creare risorse Direct2D e creare forme di base. Si è inoltre appreso come strutturare l'applicazione per migliorare le prestazioni riducendo al minimo la creazione di risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'API Direct2D](the-direct2d-api.md)
</dt> <dt>

[Miglioramento delle prestazioni di Direct2D](improving-direct2d-performance.md)
</dt> </dl>

 

 