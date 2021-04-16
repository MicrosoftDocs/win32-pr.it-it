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
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="28711-108">Creazione di un'applicazione Direct2D semplice</span><span class="sxs-lookup"><span data-stu-id="28711-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="28711-109">In questo argomento viene illustrato il processo di creazione della classe DemoApp, che crea una finestra e utilizza Direct2D per creare una griglia e due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="28711-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="28711-110">In questa esercitazione si apprenderà come creare risorse Direct2D e creare forme di base.</span><span class="sxs-lookup"><span data-stu-id="28711-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="28711-111">Si apprenderà anche come strutturare l'applicazione per migliorare le prestazioni riducendo al minimo la creazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="28711-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="28711-112">Per seguire l'esercitazione, è possibile usare Microsoft Visual Studio 2008 per creare un progetto Win32 e quindi sostituire il codice nell'intestazione principale dell'applicazione e nel file cpp con il codice descritto in questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="28711-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="28711-113">Se si vuole creare un'app di Windows Store che usa Direct2D, vedere l'argomento [avvio rapido di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="28711-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="28711-114">Per una panoramica delle interfacce che è possibile usare per creare contenuto Direct2D, vedere [Cenni preliminari sull'API Direct2D](the-direct2d-api.md).</span><span class="sxs-lookup"><span data-stu-id="28711-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="28711-115">Questa esercitazione contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="28711-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="28711-116">Parte 1: creare l'intestazione DemoApp</span><span class="sxs-lookup"><span data-stu-id="28711-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="28711-117">Parte 2: implementare l'infrastruttura della classe</span><span class="sxs-lookup"><span data-stu-id="28711-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="28711-118">Parte 3: creare risorse Direct2D</span><span class="sxs-lookup"><span data-stu-id="28711-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="28711-119">Parte 4: rendering del contenuto Direct2D</span><span class="sxs-lookup"><span data-stu-id="28711-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="28711-120">Summary</span><span class="sxs-lookup"><span data-stu-id="28711-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="28711-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28711-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="28711-122">Al termine, la classe DemoApp produce l'output mostrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="28711-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![illustrazione di due rettangoli sullo sfondo di una griglia](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="28711-124">Parte 1: creare l'intestazione DemoApp</span><span class="sxs-lookup"><span data-stu-id="28711-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="28711-125">In questo passaggio si configura l'applicazione per l'uso di Direct2D aggiungendo le intestazioni e le macro necessarie.</span><span class="sxs-lookup"><span data-stu-id="28711-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="28711-126">Si dichiarano inoltre i metodi e i membri dati che verranno usati nelle parti successive di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="28711-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="28711-127">Nel file di intestazione dell'applicazione includere le seguenti intestazioni di uso frequente.</span><span class="sxs-lookup"><span data-stu-id="28711-127">In your application header file, include the following frequently used headers.</span></span>
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

    

2.  <span data-ttu-id="28711-128">Dichiarare funzioni aggiuntive per rilasciare le interfacce e le macro per la gestione degli errori e il recupero dell'indirizzo di base del modulo.</span><span class="sxs-lookup"><span data-stu-id="28711-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
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

    

3.  <span data-ttu-id="28711-129">Dichiarare i metodi per l'inizializzazione della classe, la creazione e l'eliminazione di risorse, la gestione del ciclo di messaggi, il rendering del contenuto e la procedura di Windows.</span><span class="sxs-lookup"><span data-stu-id="28711-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
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



    

4.  <span data-ttu-id="28711-130">Dichiarare i puntatori per un oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , un oggetto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e due oggetti [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) come membri della classe.</span><span class="sxs-lookup"><span data-stu-id="28711-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="28711-131">Parte 2: implementare l'infrastruttura della classe</span><span class="sxs-lookup"><span data-stu-id="28711-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="28711-132">In questa parte si implementano il costruttore e il distruttore DemoApp, i metodi di inizializzazione e di ciclo dei messaggi e la funzione WinMain.</span><span class="sxs-lookup"><span data-stu-id="28711-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="28711-133">La maggior parte di questi metodi ha un aspetto identico a quelli presenti in qualsiasi altra applicazione Win32.</span><span class="sxs-lookup"><span data-stu-id="28711-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="28711-134">L'unica eccezione è il metodo Initialize, che chiama il metodo CreateDeviceIndependentResources (definito nella parte successiva) che crea diverse risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="28711-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="28711-135">Nel file di implementazione della classe implementare il costruttore e il distruttore della classe.</span><span class="sxs-lookup"><span data-stu-id="28711-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="28711-136">Il costruttore deve inizializzare i membri in **null**.</span><span class="sxs-lookup"><span data-stu-id="28711-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="28711-137">Il distruttore deve rilasciare tutte le interfacce archiviate come membri della classe.</span><span class="sxs-lookup"><span data-stu-id="28711-137">The destructor should release any interfaces stored as class members.</span></span>
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



    

2.  <span data-ttu-id="28711-138">Implementare il metodo DemoApp:: RunMessageLoop che converte e invia i messaggi.</span><span class="sxs-lookup"><span data-stu-id="28711-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
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

    

3.  <span data-ttu-id="28711-139">Implementare il metodo Initialize che crea la finestra, la Mostra e chiama il metodo DemoApp:: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="28711-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="28711-140">Implementare il metodo CreateDeviceIndependentResources nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="28711-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
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

    

4.  <span data-ttu-id="28711-141">Creare il metodo WinMain che funge da punto di ingresso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28711-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="28711-142">Inizializzare un'istanza della classe DemoApp e iniziare il relativo ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="28711-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
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

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="28711-143">Parte 3: creare risorse Direct2D</span><span class="sxs-lookup"><span data-stu-id="28711-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="28711-144">In questa parte vengono create le risorse Direct2D utilizzate per il progetto.</span><span class="sxs-lookup"><span data-stu-id="28711-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="28711-145">Direct2D fornisce due tipi di risorse: risorse indipendenti dal dispositivo che possono durare per la durata dell'applicazione e risorse dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28711-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="28711-146">Le risorse dipendenti dal dispositivo sono associate a un particolare dispositivo di rendering e smetteranno di funzionare se il dispositivo è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="28711-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="28711-147">Implementare il metodo DemoApp:: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="28711-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="28711-148">Nel metodo creare un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), una risorsa indipendente dal dispositivo, per la creazione di altre risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="28711-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="28711-149">Usare il membro della classe **m \_ pDirect2DdFactory** per archiviare la factory.</span><span class="sxs-lookup"><span data-stu-id="28711-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="28711-150">Implementare il metodo DemoApp:: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="28711-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="28711-151">Questo metodo crea le risorse dipendenti dal dispositivo della finestra, una destinazione di rendering e due pennelli.</span><span class="sxs-lookup"><span data-stu-id="28711-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="28711-152">Recuperare le dimensioni dell'area client e creare un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) della stessa dimensione che esegue il rendering nell'elemento **HWND** della finestra.</span><span class="sxs-lookup"><span data-stu-id="28711-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="28711-153">Archiviare la destinazione di rendering nel membro della classe **m \_ pRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="28711-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
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

    

