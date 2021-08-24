---
title: Come animare la bitmap di una finestra figlio su più livelli
description: Questo argomento descrive come creare e animare un oggetto visivo che usa la bitmap di una finestra figlio su più livelli come contenuto dell'oggetto visivo.
ms.assetid: 8912CCF9-C343-45CB-AB31-55D26C118AF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b882d1be2642f341e74a193605b217a9b7e2d0cc295370c7a5ec8bee4a844f03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670971"
---
# <a name="how-to-animate-the-bitmap-of-a-layered-child-window"></a>Come animare la bitmap di una finestra figlio su più livelli

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedi [Modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento descrive come creare e animare un oggetto visivo che usa la bitmap di una finestra figlio su più livelli come contenuto dell'oggetto visivo. L'esempio descritto in questo argomento usa una trasformazione della scala animata per "aumentare" la bitmap di una finestra figlio dalle dimensioni del cursore alle dimensioni complete. Per altre informazioni sulle finestre su più livelli, vedere [Bitmap delle finestre.](bitmap-surfaces.md)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [DirectComposition](directcomposition-portal.md)
-   [Grafica Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX Graphic Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Microsoft Win32
-   Component Object Model (COM)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-a-layered-child-window"></a>Passaggio 1: Creare una finestra figlio su più livelli

Usare la procedura seguente per creare una finestra figlio su più livelli.

1.  Registrare la classe della finestra figlio e creare una finestra figlio con lo [**stile WS \_ EX \_ LAYERED.**](/windows/desktop/winmsg/extended-window-styles) Nell'esempio seguente specificare la risoluzione dello schermo in pixel per pollice logico e è l'handle della finestra principale `m_dpiX` `m_dpiY` `m_hwndMain` dell'applicazione.
```C++
    HWND m_hwndLayeredChild;

    
HRESULT hr = S_OK;

    WNDCLASSEXW wcex;
    wcex.cbSize         = sizeof(wcex);
    wcex.style          = 0;
    wcex.lpfnWndProc    = DemoApp::ChildWndProc;
    wcex.cbClsExtra     = 0;
    wcex.cbWndExtra     = 0;
    wcex.hInstance      = HINST_THISCOMPONENT;
    wcex.hIcon          = NULL;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH) GetStockObject (GRAY_BRUSH);
    wcex.lpszMenuName   = NULL;
    wcex.lpszClassName  = L&quot;DCompLayeredChildWindow&quot;;
    wcex.hIconSm        = NULL;

    if (!RegisterClassExW(&wcex))
    {
        return FALSE;
    }

    m_hwndLayeredChild = CreateWindowEx(WS_EX_LAYERED,
        L&quot;DCompLayeredChildWindow&quot;,                
        NULL,                                    
        WS_CHILD | WS_CLIPSIBLINGS,             
        0, 
        0, 
        static_cast<UINT>(ceil(640.0f * m_dpiX / 96.0f)),
        static_cast<UINT>(ceil(480.0f * m_dpiY / 96.0f)),                                  
        m_hwndMain,                               
        NULL,                                     
        HINST_THISCOMPONENT,                    
        this);                                   
```



    

2.  Chiamare la [**funzione SetLayeredWindowAttributes**](/windows/desktop/api/winuser/nf-winuser-setlayeredwindowattributes) per impostare la chiave di colore di trasparenza e l'opacità della finestra figlio su più livelli. Il codice seguente imposta la chiave di colore della trasparenza su zero e l'opacità su 255 (opaca).

```C++
    if (!SetLayeredWindowAttributes(m_hwndLayeredChild, 0, 255, LWA_ALPHA))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
```

    

3.  Eseguire il rendering di contenuto nella finestra figlio.

### <a name="step-2-initialize-directcomposition-objects"></a>Passaggio 2: Inizializzare gli oggetti DirectComposition

Creare l'oggetto dispositivo e l'oggetto di destinazione della composizione. Per altre informazioni, vedere [Come inizializzare DirectComposition.](initialize-directcomposition.md)

### <a name="step-3-create-a-visual-object-and-set-the-layered-child-windows-bitmap-as-the-content-property"></a>Passaggio 3: Creare un oggetto visivo e impostare la bitmap della finestra figlio su più livelli come proprietà del contenuto

Usare la procedura seguente per creare un oggetto visivo, impostarne la proprietà del contenuto in modo da usare la bitmap della finestra figlio su più livelli e quindi aggiungere l'oggetto visivo alla struttura ad albero visuale.

1.  Chiamare [**IDCompositionDevice::CreateVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) per creare un oggetto visivo.
2.  Creare una superficie Microsoft DirectComposition per la finestra figlio su più livelli passando l'handle della finestra figlio alla [**funzione CreateSurfaceFromHwnd.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhwnd)
3.  Chiamare il metodo [**IDCompositionVisual::SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) dell'oggetto visivo per impostare la nuova superficie come contenuto visivo della finestra figlio su più livelli.
4.  Aggiungere l'oggetto visivo alla struttura ad albero visuale. Per aggiungere l'oggetto visivo alla radice dell'albero, chiamare il [**metodo IDCompositionTarget::SetRoot.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) Per aggiungere l'oggetto visivo come figlio di un altro oggetto visivo, usare il [**metodo IDCompositionVisual::AddVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-addvisual) dell'oggetto visivo padre.

L'esempio seguente crea un oggetto visivo, ne imposta la proprietà Content per usare la bitmap della finestra figlio su più livelli e aggiunge l'oggetto visivo alla radice della struttura ad albero visuale.


```C++
IDCompositionVisual *pVisual = nullptr;
IUnknown* pSurface    = nullptr;

hr = m_pDevice->CreateVisual(&pVisual);
if (SUCCEEDED(hr))
{
    hr = m_pDevice->CreateSurfaceFromHwnd(m_hwndLayeredChild, &pSurface);
}

if (SUCCEEDED(hr))
{
    hr = pVisual->SetContent(pSurface);
}

if (SUCCEEDED(hr))
{
    hr = m_pCompTarget->SetRoot(pVisual);
}
```



### <a name="step-4-create-an-animation-object-and-a-scale-transform-object"></a>Passaggio 4: Creare un oggetto animazione e un oggetto di trasformazione della scala

Usare il [**metodo IDCompositionDevice::CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) per creare un oggetto animazione e il metodo [**IDCompositionDevice::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform) per creare un oggetto di trasformazione della scala.


```C++
IDCompositionAnimation *pAnimateScale = NULL;
IDCompositionScaleTransform *pScale = NULL;

if (SUCCEEDED(hr))
{
    hr = m_pDevice->CreateAnimation(&pAnimateScale);
}

if (SUCCEEDED(hr))
{
    // Create the scale transform object.
    hr = m_pDevice->CreateScaleTransform(&pScale);
}
```



### <a name="step-5-build-the-animation-function"></a>Passaggio 5: Creare la funzione di animazione

Usare i metodi dell'interfaccia [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) dell'oggetto animazione per creare una funzione di animazione.

Nell'esempio seguente viene compilata una semplice funzione di animazione costituita da un segmento polinomiale cubico e un segmento finale.


```C++
pAnimateScale->AddCubic(
    0.0f,  // offset from beginning of animation function, in seconds
    0.0f,  // constant coefficient  
    1.0f,  // linear coefficient
    0.0f,  // quadratic coefficient
    0.0f); // cubic coefficient
pAnimateScale->End(1.0f, 1.0f);
```



### <a name="step-6-apply-the-animation-object-to-properties-of-the-scale-transform-object"></a>Passaggio 6: Applicare l'oggetto animazione alle proprietà dell'oggetto di trasformazione della scala

Usare i [**metodi IDCompositionScale::SetScaleX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(idcompositionanimation)) e [**SetScaleY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscaley(idcompositionanimation)) per applicare l'oggetto animazione alle proprietà ScaleX e ScaleY dell'oggetto di trasformazione della scala.


```C++
// Find the center of the child window.
RECT rcChild = { };
GetClientRect(m_hwndLayeredChild, &rcChild);
float centerX = rcChild.right / 2.0f;
float centerY = rcChild.bottom / 2.0f;

// Scale from the center point of the child window's bitmap.
pScale->SetCenterX(centerX);
pScale->SetCenterY(centerY);

// Use the same animation object to animate the X and Y scale
// factors.
pScale->SetScaleX(pAnimateScale);
pScale->SetScaleY(pAnimateScale);
```



### <a name="step-7-apply-the-scale-transform-object-to-the-transform-property-of-the-visual"></a>Passaggio 7: Applicare l'oggetto trasformazione della scala alla proprietà transform dell'oggetto visivo

Usa il [**metodo IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) per applicare l'oggetto trasformazione della scala alla proprietà Transform dell'oggetto visivo.


```C++
hr = pVisual->SetTransform(pScale);
```



### <a name="step-8-cloak-the-layered-child-window"></a>Passaggio 8: Mascherare la finestra figlio su più livelli

Prima di eseguire il commit dell'animazione, usare la funzione [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) con il flag [**\_ CLOAK DWMWA**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) per "mascherare" la finestra figlio su più livelli. La clonazione rimuove la finestra figlio su più livelli dalla visualizzazione mentre viene eseguito il rendering sullo schermo della versione animata della visualizzazione bitmap della finestra.


```C++
BOOL fCloak = TRUE;
DwmSetWindowAttribute(pDemoApp->m_hwndLayeredChild,
    DWMWA_CLOAK,
    &fCloak,
    sizeof(fCloak));
```



### <a name="step-9-commit-the-composition"></a>Passaggio 9: Eseguire il commit della composizione

Usare il [**metodo IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit del batch di comandi in Microsoft DirectComposition per l'elaborazione. L'animazione verrà visualizzata nella finestra di destinazione.

### <a name="step-10-uncloak-the-layered-child-window"></a>Passaggio 10: Rimuovere la finestra figlio su più livelli

Al termine dell'animazione, usare la funzione [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) con il flag **\_ CLOAK DWMWA** per rimuovere la finestra figlio su più livelli.

### <a name="step-11-release-directcomposition-objects"></a>Passaggio 11: Rilasciare oggetti DirectComposition

Assicurarsi di rilasciare tutti gli oggetti DirectComposition quando non sono più necessari. Nell'esempio seguente viene chiamata la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti DirectComposition.


```C++
SafeRelease(&pVisual);
SafeRelease(&pAnimateScale);
SafeRelease(&pScale);


SafeRelease(&m_pDevice);
SafeRelease(&m_pCompTarget);
```





## <a name="complete-example"></a>Esempio completo


```C++
//
// AnimateLayeredChildWindow.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>
#include <wincodec.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition Header File
#include <dcomp.h>

// Direct2D Header Files
#include <d2d1.h>
#include <d2d1helper.h>

// Desktop Window Manager (DWM) Header File
#include <dwmapi.h>


/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT InitializeMainWindow();
    HRESULT InitializeLayeredChildWindow();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionObjects();

    HRESULT CreateDeviceIndependentResources();
    HRESULT CreateDeviceResources();
    void DiscardDeviceResources();

    HRESULT OnChildClick();
    HRESULT OnChildRender();

    HRESULT LoadResourceD2DBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
        ID2D1Bitmap **ppBitmap
        );

    static LRESULT CALLBACK MainWndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

    static LRESULT CALLBACK ChildWndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );
    
 private:
    int m_dpiX;
    int m_dpiY;
    int m_childOffsetX;
    int m_childOffsetY;

    HWND m_hwndMain;
    HWND m_hwndLayeredChild;

    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
    ID2D1HwndRenderTarget *m_pRenderTarget;
    ID2D1Factory *m_pD2DFactory;
    ID2D1Bitmap *m_pBitmap;
    IWICImagingFactory *m_pWICFactory;

 };


//
// AnimateLayeredChildWindow.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Click the thumnail image to animate the transition
//   of the child window from thumbsize to fullsize. Click the child
//   window again to reset.

#include &quot;AnimateLayeredChildWindow.h&quot;

#define TIMER_ID 100

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE   /* hInstance */,
    HINSTANCE   /* hPrevInstance */,
    LPSTR       /* lpCmdLine */,
    int         /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.InitializeMainWindow()) && SUCCEEDED(app.InitializeLayeredChildWindow()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                        *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_dpiX(0),
    m_dpiY(0),
    m_childOffsetX(20),
    m_childOffsetY(40),
    m_hwndMain(NULL),
    m_hwndLayeredChild(NULL),
    m_pDevice(NULL),
    m_pCompTarget(NULL),
    m_pRenderTarget(NULL),
    m_pBitmap(NULL),
    m_pD2DFactory(NULL),
    m_pWICFactory(NULL)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pRenderTarget);
    SafeRelease(&m_pBitmap),
    SafeRelease(&m_pD2DFactory);
    SafeRelease(&m_pWICFactory);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::InitializeMainWindow()
{
    HRESULT hr = S_OK;

    // Initialize device-independent resources, such 
    // as the Direct2D factory.
    hr = CreateDeviceIndependentResources();
    if (SUCCEEDED(hr))
    {
        // Register the main window class.
        WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
        wcex.style         = 0;
        wcex.lpfnWndProc   = DemoApp::MainWndProc;
        wcex.cbClsExtra    = 0;
        wcex.cbWndExtra    = sizeof(LONG_PTR);
        wcex.hInstance     = HINST_THISCOMPONENT;
        wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
        wcex.lpszMenuName  = NULL;
        wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
        wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

        RegisterClassEx(&wcex);

        RECT rect = { };
        SetRect(&rect, 0, 0, 640, 480);
        AdjustWindowRect(&rect, WS_OVERLAPPED | WS_SYSMENU, FALSE); 

        // Create the main application window.
        //

        // Because the CreateWindow function takes its size in pixels, we
        // obtain the system DPI and use it to scale the window size.
        HDC hdc = GetDC(NULL);
        if (hdc)
        {
            m_dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
            m_dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
            ReleaseDC(NULL, hdc);
        }

        float width = static_cast<float>(rect.right - rect.left);
        float height = static_cast<float>(rect.bottom - rect.top);

        m_hwndMain = CreateWindow(
            L&quot;DirectCompDemoApp&quot;,
            L&quot;DirectComposition Demo Application&quot;,
            WS_OVERLAPPED | WS_SYSMENU,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(width * m_dpiX / 96.f)),
            static_cast<UINT>(ceil(height * m_dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
    }

    hr = m_hwndMain ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Create and initialize the DirectCompositoin objects.
        hr =  InitializeDirectCompositionObjects();
    }

    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwndMain, SW_SHOWNORMAL);
        UpdateWindow(m_hwndMain);
    }
  
    return hr;
}

/*******************************************************************
*                                                                  *
* Create the layered child window.                                 *
*                                                                  *
/******************************************************************/

HRESULT DemoApp::InitializeLayeredChildWindow()
{
    int thumbWidth = 48;
    int thumbHeight = 32;

    HRESULT hr = S_OK;

    WNDCLASSEXW wcex;
    wcex.cbSize         = sizeof(wcex);
    wcex.style          = 0;
    wcex.lpfnWndProc    = DemoApp::ChildWndProc;
    wcex.cbClsExtra     = 0;
    wcex.cbWndExtra     = 0;
    wcex.hInstance      = HINST_THISCOMPONENT;
    wcex.hIcon          = NULL;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH) GetStockObject (GRAY_BRUSH);
    wcex.lpszMenuName   = NULL;
    wcex.lpszClassName  = L&quot;DCompLayeredChildWindow&quot;;
    wcex.hIconSm        = NULL;
    
    if (!RegisterClassExW(&wcex))
    {
        return FALSE;
    }

    m_hwndLayeredChild = CreateWindowEx(WS_EX_LAYERED,
        L&quot;DCompLayeredChildWindow&quot;,                
        NULL,                                    
        WS_CHILD | WS_CLIPSIBLINGS,             
        0, 
        0, 
        static_cast<UINT>(ceil(640.0f * m_dpiX / 96.0f)),
        static_cast<UINT>(ceil(480.0f * m_dpiY / 96.0f)),                                  
        m_hwndMain,                               
        NULL,                                     
        HINST_THISCOMPONENT,                    
        this);                                   

    hr = m_hwndLayeredChild ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Set the opacity and transparency color key of the layered 
        // child window.
        if (!SetLayeredWindowAttributes(m_hwndLayeredChild, 0, 255, LWA_ALPHA))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // While the child window is fullsize, load the bitmap resource and
        // render it to the child window.  
        hr = CreateDeviceResources(); 
    }
    
    if (SUCCEEDED(hr))
    {
        // Reduce the window to thumbsize.
        MoveWindow(m_hwndLayeredChild, m_childOffsetX, m_childOffsetY, 
            thumbWidth, thumbHeight, TRUE);
        ShowWindow(m_hwndLayeredChild, SW_SHOWNORMAL);
        UpdateWindow(m_hwndLayeredChild);
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionObjects()
{
    HRESULT hr = S_OK;

    // Create a DirectComposition device object. 
    hr = DCompositionCreateDevice(nullptr, __uuidof(IDCompositionDevice), 
        reinterpret_cast<void**>(&m_pDevice));

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwndMain, TRUE, &m_pCompTarget);   
    }

    return hr;
}


/******************************************************************
*                                                                 *
*  This method is used to create resources which are not bound    *
*  to any device. Their lifetime effectively extends for the      *
*  duration of the app.                                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pWICFactory)
        );

    if (SUCCEEDED(hr))
    {
        // Create a Direct2D factory.
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the D2D bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateDeviceResources()
{
    HRESULT hr = S_OK;

    RECT rc;
    GetClientRect(m_hwndLayeredChild, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(
        rc.right - rc.left,
        rc.bottom - rc.top
        );

    // Create a Direct2D render target.
    hr = m_pD2DFactory->CreateHwndRenderTarget(
        D2D1::RenderTargetProperties(),
        D2D1::HwndRenderTargetProperties(m_hwndLayeredChild, size),
        &m_pRenderTarget
        );

    if (SUCCEEDED(hr))
    {
        hr = LoadResourceD2DBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L&quot;WhiteFlowers&quot;,
            L&quot;Image&quot;,
            &m_pBitmap
            );
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardDeviceResources()
{
    SafeRelease(&m_pRenderTarget);
    SafeRelease(&m_pBitmap);
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message handler.                             *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::MainWndProc(HWND hwnd, UINT message, 
    WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
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
 
            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardDeviceResources();
                }
                wasHandled = true;
                result = 1;
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

/******************************************************************
*                                                                 *
*  The layered child window&#39;s message handler.                    *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::ChildWndProc(HWND hwnd, UINT message, 
    WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
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
            case WM_PAINT:
                {
                    pDemoApp->OnChildRender();
                    ValidateRect(hwnd, NULL);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_LBUTTONDOWN:
                {
                    HRESULT hr = S_OK;
                    static BOOL fThumbsize = TRUE;

                    // If the child window is already fullsize, reset
                    // the visual tree and return the child window
                    // to thumbsize and move it to its initial location.
                    if (!fThumbsize)
                    {
                        pDemoApp->m_pCompTarget->SetRoot(NULL);
                        hr = pDemoApp->m_pDevice->Commit();  

                        MoveWindow(pDemoApp->m_hwndLayeredChild, 
                            pDemoApp->m_childOffsetX, 
                            pDemoApp->m_childOffsetY, 48, 32, TRUE);

                        pDemoApp->OnChildRender();
                    }   
                    else
                    {
                        // Cloak the child window.
                        BOOL fCloak = TRUE;
                        DwmSetWindowAttribute(pDemoApp->m_hwndLayeredChild,
                            DWMWA_CLOAK,
                            &fCloak,
                            sizeof(fCloak));

                        pDemoApp->OnChildClick();
                    }                    
                    fThumbsize = !fThumbsize;
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_TIMER:
                {
                    // Uncloak the child window.
                    BOOL fCloak = FALSE;
                    DwmSetWindowAttribute(pDemoApp->m_hwndLayeredChild,
                        DWMWA_CLOAK,
                        &fCloak,
                        sizeof(fCloak)); 
                    KillTimer(pDemoApp->m_hwndLayeredChild, TIMER_ID);
                }
                wasHandled = true;
                result = 0;
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


/******************************************************************
*                                                                 *
*  Draws a bitmap in the layered child window.                    *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnChildRender()
{
    HRESULT hr = S_OK;
 
    // Retrieve the size of the render target.
    D2D1_SIZE_F size = m_pRenderTarget->GetSize();
    
    m_pRenderTarget->BeginDraw();
    
    // Draw a bitmap scaled to fill the window.
    m_pRenderTarget->DrawBitmap(
        m_pBitmap,
        D2D1::RectF(0.0f, 0.0f, size.width, size.height)
        );

    hr = m_pRenderTarget->EndDraw();

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Handles a mouse click in the layered child window by animating *
*  the transition from a thumbsize window to a fullsize window.   *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnChildClick()
{
    int fullWidth = 640;
    int fullHeight = 480;
    HRESULT hr = S_OK;

    IDCompositionVisual *pVisual = nullptr;
    IUnknown* pSurface    = nullptr;

    hr = m_pDevice->CreateVisual(&pVisual);
    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateSurfaceFromHwnd(m_hwndLayeredChild, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        hr = pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pCompTarget->SetRoot(pVisual);
    }

    if (SUCCEEDED(hr))
    {
       // Position the visual at the same location as the
       // the child window.
        hr = pVisual->SetOffsetX(static_cast<float>(m_childOffsetX));
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(static_cast<float>(m_childOffsetY));  
        }
    }


    IDCompositionAnimation *pAnimateX = NULL;
    IDCompositionAnimation *pAnimateY = NULL;

    if (SUCCEEDED(hr))
    {
        // Create the animation objects.
        hr = m_pDevice->CreateAnimation(&pAnimateX);
        if (SUCCEEDED(hr))
        {
            hr = m_pDevice->CreateAnimation(&pAnimateY);
        }
    }

    IDCompositionAnimation *pAnimateScale = NULL;
    IDCompositionScaleTransform *pScale = NULL;

    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateAnimation(&pAnimateScale);
    }

    if (SUCCEEDED(hr))
    {
        // Create the scale transform object.
        hr = m_pDevice->CreateScaleTransform(&pScale);
    }

    if (SUCCEEDED(hr))
    {
        // Calculate the X and Y offsets that will position the child window 
        // in the center of the main window&#39;s client area.
        RECT rcParent = { };
        RECT rcChild = { };
        GetClientRect(m_hwndMain, &rcParent);
        GetClientRect(m_hwndLayeredChild, &rcChild);
        float endValX = rcParent.right / 2.0f - rcChild.right / 2.0f;
        float endValY = rcParent.bottom / 2.0f - rcChild.bottom / 2.0f;
 
        // Build the animation functions that will move the visual to the 
        // center of the main window&#39;s client area.
        pAnimateX->AddCubic(0.0f, static_cast<float>(m_childOffsetX), 
            endValX - m_childOffsetX, 0.0f, 0.0f);
        pAnimateX->End(0.9f, endValX);

        pAnimateY->AddCubic(0.0f, static_cast<float>(m_childOffsetY), 
            endValY - m_childOffsetY, 0.0f, 0.0f);
        pAnimateY->End(0.9f, endValY);

        // Associate the animation objects with the offset properties of 
        // the visual.
        hr = pVisual->SetOffsetX(pAnimateX);
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(pAnimateY);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual tree.
        hr = m_pDevice->Commit();  

        // Give the animation a chance to run.
        Sleep(900);
    }

    if (SUCCEEDED(hr))
    {
        // Align the visual with the upper-left corner of the
        // parent window&#39;s client area.
        pVisual->SetOffsetX(0.0);
        pVisual->SetOffsetY(0.0);

        // Enlarge the child window to fill the main window.
        if (!MoveWindow(m_hwndLayeredChild, 0, 0, fullWidth, fullHeight, TRUE))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // Add animation primitives that define the animation object function 
        // used to scale up the child window&#39;s bitmap.
        pAnimateScale->AddCubic(
            0.0f,  // offset from beginning of animation function, in seconds
            0.0f,  // constant coefficient  
            1.0f,  // linear coefficient
            0.0f,  // quadratic coefficient
            0.0f); // cubic coefficient
        pAnimateScale->End(1.0f, 1.0f);

        // Find the center of the child window.
        RECT rcChild = { };
        GetClientRect(m_hwndLayeredChild, &rcChild);
        float centerX = rcChild.right / 2.0f;
        float centerY = rcChild.bottom / 2.0f;

        // Scale from the center point of the child window&#39;s bitmap.
        pScale->SetCenterX(centerX);
        pScale->SetCenterY(centerY);

        // Use the same animation object to animate the X and Y scale
        // factors.
        pScale->SetScaleX(pAnimateScale);
        pScale->SetScaleY(pAnimateScale);

        // Set the Transform property of the visual to use the scale 
        // transform.
        hr = pVisual->SetTransform(pScale);
    }
    
    if (SUCCEEDED(hr))
    {   // Commit the visual tree.
        hr = m_pDevice->Commit();  

        // Use a WM_TIMER message in the child window procedure 
        // to uncloak the child window. 
        SetTimer(m_hwndLayeredChild, TIMER_ID, 1000, NULL);
    }

    SafeRelease(&pAnimateX);
    SafeRelease(&pAnimateY);
    SafeRelease(&pVisual);
    SafeRelease(&pAnimateScale);
    SafeRelease(&pScale);
    
    return hr;
}


/******************************************************************
*                                                                 *
*  This method will create a Direct2D bitmap from an application  *
*  resource.                                                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceD2DBitmap(
    ID2D1RenderTarget *pRenderTarget,
    IWICImagingFactory *pIWICFactory,
    PCWSTR resourceName,
    PCWSTR resourceType,
    ID2D1Bitmap **ppBitmap
    )
{
    HRESULT hr = S_OK;
    IWICBitmapDecoder *pDecoder = NULL;
    IWICBitmapFrameDecode *pSource = NULL;
    IWICStream *pStream = NULL;
    IWICFormatConverter *pConverter = NULL;

    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource.
    imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);

    hr = imageResHandle ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Load the resource.
        imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

        hr = imageResDataHandle ? S_OK : E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        // Lock it to get a system memory pointer.
        pImageFile = LockResource(imageResDataHandle);

        hr = pImageFile ? S_OK : E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        // Calculate the size.
        imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

        hr = imageFileSize ? S_OK : E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        // Create a WIC stream to map onto the memory.
        hr = pIWICFactory->CreateStream(&pStream);
    }

    if (SUCCEEDED(hr))
    {
        // Initialize the stream with the memory pointer and size.
        hr = pStream->InitializeFromMemory(
            reinterpret_cast<BYTE*>(pImageFile),
            imageFileSize
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create a decoder for the stream.
        hr = pIWICFactory->CreateDecoderFromStream(
            pStream,
            NULL,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create the initial frame.
        hr = pDecoder->GetFrame(0, &pSource);
    }

    if (SUCCEEDED(hr))
    {
        // Convert the image format to 32bppPBGRA
        // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
        hr = pIWICFactory->CreateFormatConverter(&pConverter);
    }

    if (SUCCEEDED(hr))
    {
        hr = pConverter->Initialize(
            pSource,
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            NULL,
            0.f,
            WICBitmapPaletteTypeMedianCut
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create a Direct2D bitmap from the WIC bitmap.
        hr = pRenderTarget->CreateBitmapFromWicBitmap(
            pConverter,
            NULL,
            ppBitmap
            );
    }

    SafeRelease(&pDecoder);
    SafeRelease(&pSource);
    SafeRelease(&pStream);
    SafeRelease(&pConverter);

    return hr;
}
```





## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Animazione](animation.md)
</dt> <dt>

[Oggetti bitmap](bitmap-surfaces.md)
</dt> <dt>

[Esempio di finestra figlio su più livelli DirectComposition](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionLayeredChildWindow)
</dt> </dl>

 

 