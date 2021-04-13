---
title: Come compilare una semplice struttura ad albero visuale
description: Questo argomento illustra come compilare una semplice struttura ad albero visuale Microsoft DirectComposition. Nell'esempio riportato in questo argomento viene compilata e composta una struttura ad albero visuale costituita da un oggetto visivo radice e da tre oggetti visivi figlio.
ms.assetid: 86006C3C-67A8-4931-BE76-D0CA9DB19505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621e3f48f76b76be92dc464678dce23b08ebdbd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399046"
---
# <a name="how-to-build-a-simple-visual-tree"></a><span data-ttu-id="ff131-104">Come compilare una semplice struttura ad albero visuale</span><span class="sxs-lookup"><span data-stu-id="ff131-104">How to build a simple visual tree</span></span>

> [!NOTE]
> <span data-ttu-id="ff131-105">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="ff131-105">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="ff131-106">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="ff131-106">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="ff131-107">Questo argomento illustra come compilare una semplice struttura ad albero visuale Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="ff131-107">This topic demonstrates how to build a simple Microsoft DirectComposition visual tree.</span></span> <span data-ttu-id="ff131-108">Nell'esempio riportato in questo argomento viene compilata e composta una struttura ad albero visuale costituita da un oggetto visivo radice e da tre oggetti visivi figlio.</span><span class="sxs-lookup"><span data-stu-id="ff131-108">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <span data-ttu-id="ff131-109">Il contenuto dell'oggetto visivo radice è una bitmap blu chiaro che funge da sfondo per gli oggetti visivi figlio.</span><span class="sxs-lookup"><span data-stu-id="ff131-109">The content of the root visual is a light-blue bitmap that serves as the background for the child visuals.</span></span> <span data-ttu-id="ff131-110">Questa illustrazione mostra la composizione creata dal codice di esempio in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="ff131-110">This illustration shows the composition created by the example code in this topic.</span></span>

