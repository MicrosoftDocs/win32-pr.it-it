---
title: Come assicurarsi che l'applicazione venga visualizzata correttamente su schermi con valori DPI elevati (DirectWrite)
description: Viene descritto come assicurarsi che l'applicazione crei una finestra che viene visualizzata correttamente su schermi con valori DPI elevati.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406424"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="2ad39-103">Come assicurarsi che l'applicazione venga visualizzata correttamente su schermi con valori DPI elevati</span><span class="sxs-lookup"><span data-stu-id="2ad39-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="2ad39-104">Anche [se DirectWrite](direct-write-portal.md) risolve automaticamente molti problemi di DPI elevati, è necessario eseguire due passaggi per garantire che l'applicazione funzioni correttamente su schermi con valori DPI elevati:</span><span class="sxs-lookup"><span data-stu-id="2ad39-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="2ad39-105">Passaggio 1: Usare l'interfaccia DPI di sistema durante la creazione di Windows</span><span class="sxs-lookup"><span data-stu-id="2ad39-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="2ad39-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="2ad39-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="2ad39-107">Gdi</span><span class="sxs-lookup"><span data-stu-id="2ad39-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="2ad39-108">Passaggio 2: Dichiarare che l'applicazione è in grado di riconoscere DPI</span><span class="sxs-lookup"><span data-stu-id="2ad39-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="2ad39-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ad39-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="2ad39-110">Passaggio 1: Usare l'interfaccia DPI di sistema durante la creazione di Windows</span><span class="sxs-lookup"><span data-stu-id="2ad39-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="2ad39-111">Questa operazione può essere eseguita usando [Direct2D](../direct2d/direct2d-portal.md) o [GDI.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="2ad39-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="2ad39-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="2ad39-112">Direct2D</span></span>

<span data-ttu-id="2ad39-113">[**L'interfaccia ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornisce il [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per il recupero dell'interfaccia DPI di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ad39-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="2ad39-114">Fornisce le dimensioni orizzontali e verticali della visualizzazione in punti per pollice (DPI).</span><span class="sxs-lookup"><span data-stu-id="2ad39-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="2ad39-115">Per usare questi valori per impostare la larghezza di una finestra, usare la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="2ad39-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="2ad39-116"><*DPI orizzontale* >  \*  < *width*, in pixel>/<*valore DPI orizzontale predefinito*></span><span class="sxs-lookup"><span data-stu-id="2ad39-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="2ad39-117">... dove *DPI orizzontale* è il valore ritentato da GetDpi e *DPI orizzontale* predefinito è 96.</span><span class="sxs-lookup"><span data-stu-id="2ad39-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="2ad39-118">La formula è simile per le dimensioni verticali:</span><span class="sxs-lookup"><span data-stu-id="2ad39-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="2ad39-119"><*DPI verticale* >  \*  < *height*, in pixel>/<*DPI verticale predefinito*></span><span class="sxs-lookup"><span data-stu-id="2ad39-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="2ad39-120">... dove *DPI verticale* è il valore recuperato dal [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e *il valore DPI verticale* predefinito è 96.</span><span class="sxs-lookup"><span data-stu-id="2ad39-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="2ad39-121">Il codice seguente usa il [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per creare una finestra 640 x 480, ridimensionata in base al valore DPI di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ad39-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="2ad39-122">Nel codice seguente m *\_ spD2DFactory* è un puntatore intelligente a [**un'istanza id2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)</span><span class="sxs-lookup"><span data-stu-id="2ad39-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


```C++
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
```



### <a name="gdi"></a><span data-ttu-id="2ad39-123">GDI</span><span class="sxs-lookup"><span data-stu-id="2ad39-123">GDI</span></span>

<span data-ttu-id="2ad39-124">[GDI](interoperating-with-gdi.md) fornisce la [**funzione GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) per il recupero delle informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ad39-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="2ad39-125">È possibile recuperare le informazioni DPI passando i *valori di indice LOGPIXELSX* e *LOGPIXELSY.*</span><span class="sxs-lookup"><span data-stu-id="2ad39-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="2ad39-126">La formula per determinare le dimensioni orizzontale e verticale di una finestra è la stessa dell'esempio [Direct2D](../direct2d/direct2d-portal.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="2ad39-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="2ad39-127">Il codice seguente usa la [**funzione GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) per creare una finestra 640 x 480, ridimensionata in base al valore DPI di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ad39-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="2ad39-128">Passaggio 2: Dichiarare che l'applicazione è DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="2ad39-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="2ad39-129">Quando un'applicazione si dichiara in grado di riconoscere DPI, si tratta di un'istruzione che specifica che l'applicazione si comporta bene in base alle impostazioni DPI fino a 200 DPI.</span><span class="sxs-lookup"><span data-stu-id="2ad39-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="2ad39-130">In Windows Vista e Windows 7, quando è abilitata la virtualizzazione DPI, le applicazioni che non supportano DPI vengono ridimensionate e le applicazioni ricevono dati virtualizzati dalle API di sistema, ad esempio la [**funzione GetSystemMetric.**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)</span><span class="sxs-lookup"><span data-stu-id="2ad39-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="2ad39-131">Per dichiarare che l'applicazione è in grado di riconoscere DPI, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="2ad39-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="2ad39-132">Creare un file denominato DeclareDPIAware.manifest.</span><span class="sxs-lookup"><span data-stu-id="2ad39-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="2ad39-133">Copiare il codice XML seguente nel file e salvarlo:</span><span class="sxs-lookup"><span data-stu-id="2ad39-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="2ad39-134">Nel file con estensione vcproj del progetto aggiungere la voce seguente all'interno di ogni elemento Configuration in VisualStudioProject/Configurations:</span><span class="sxs-lookup"><span data-stu-id="2ad39-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2ad39-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ad39-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ad39-136">Direct2D e High-DPI</span><span class="sxs-lookup"><span data-stu-id="2ad39-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 