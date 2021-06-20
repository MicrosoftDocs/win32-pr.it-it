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
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Come assicurarsi che l'applicazione venga visualizzata correttamente su schermi con valori DPI elevati

Anche [se DirectWrite](direct-write-portal.md) risolve automaticamente molti problemi di DPI elevati, è necessario eseguire due passaggi per garantire che l'applicazione funzioni correttamente su schermi con valori DPI elevati:

-   [Passaggio 1: Usare l'interfaccia DPI di sistema durante la creazione di Windows](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [Gdi](#gdi)
-   [Passaggio 2: Dichiarare che l'applicazione è in grado di riconoscere DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Argomenti correlati](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Passaggio 1: Usare l'interfaccia DPI di sistema durante la creazione di Windows

Questa operazione può essere eseguita usando [Direct2D](../direct2d/direct2d-portal.md) o [GDI.](../gdi/windows-gdi.md)

### <a name="direct2d"></a>Direct2D

[**L'interfaccia ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornisce il [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per il recupero dell'interfaccia DPI di sistema. Fornisce le dimensioni orizzontali e verticali della visualizzazione in punti per pollice (DPI). Per usare questi valori per impostare la larghezza di una finestra, usare la formula seguente:

<*DPI orizzontale* >  \*  < *width*, in pixel>/<*valore DPI orizzontale predefinito*>

... dove *DPI orizzontale* è il valore ritentato da GetDpi e *DPI orizzontale* predefinito è 96. La formula è simile per le dimensioni verticali:

<*DPI verticale* >  \*  < *height*, in pixel>/<*DPI verticale predefinito*>

... dove *DPI verticale* è il valore recuperato dal [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e *il valore DPI verticale* predefinito è 96.

Il codice seguente usa il [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per creare una finestra 640 x 480, ridimensionata in base al valore DPI di sistema. Nel codice seguente m *\_ spD2DFactory* è un puntatore intelligente a [**un'istanza id2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)


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



### <a name="gdi"></a>GDI

[GDI](interoperating-with-gdi.md) fornisce la [**funzione GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) per il recupero delle informazioni sul dispositivo. È possibile recuperare le informazioni DPI passando i *valori di indice LOGPIXELSX* e *LOGPIXELSY.* La formula per determinare le dimensioni orizzontale e verticale di una finestra è la stessa dell'esempio [Direct2D](../direct2d/direct2d-portal.md) precedente.

Il codice seguente usa la [**funzione GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) per creare una finestra 640 x 480, ridimensionata in base al valore DPI di sistema.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Passaggio 2: Dichiarare che l'applicazione è DPI-Aware

Quando un'applicazione si dichiara in grado di riconoscere DPI, si tratta di un'istruzione che specifica che l'applicazione si comporta bene in base alle impostazioni DPI fino a 200 DPI. In Windows Vista e Windows 7, quando è abilitata la virtualizzazione DPI, le applicazioni che non supportano DPI vengono ridimensionate e le applicazioni ricevono dati virtualizzati dalle API di sistema, ad esempio la [**funzione GetSystemMetric.**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) Per dichiarare che l'applicazione è in grado di riconoscere DPI, seguire questa procedura.

1.  Creare un file denominato DeclareDPIAware.manifest.
2.  Copiare il codice XML seguente nel file e salvarlo:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  Nel file con estensione vcproj del progetto aggiungere la voce seguente all'interno di ogni elemento Configuration in VisualStudioProject/Configurations:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct2D e High-DPI](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 