3.  <span data-ttu-id="28711-154">Usare la destinazione di rendering per creare una [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) grigia e un **ID2D1SolidColorBrush** blu fiordaliso.</span><span class="sxs-lookup"><span data-stu-id="28711-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
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

    

4.  <span data-ttu-id="28711-155">Poiché questo metodo verrà chiamato ripetutamente, aggiungere un'istruzione if per verificare se la destinazione di rendering (**m \_ pRenderTarget** ) esiste già.</span><span class="sxs-lookup"><span data-stu-id="28711-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="28711-156">Il codice seguente illustra il metodo CreateDeviceResources completo.</span><span class="sxs-lookup"><span data-stu-id="28711-156">The following code shows the complete CreateDeviceResources method.</span></span>
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

    

5.  <span data-ttu-id="28711-157">Implementare il metodo DemoApp::D iscardDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="28711-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="28711-158">In questo metodo rilasciare la destinazione di rendering e i due pennelli creati nel metodo DemoApp:: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="28711-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="28711-159">Parte 4: rendering del contenuto Direct2D</span><span class="sxs-lookup"><span data-stu-id="28711-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="28711-160">In questa parte si implementa la routine di Windows, il metodo OnRender che dipinge il contenuto e il metodo OnResize che regola la dimensione della destinazione di rendering quando la finestra viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="28711-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="28711-161">Implementare il metodo DemoApp:: WndProc per gestire i messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="28711-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="28711-162">Per il messaggio di [**\_ dimensioni WM**](../winmsg/wm-size.md) , chiamare il metodo demoApp:: OnResize e passargli la nuova larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="28711-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="28711-163">Per i messaggi [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , chiamare il metodo demoApp:: OnRender per disegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="28711-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="28711-164">Implementare i metodi OnRender e OnResize nei passaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="28711-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
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

    

2.  <span data-ttu-id="28711-165">Implementare il metodo DemoApp:: OnRender.</span><span class="sxs-lookup"><span data-stu-id="28711-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="28711-166">Per prima cosa, creare un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="28711-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="28711-167">Chiamare quindi il metodo CreateDeviceResource.</span><span class="sxs-lookup"><span data-stu-id="28711-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="28711-168">Questo metodo viene chiamato ogni volta che la finestra viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="28711-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="28711-169">Si ricordi che nel passaggio 4 della parte 3 è stata aggiunta un'istruzione **if** per impedire al metodo di eseguire qualsiasi operazione se la destinazione di rendering esiste già.</span><span class="sxs-lookup"><span data-stu-id="28711-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="28711-170">Verificare che il metodo CreateDeviceResource sia stato completato.</span><span class="sxs-lookup"><span data-stu-id="28711-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="28711-171">In caso contrario, non eseguire alcun disegno.</span><span class="sxs-lookup"><span data-stu-id="28711-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="28711-172">All'interno dell'istruzione **if** appena creata, avviare il disegno chiamando il metodo BeginDraw della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="28711-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="28711-173">Impostare la trasformazione della destinazione di rendering sulla matrice di identità e deselezionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="28711-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="28711-174">Recuperare le dimensioni dell'area di disegno.</span><span class="sxs-lookup"><span data-stu-id="28711-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="28711-175">Disegnare uno sfondo della griglia usando un ciclo **for** e il metodo [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) della destinazione di rendering per disegnare una serie di righe.</span><span class="sxs-lookup"><span data-stu-id="28711-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
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

    

7.  <span data-ttu-id="28711-176">Creare due primitive rettangolari centrate sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="28711-176">Create two rectangle primitives that are centered on the screen.</span></span>
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

    

8.  <span data-ttu-id="28711-177">Usare il metodo [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) della destinazione di rendering per disegnare l'interno del primo rettangolo con il pennello grigio.</span><span class="sxs-lookup"><span data-stu-id="28711-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="28711-178">Usare il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) della destinazione di rendering per disegnare la struttura del secondo rettangolo con il pennello blu fiordaliso.</span><span class="sxs-lookup"><span data-stu-id="28711-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="28711-179">Chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="28711-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="28711-180">Il metodo **EndDraw** restituisce un valore **HRESULT** per indicare se le operazioni di disegno sono state completate correttamente.</span><span class="sxs-lookup"><span data-stu-id="28711-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="28711-181">Chiudere l'istruzione **if** iniziata nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="28711-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="28711-182">Controllare **HRESULT** restituito da [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="28711-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="28711-183">Se indica che è necessario ricreare la destinazione di rendering, chiamare il metodo DemoApp::D iscardDeviceResources per rilasciarlo; verrà ricreato la volta successiva che la finestra riceverà un messaggio [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) o [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="28711-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="28711-184">Restituire **HRESULT** e chiudere il metodo.</span><span class="sxs-lookup"><span data-stu-id="28711-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="28711-185">Implementare il metodo DemoApp:: OnResize in modo da ridimensionare la destinazione di rendering alla nuova dimensione della finestra.</span><span class="sxs-lookup"><span data-stu-id="28711-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
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

    

<span data-ttu-id="28711-186">L'esercitazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="28711-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="28711-187">Per usare Direct2D, verificare che l'applicazione includa il file di intestazione d2d1. h e venga compilato con la libreria d2d1. lib.</span><span class="sxs-lookup"><span data-stu-id="28711-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="28711-188">È possibile trovare d2d1. h e d2d1. lib in [Windows Software Development Kit (SDK) per Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="28711-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="28711-189">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="28711-189">Summary</span></span>

<span data-ttu-id="28711-190">In questa esercitazione si è appreso come creare risorse Direct2D e creare forme di base.</span><span class="sxs-lookup"><span data-stu-id="28711-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="28711-191">Si è inoltre appreso come strutturare l'applicazione per migliorare le prestazioni riducendo al minimo la creazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="28711-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28711-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28711-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28711-193">Panoramica dell'API Direct2D</span><span class="sxs-lookup"><span data-stu-id="28711-193">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> <dt>

[<span data-ttu-id="28711-194">Miglioramento delle prestazioni di Direct2D</span><span class="sxs-lookup"><span data-stu-id="28711-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 