![composizione costituita da una bitmap radice e da tre bitmap figlio](images/buildvisualtree.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="ff131-112">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="ff131-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ff131-113">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="ff131-113">Technologies</span></span>

-   [<span data-ttu-id="ff131-114">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="ff131-114">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="ff131-115">Grafica Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ff131-115">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="ff131-116">Infrastruttura grafica DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="ff131-116">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="ff131-117">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="ff131-117">Prerequisites</span></span>

<span data-ttu-id="ff131-118">Conoscenza di:</span><span class="sxs-lookup"><span data-stu-id="ff131-118">Knowledge of:</span></span>

-   <span data-ttu-id="ff131-119">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff131-119">C/C++</span></span>
-   <span data-ttu-id="ff131-120">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="ff131-120">Microsoft Win32</span></span>
-   <span data-ttu-id="ff131-121">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="ff131-121">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="ff131-122">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ff131-122">Instructions</span></span>

### <a name="step-1-initialize-the-device-and-composition-target-objects"></a><span data-ttu-id="ff131-123">Passaggio 1: inizializzare gli oggetti di destinazione del dispositivo e della composizione</span><span class="sxs-lookup"><span data-stu-id="ff131-123">Step 1: Initialize the device and composition target objects</span></span>

<span data-ttu-id="ff131-124">Per ulteriori informazioni, vedere [come inizializzare DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="ff131-124">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-visual-objects-and-set-the-bitmap-content"></a><span data-ttu-id="ff131-125">Passaggio 2: creare gli oggetti visivi e impostare il contenuto della bitmap</span><span class="sxs-lookup"><span data-stu-id="ff131-125">Step 2: Create the visual objects and set the bitmap content</span></span>

<span data-ttu-id="ff131-126">Usare il metodo [**IDCompositionDevice:: CreateVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) per creare gli oggetti visivi e il metodo [**IDCompositionVisual:: secontent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) per impostare il contenuto della bitmap degli oggetti visivi.</span><span class="sxs-lookup"><span data-stu-id="ff131-126">Use the [**IDCompositionDevice::CreateVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) method to create the visuals, and the [**IDCompositionVisual::SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) method to set the bitmap content of the visuals.</span></span>

> [!NOTE]  
> <span data-ttu-id="ff131-127">Nell'esempio seguente, il primo elemento della `m_hBitmaps` matrice contiene la bitmap per l'oggetto visivo radice e gli elementi rimanenti contengono le bitmap per gli oggetti visivi figlio.</span><span class="sxs-lookup"><span data-stu-id="ff131-127">In the following example, the first element of the `m_hBitmaps` array contains the bitmap for the root visual, and the remaining elements contain the bitmaps for the child visuals.</span></span>

```cpp
#define NUM_VISUALS 4 // number of visuals in the composition
HBITMAP m_hBitmaps[NUM_VISUALS];
HRESULT hr = S_OK;

IDCompositionVisual *pVisuals[NUM_VISUALS]{ };
IDCompositionSurface *pSurface{ nullptr };

// Create a visual objects and set their content.   
for (int i = 0; i < NUM_VISUALS; i++)
{
    hr = m_pDevice->CreateVisual(&pVisuals[i]);
    if (SUCCEEDED(hr))
    {
        // This application-defined function creates a DirectComposition
        // surface and renders a GDI bitmap onto the surface. 
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmaps[i], &pSurface);

        if (SUCCEEDED(hr))
        {
            // Set the bitmap content.  
            hr = pVisuals[i]->SetContent(pSurface);
        }

        SafeRelease(&pSurface);
    }

    if (FAILED(hr))
    {
        goto Cleanup;
    }
}
``` 

<span data-ttu-id="ff131-128">La funzione definita dall'applicazione seguente illustra come creare la superficie Microsoft DirectComposition ed eseguire il rendering di una bitmap di Windows Graphics Device Interface (GDI) nella superficie.</span><span class="sxs-lookup"><span data-stu-id="ff131-128">The following application defined function shows how to create the Microsoft DirectComposition surface and render a Windows Graphics Device Interface (GDI) bitmap to the surface.</span></span>

```cpp
// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
     BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
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
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, ppSurface);
    }

    hr = ppSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        hr = (*ppSurface)->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    (*ppSurface)->EndDraw();

    SafeRelease(&pDXGISurface);

    return hr;
}
```

### <a name="step-3-set-the-root-visual"></a><span data-ttu-id="ff131-129">Passaggio 3: impostare l'oggetto visivo radice</span><span class="sxs-lookup"><span data-stu-id="ff131-129">Step 3: Set the root visual</span></span>

<span data-ttu-id="ff131-130">Impostare gli offset orizzontali e verticali dell'oggetto visivo radice e quindi aggiungerlo alla struttura ad albero visuale chiamando il metodo [**IDCompositionTarget:: seroot**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) .</span><span class="sxs-lookup"><span data-stu-id="ff131-130">Set the horizontal and vertical offsets of the root visual, and then add it to the visual tree by calling the [**IDCompositionTarget::SetRoot**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) method.</span></span>

```cpp
float xPosRoot = 50.0;
float yPosRoot = 50.0;

// Set the horizontal and vertical position of the root visual. 
pVisuals[0]->SetOffsetX(xPosRoot);
pVisuals[0]->SetOffsetY(yPosRoot);

// Set the root visual of the visual tree.          
hr = m_pCompTarget->SetRoot(pVisuals[0]);
```

### <a name="step-4-add-the-child-visuals-and-commit-the-composition"></a><span data-ttu-id="ff131-131">Passaggio 4: aggiungere gli oggetti visivi figlio ed eseguire il commit della composizione</span><span class="sxs-lookup"><span data-stu-id="ff131-131">Step 4: Add the child visuals, and commit the composition</span></span>

<span data-ttu-id="ff131-132">Usare i metodi esposti dall'interfaccia [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) di ogni oggetto visivo figlio per impostare il contenuto della bitmap e altre proprietà, quindi usare il metodo [**IDCompositionVisual:: AddVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-addvisual) dell'oggetto visivo radice per aggiungere gli oggetti visivi figlio alla radice della struttura ad albero visuale.</span><span class="sxs-lookup"><span data-stu-id="ff131-132">Use methods exposed by each child visual's [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) interface to set the bitmap content and other properties, and then use the root visual's [**IDCompositionVisual::AddVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-addvisual) method to add the child visuals to the root of the visual tree.</span></span> <span data-ttu-id="ff131-133">Chiamare [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit del batch di comandi in DirectComposition per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ff131-133">Call [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) to commit the batch of commands to DirectComposition for processing.</span></span> <span data-ttu-id="ff131-134">La composizione risultante viene visualizzata nella finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ff131-134">The resulting composition appears in the target window.</span></span>

```cpp
float xPosChild = 20.0f;
float yPosChild = 20.0f;

if (SUCCEEDED(hr))
{
    // Set the positions of the child visuals and add them to the visual tree.
    for (int i = 1; i < NUM_VISUALS; i++)
    {
        pVisuals[i]->SetOffsetX(xPosChild);
        pVisuals[i]->SetOffsetY(
            static_cast<float>((yPosChild * i) + (CHILD_BITMAP_HEIGHT * (i - 1))));

        // Add the child visuals as children of the root visual.
        pVisuals[0]->AddVisual(pVisuals[i], TRUE, nullptr);
    }
}

// Commit the visual to be composed and displayed.
hr = m_pDevice->Commit();
```

### <a name="step-5-free-the-directcomposition-objects"></a><span data-ttu-id="ff131-135">Passaggio 5: liberare gli oggetti DirectComposition</span><span class="sxs-lookup"><span data-stu-id="ff131-135">Step 5: Free the DirectComposition objects</span></span>

<span data-ttu-id="ff131-136">Liberare gli oggetti visivi non appena non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="ff131-136">Free the visual objects as soon as you no longer need them.</span></span> <span data-ttu-id="ff131-137">Questo frammento di codice successivo chiama la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti visivi.</span><span class="sxs-lookup"><span data-stu-id="ff131-137">This next bit of code calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the visual objects.</span></span>

```cpp
Cleanup:
    // Free the visuals.
    for (int i = 0; i < NUM_VISUALS; i++) 
    {
        SafeRelease(&pVisuals[i]);
    }
```

<span data-ttu-id="ff131-138">Inoltre, ricordarsi di liberare gli oggetti di destinazione del dispositivo e della composizione prima che l'applicazione venga chiusa.</span><span class="sxs-lookup"><span data-stu-id="ff131-138">Also, remember to free the device and composition target objects before your application exits.</span></span>

```cpp
SafeRelease(&m_pD3D11Device);
SafeRelease(&m_pDevice);
SafeRelease(&m_pCompTarget);
```

## <a name="complete-example"></a><span data-ttu-id="ff131-139">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="ff131-139">Complete example</span></span>

```cpp
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
#ifndef Assert
#if defined( DEBUG ) || defined( _DEBUG )
#define Assert(b) if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}
#else
#define Assert(b)
#endif //DEBUG || _DEBUG
#endif

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

// Application-defined constants
#define NUM_VISUALS 4       // number of visuals in the composition
#define CHILD_BITMAP_HEIGHT 96    // height, in pixels, of a child visual
#define NUM_BITMAPS 4       // number of bitmaps in the composition

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

    HRESULT OnClientClick();

    HRESULT DemoApp::LoadResourceGDIBitmap(
        PCWSTR resourceName,
        HBITMAP &hbmp
    );
    HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, IDCompositionSurface **ppSurface);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
    );

private:
    HWND m_hwnd;

    HBITMAP m_hBitmaps[NUM_VISUALS];
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
};
```

```cpp
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Right-click in the client area to cause DirectCompostion
// to create a simple composition consisting a root visual and three child 
// visuals. The root visual provides the background bitmap for the 
// composition, and the three child visuals provide bitmaps that are 
// composed on top of the root. All bitmaps are GDI.

#include "SimpleVisualTree.h"

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
    m_hBitmaps(),
    m_pD3D11Device(nullptr),
    m_pDevice(nullptr),
    m_pCompTarget(nullptr)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
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
    wcex.lpszClassName = L"DirectCompDemoApp";

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
        L"DirectCompDemoApp",
        L"DirectComposition Demo Application",
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

        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
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
    IDXGIDevice *pDXGIDevice = nullptr;

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

    hr = (m_pD3D11Device == nullptr) ? E_UNEXPECTED : S_OK;
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, __uuidof(IDCompositionDevice), 
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
*  This method creates the GDI bitmaps to be associated with      *
*  DirectComposition visual objects.                              *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L"Background", m_hBitmaps[0]);
    hr = LoadResourceGDIBitmap(L"BlkKnight", m_hBitmaps[1]);
    hr = LoadResourceGDIBitmap(L"BlkQueen", m_hBitmaps[2]);
    hr = LoadResourceGDIBitmap(L"BlkRook", m_hBitmaps[3]);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    int i = 0;
    while (i < NUM_VISUALS) 
    {
        DeleteObject(m_hBitmaps[i++]);
    }
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
*  Called whenever the user clicks the client area of the main    *
*  window. This method builds a simple visual tree consisting of  *   
*  a root visual and three child visuals.                         *
******************************************************************/

HRESULT DemoApp::OnClientClick()
{
    HRESULT hr = S_OK;

    IDCompositionVisual *pVisuals[NUM_VISUALS] = { };
    IDCompositionSurface *pSurface = nullptr;
    
    // Create a visual objects and set their content.   
    for (int i = 0; i < NUM_VISUALS; i++)
    {
        hr = m_pDevice->CreateVisual(&pVisuals[i]); 
        if (SUCCEEDED(hr))
        {
            // This application-defined function creates a DirectComposition
            // surface and renders a GDI bitmap onto the surface. 
            hr = MyCreateGDIRenderedDCompSurface(m_hBitmaps[i], &pSurface);

            if (SUCCEEDED(hr))
            {
                // Set the bitmap content.  
                hr = pVisuals[i]->SetContent(pSurface);
            }

            SafeRelease(&pSurface);
        }

        if (FAILED(hr))
        {
            goto Cleanup;
        }
    }

    float xPosRoot = 50.0; 
    float yPosRoot = 50.0; 

    // Set the horizontal and vertical position of the root visual. 
    pVisuals[0]->SetOffsetX(xPosRoot);  
    pVisuals[0]->SetOffsetY(yPosRoot);  

    // Set the root visual of the visual tree.          
    hr = m_pCompTarget->SetRoot(pVisuals[0]);  

    float xPosChild = 20.0f;
    float yPosChild = 20.0f;

    if (SUCCEEDED(hr))
    {
        // Set the positions of the child visuals and add them to the visual tree.
        for (int i = 1; i < NUM_VISUALS; i++)
        {
            pVisuals[i]->SetOffsetX(xPosChild);
            pVisuals[i]->SetOffsetY(
                static_cast<float>((yPosChild * i) + (CHILD_BITMAP_HEIGHT * (i - 1))));

            // Add the child visuals as children of the root visual.
            pVisuals[0]->AddVisual(pVisuals[i], TRUE, nullptr);
        }
    }
    
    // Commit the visual to be composed and displayed.
    hr = m_pDevice->Commit();  

Cleanup:
    // Free the visuals.
    for (int i = 0; i < NUM_VISUALS; i++) 
    {
        SafeRelease(&pVisuals[i]);
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

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
                    pDemoApp->OnClientClick();
                }
 
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
    // Load the bitmap from the application resources.
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}

// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
     BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
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
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, ppSurface);
    }

    hr = ppSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        hr = (*ppSurface)->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    (*ppSurface)->EndDraw();

    SafeRelease(&pDXGISurface);

    return hr;
}
```

## <a name="related-topics"></a><span data-ttu-id="ff131-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff131-140">Related topics</span></span>

* [<span data-ttu-id="ff131-141">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="ff131-141">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)
* [<span data-ttu-id="ff131-142">**IDCompositionDevice:: commit**</span><span class="sxs-lookup"><span data-stu-id="ff131-142">**IDCompositionDevice::Commit**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
* [<span data-ttu-id="ff131-143">**IDCompositionDevice::CreateTargetForHwnd**</span><span class="sxs-lookup"><span data-stu-id="ff131-143">**IDCompositionDevice::CreateTargetForHwnd**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd)
* [<span data-ttu-id="ff131-144">**IDCompositionDevice::CreateVisual**</span><span class="sxs-lookup"><span data-stu-id="ff131-144">**IDCompositionDevice::CreateVisual**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual)
* [<span data-ttu-id="ff131-145">**IDCompositionTarget:: seroot**</span><span class="sxs-lookup"><span data-stu-id="ff131-145">**IDCompositionTarget::SetRoot**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot)
* [<span data-ttu-id="ff131-146">**IDCompositionVisual:: secontece**</span><span class="sxs-lookup"><span data-stu-id="ff131-146">**IDCompositionVisual::SetContent**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)
* [<span data-ttu-id="ff131-147">**SafeRelease**</span><span class="sxs-lookup"><span data-stu-id="ff131-147">**SafeRelease**</span></span>](/windows/desktop/medfound/saferelease)