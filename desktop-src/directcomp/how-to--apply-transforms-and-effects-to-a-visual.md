---
title: Come applicare gli effetti
description: Questo argomento illustra come usare Microsoft DirectComposition per applicare effetti e trasformazioni 3D a un oggetto visivo.
ms.assetid: FE5A0BE9-B84C-4DE1-85D8-375897237F96
keywords:
- come applicare gli effetti DirectComposition
- Effetti DirectComposition, come applicare
- Trasformazioni DirectComposition 3D
- Trasformazioni DirectComposition 3D
- Opacità DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85a3a06fa0650e43f8f1a1be299021cafd233cc59937359dc78bc7b6d25bbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088815"
---
# <a name="how-to-apply-effects"></a>Come applicare gli effetti

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedere [Modernizzare l'app desktop usando il livello Visivo.](/windows/uwp/composition/visual-layer-in-desktop-apps)

Questo argomento illustra come usare Microsoft DirectComposition per applicare effetti e trasformazioni 3D a un oggetto visivo. L'esempio in questo argomento modifica l'opacità di un oggetto visivo e lo ruota intorno a un asse verticale posizionato al centro dell'oggetto visivo. Per altre informazioni sugli altri effetti supportati da DirectComposition, vedere [Effetti](effects.md).

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

### <a name="step-1-initialize-directcomposition-objects"></a>Passaggio 1: Inizializzare oggetti DirectComposition

1.  Creare l'oggetto dispositivo e l'oggetto di destinazione della composizione.
2.  Creare un oggetto visivo, impostarne il contenuto e aggiungerlo alla struttura ad albero visuale.

Per altre informazioni, vedere [Come inizializzare DirectComposition.](initialize-directcomposition.md)

### <a name="step-2-create-a-3d-rotate-transform-object-an-effect-group-object-and-an-animation-object"></a>Passaggio 2: Creare un oggetto di trasformazione rotazione 3D, un oggetto gruppo di effetti e un oggetto di animazione

Usare il [**metodo IDCompositionDevice::CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) per creare un oggetto di trasformazione di rotazione 3D e il [**metodo CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) per creare un oggetto gruppo di effetti. Questo esempio usa anche il [**metodo CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) per creare un oggetto di animazione per animare la trasformazione di rotazione 3D. Per altre informazioni sull'applicazione di animazioni, vedere [Come applicare animazioni](how-to--animate-a-visual.md).


```C++
    HRESULT hr = S_OK;

    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionRotateTransform3D *pRotate3D = nullptr;
    IDCompositionEffectGroup *pEffectGroup = nullptr;


    // Create a 3D rotate transform object.
    hr = m_pDevice->CreateRotateTransform3D(&pRotate3D);

    if (SUCCEEDED(hr))
    {
        // Create an effect group object.
        hr = m_pDevice->CreateEffectGroup(&pEffectGroup);
    }
    
    if (SUCCEEDED(hr))
    {
        // Create an animation object.
        hr = m_pDevice->CreateAnimation(&pAnimation);
    }
```





### <a name="step-3-define-the-animation-function"></a>Passaggio 3: Definire la funzione di animazione

Usare i metodi [**dell'oggetto IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) per definire la funzione di animazione.

Nell'esempio seguente viene definita una funzione di animazione semplice. Quando viene applicata a una proprietà dell'oggetto, la funzione di animazione modifica in modo incrementale il valore della proprietà da 0 al valore dell'argomento *degrees* nel corso di un secondo.


```C++
    if (SUCCEEDED(hr))
    {
        // Define the animation function.
        pAnimation->AddCubic(0.0f, 0.0f, degrees, 0.0f, 0.0f);
        pAnimation->End(1.0f, degrees);
```



### <a name="step-4-set-the-properties-of-the-3d-rotate-transform"></a>Passaggio 4: Impostare le proprietà della trasformazione Rotazione 3D

1.  Applicare la funzione di animazione alla proprietà Angle della trasformazione di rotazione 3D chiamando il [**metodo IDCompositionRotateTransform3D::SetAngle.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation))
2.  Impostare l'asse di rotazione per la trasformazione di rotazione 3D chiamando i metodi [**IDCompositionRotateTransform3D::SetAxisX,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)) [**SetAxisY**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisy)e [**SetAxisZ.**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisz)
3.  Impostare il centro di rotazione per la trasformazione di rotazione 3D chiamando i metodi [**IDCompositionRotateTransform3D::SetCenterX**](/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)) [**e SetCenterY.**](/previous-versions/windows/desktop/legacy/hh448988(v=vs.85))

