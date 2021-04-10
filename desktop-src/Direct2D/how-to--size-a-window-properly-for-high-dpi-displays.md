---
title: Visualizzazione corretta in una visualizzazione a DPI elevato
description: Viene descritto come creare una finestra visualizzata correttamente su schermi a DPI elevato.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3e82951dfa77e6f61c661b87064dad5cb9f08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963365"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="8279c-103">Visualizzazione corretta in una visualizzazione a DPI elevato</span><span class="sxs-lookup"><span data-stu-id="8279c-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="8279c-104">Anche se Direct2D risolve molti problemi di elevata risoluzione dei problemi, è necessario eseguire due passaggi per assicurarsi che l'applicazione funzioni correttamente su schermi a DPI elevato:</span><span class="sxs-lookup"><span data-stu-id="8279c-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="8279c-105">Passaggio 1: usare il valore DPI di sistema durante la creazione di Windows</span><span class="sxs-lookup"><span data-stu-id="8279c-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="8279c-106">Passaggio 2: dichiarare che l'applicazione è compatibile con DPI</span><span class="sxs-lookup"><span data-stu-id="8279c-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="8279c-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8279c-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="8279c-108">Passaggio 1: usare il valore DPI di sistema durante la creazione di Windows</span><span class="sxs-lookup"><span data-stu-id="8279c-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="8279c-109">L'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornisce il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per il recupero del valore dpi del sistema.</span><span class="sxs-lookup"><span data-stu-id="8279c-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="8279c-110">Fornisce le dimensioni orizzontali e verticali dello schermo in punti per pollice (DPI).</span><span class="sxs-lookup"><span data-stu-id="8279c-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="8279c-111">Per utilizzare questi valori per impostare la larghezza di una finestra, utilizzare la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="8279c-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="8279c-112"><*dpi* >  \* orizzontale  < *larghezza*, in pixel>/<*DPI orizzontale predefinito*></span><span class="sxs-lookup"><span data-stu-id="8279c-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="8279c-113">... dove *DPI orizzontale* è il valore recuperati da [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e *DPI orizzontale predefinito* è 96.</span><span class="sxs-lookup"><span data-stu-id="8279c-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="8279c-114">La formula è simile alla dimensione verticale:</span><span class="sxs-lookup"><span data-stu-id="8279c-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="8279c-115"><*dpi* >  \* verticale  < *altezza*, in pixel>/<*dpi verticale predefinito*></span><span class="sxs-lookup"><span data-stu-id="8279c-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="8279c-116">... dove *dpi verticale* è il valore recuperato dal metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e il valore *dpi verticale predefinito* è 96.</span><span class="sxs-lookup"><span data-stu-id="8279c-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="8279c-117">Il codice seguente usa il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per recuperare il valore dpi di sistema e quindi crea una finestra 640 × 480, ridimensionata in base al valore dpi del sistema.</span><span class="sxs-lookup"><span data-stu-id="8279c-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


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



> [!Note]
>
> <span data-ttu-id="8279c-118">A partire da Windows 8, è possibile usare la classe [**Windows:: graphics::D:D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) per ottenere il valore dpi del sistema.</span><span class="sxs-lookup"><span data-stu-id="8279c-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="8279c-119">Passaggio 2: dichiarare che l'applicazione è DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="8279c-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="8279c-120">Quando un'applicazione dichiara se stessa in modo che sia compatibile con DPI, si tratta di un'istruzione che specifica che l'applicazione si comporta bene alle impostazioni DPI fino a 200 DPI.</span><span class="sxs-lookup"><span data-stu-id="8279c-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="8279c-121">In Windows Vista e Windows 7, quando è abilitata la virtualizzazione DPI, le applicazioni che non sono compatibili con DPI vengono ridimensionate e le applicazioni ricevono dati virtualizzati dalle API di sistema, ad esempio la funzione [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="8279c-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="8279c-122">Per dichiarare che l'applicazione è compatibile con DPI, completare i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8279c-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="8279c-123">Creare un file denominato DeclareDPIAware. manifest.</span><span class="sxs-lookup"><span data-stu-id="8279c-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="8279c-124">Copiare il codice XML seguente nel file e salvarlo:</span><span class="sxs-lookup"><span data-stu-id="8279c-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="8279c-125">Nel file con estensione vcproj del progetto aggiungere la voce seguente all'interno di ogni elemento di configurazione in Progettovisualstudio/Configurations:</span><span class="sxs-lookup"><span data-stu-id="8279c-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="8279c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8279c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8279c-127">Direct2D e High-DPI</span><span class="sxs-lookup"><span data-stu-id="8279c-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 