L'esempio seguente configura una trasformazione di rotazione 3D per ruotare un oggetto visivo intorno a un asse verticale che si trova al centro dell'oggetto visivo. I *parametri m \_ bitmapWidth* *e m \_ bitmapHeight* sono la larghezza e l'altezza della bitmap, in pixel.


```C++
        // Set the properties of the rotate transform object.  
        //
        // Apply the animation object to the Angle property so that
        // the visual will appear to spin around an axis. 
        pRotate3D->SetAngle(pAnimation);

        // Set a vertical axis through the center of the visual's bitmap. 
        pRotate3D->SetAxisX(0.0f);
        pRotate3D->SetAxisY(1.0f);
        pRotate3D->SetAxisZ(0.0f);

        // Set the center of rotation to the center of the visual's bitmap.
        pRotate3D->SetCenterX(m_bitmapWidth / 2.0f);
        pRotate3D->SetCenterY(m_bitmapHeight / 2.0f);
    }
```



### <a name="step-5-set-the-properties-of-the-effect-group-object"></a>Passaggio 5: Impostare le proprietà dell'oggetto gruppo di effetti

1.  Applicare l'oggetto trasformazione rotazione 3D alla proprietà Transform3D dell'oggetto gruppo di effetti chiamando il [**metodo IDCompositionEffectGroup::SetTransform3D.**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d)
2.  Impostare la proprietà Opacity dell'oggetto gruppo di effetti chiamando [**IDCompositionEffectGroup::SetOpacity**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-setopacity(float)).


```C++
    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to the Tranform3D property
        // of the effect group object.
        hr = pEffectGroup->SetTransform3D(pRotate3D);
    }


    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }
```





### <a name="step-6-apply-the-effect-group-object-to-the-effect-property-of-the-visual"></a>Passaggio 6: Applicare l'oggetto gruppo di effetti alla proprietà Effect dell'oggetto visivo

Chiamare il [**metodo IDCompositionVisual::SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) per applicare l'oggetto gruppo di effetti all'oggetto visivo.


```C++
    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = pVisual->SetEffect(pEffectGroup);
    }
```



### <a name="step-7-commit-the-composition"></a>Passaggio 7: Eseguire il commit della composizione

Chiamare il [**metodo IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit del batch di comandi a DirectComposition per l'elaborazione. La composizione risultante viene visualizzata nella finestra di destinazione.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }
```



### <a name="step-8-free-the-directcomposition-objects"></a>Passaggio 8: Liberare gli oggetti DirectComposition

Assicurarsi di liberare l'oggetto di animazione, l'oggetto trasformazione rotazione 3D e l'oggetto gruppo di effetti quando non sono più necessari. Nell'esempio seguente viene chiamata la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti .


```C++
    // Release the DirectComposition objects.
    SafeRelease(&pAnimation);
    SafeRelease(&pRotate3D);
    SafeRelease(&pEffectGroup);
```



Ricordarsi anche di liberare l'oggetto dispositivo, l'oggetto di destinazione della composizione e l'oggetto visivo prima della chiusura dell'applicazione. Per altre informazioni, vedere [Come inizializzare DirectComposition.](initialize-directcomposition.md)

## <a name="complete-example"></a>Esempio completo


```C++
//
// ApplyEffects.h
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

// C RunTime Header Files
#include <math.h>

// DirectComposition and Direct3D Header Files
#include <dcomp.h>
#include <d3d11.h>

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

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT CreateResources();
    void DiscardResources();

    HRESULT OnPaint();
    HRESULT OnClientClick(int xPos, int yPos);
    HRESULT OnMouseMove(int xPos, int yPos);

    HRESULT LoadResourceGDIBitmap(
        PCWSTR resourceName, 
        HBITMAP &hbmp
        );

    HRESULT MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface);

    HRESULT SetVisualOpacity(IDCompositionVisual *pVisual, float opacity);
    HRESULT RotateVisual(IDCompositionVisual *pVisual,float degrees);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;
    HBITMAP m_hBitmap;
    int m_bitmapWidth;
    int m_bitmapHeight;
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
    IDCompositionVisual *m_pVisual;
 };


//
// ApplyEffects.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Hover over the image to see the opacity change. Click
//   the image to apply a 3D rotation.

#include &quot;ApplyEffects.h&quot;

#define OFFSET_X 20
#define OFFSET_Y 20
#define TRANSPARENT 0.5
#define OPAQUE 1.0

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
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

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_hBitmap(NULL),
    m_pDevice(nullptr),
    m_pCompTarget(nullptr),
    m_pD3D11Device(nullptr),
    m_pVisual(nullptr),
    m_bitmapHeight(0),
    m_bitmapWidth(0)
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
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pVisual);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        L&quot;DirectCompDemoApp&quot;,
        L&quot;DirectComposition Demo Application&quot;,
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
        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
    }

    if (SUCCEEDED(hr))
    {
       ShowWindow(m_hwnd, SW_SHOWNORMAL);
       UpdateWindow(m_hwnd);
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

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object.
    D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT,
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        NULL);

    IDXGIDevice *pDXGIDevice = nullptr;

    hr = (m_pD3D11Device == nullptr) ? E_UNEXPECTED : S_OK;
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pCompTarget);   
    }

    SafeRelease(&pDXGIDevice);

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the GDI bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L&quot;Penguins&quot;, m_hBitmap);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    DeleteObject(m_hBitmap);
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
*  Called when the application&#39;s main window is painted. This     *
*  method builds a simple visual tree and passes it to            *
*  DirectComposition.                                             *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnPaint()
{
    HRESULT hr = S_OK;
    IDCompositionSurface *pSurface = nullptr;

    // Create a visual object.          
    hr = m_pDevice->CreateVisual(&m_pVisual);  

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = m_pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        m_pVisual->SetOffsetX(OFFSET_X);  
        m_pVisual->SetOffsetY(OFFSET_Y);  
        hr = SetVisualOpacity(m_pVisual, TRANSPARENT);
    }

   if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pCompTarget->SetRoot(m_pVisual);  
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Called when the mouse moves in the main window&#39;s client area.  *
*  This method determines whether the mouse cursor is over the    *
*  visual, and calls an application-defined function to set the   *
*  visual&#39;s opacity.                                              *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnMouseMove(int xPos, int yPos)
{
    HRESULT hr = S_OK;
    static BOOL fOverImage = FALSE;

    // Determine whether the cursor is over the visual.
    if ((xPos >= OFFSET_X && xPos <= (OFFSET_X + m_bitmapWidth))
        && (yPos >= OFFSET_Y && yPos <= (OFFSET_Y + m_bitmapHeight)))
    {
        if (!fOverImage)
        {
            // The cursor has moved over the visual, so make the visual 
            // 100% opaque.
            hr = SetVisualOpacity(m_pVisual, OPAQUE);
            fOverImage = TRUE;
        }
    }

    else if (fOverImage)
    {
        // The cursor has moved off the visual, so make the visual
        // 50% opaque.
        hr = SetVisualOpacity(m_pVisual, TRANSPARENT);
        fOverImage = FALSE;
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Changes the opacity of a visual.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::SetVisualOpacity(IDCompositionVisual *pVisual, float opacity)
{
    HRESULT hr = S_OK;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (opacity > 1.0f || opacity < 0.0f))
        return E_INVALIDARG;

    // Create an effect group object.
    hr = m_pDevice->CreateEffectGroup(&pEffectGroup);

    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = m_pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Free the effect group object.
    SafeRelease(&pEffectGroup);

    return hr;
}


/******************************************************************
*                                                                 *
*  Called when the user clicks in the main window&#39;s client area.  *
*  This method determines whether the mouse cursor is over the    *
*  visual and calls an application-defined function to rotate the *
*  visual.                                                        *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnClientClick(int xPos, int yPos)
{
    HRESULT hr = S_OK;

    // Determine whether the mouse cursor is over the visual. If so,
    // rotate the visual.
    if ((xPos >= OFFSET_X && xPos <= (OFFSET_X + m_bitmapWidth))
        && (yPos >= OFFSET_Y && yPos <= (OFFSET_Y + m_bitmapHeight)))
    {
        hr = RotateVisual(m_pVisual, 360.0f);
    }
    
    return hr;
}

/******************************************************************
*                                                                 *
*  Performs an animated 3D rotation of a visual.                  *
*                                                                 *
******************************************************************/

HRESULT DemoApp::RotateVisual(IDCompositionVisual *pVisual, float degrees)
{
    HRESULT hr = S_OK;

    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionRotateTransform3D *pRotate3D = nullptr;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (degrees > 360.0f || degrees < -360.0f))
        return E_INVALIDARG;

    // Create a 3D rotate transform object.
    hr = m_pDevice->CreateRotateTransform3D(&pRotate3D);

    if (SUCCEEDED(hr))
    {
        // Create an effect group object.
        hr = m_pDevice->CreateEffectGroup(&pEffectGroup);
    }
    
    if (SUCCEEDED(hr))
    {
        // Create an animation object.
        hr = m_pDevice->CreateAnimation(&pAnimation);
    }

    if (SUCCEEDED(hr))
    {
        // Define the animation function.
        pAnimation->AddCubic(0.0f, 0.0f, degrees, 0.0f, 0.0f);
        pAnimation->End(1.0f, degrees);

        // Set the properties of the rotate transform object.  
        //
        // Apply the animation object to the Angle property so that
        // the visual will appear to spin around an axis. 
        pRotate3D->SetAngle(pAnimation);

        // Set a vertical axis through the center of the visual&#39;s bitmap. 
        pRotate3D->SetAxisX(0.0f);
        pRotate3D->SetAxisY(1.0f);
        pRotate3D->SetAxisZ(0.0f);

        // Set the center of rotation to the center of the visual&#39;s bitmap.
        pRotate3D->SetCenterX(m_bitmapWidth / 2.0f);
        pRotate3D->SetCenterY(m_bitmapHeight / 2.0f);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to the Tranform3D property
        // of the effect group object.
        hr = pEffectGroup->SetTransform3D(pRotate3D);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Release the DirectComposition objects.
    SafeRelease(&pAnimation);
    SafeRelease(&pRotate3D);
    SafeRelease(&pEffectGroup);

    return hr;
}


/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, 
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
            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClientClick(LOWORD(lParam), HIWORD(lParam));
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_MOUSEMOVE:
                {
                    pDemoApp->OnMouseMove(LOWORD(lParam), HIWORD(lParam));
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_PAINT:
                {
                    pDemoApp->OnPaint();
                    ValidateRect(hwnd, NULL);
                }
                wasHandled = true;
                result = 0;
                break;

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
                    pDemoApp->DiscardResources();
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
*  This method loads the specified GDI bitmap from the            *
*  application resources, creates a new bitmap that is in a       *
*  format that DirectComposition can use, and copies the contents *
*  of the original bitmap to the new bitmap.                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceGDIBitmap(PCWSTR resourceName, HBITMAP &hbmp)
{
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}

// CreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    hr =  hBitmap ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Get information about the bitmap.
        bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);
    }

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        m_bitmapWidth = bmp.bmWidth;
        m_bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(m_bitmapWidth, m_bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    hr = pDCSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Create a compatible (DC) and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                m_bitmapWidth, m_bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    SafeRelease(&pDXGISurface);

    return hr;
}
```





## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti](effects.md)
</dt> </dl>

 

 