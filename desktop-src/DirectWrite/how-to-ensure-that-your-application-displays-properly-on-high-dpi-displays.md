---
title: Come verificare che l'applicazione venga visualizzata correttamente in schermi a DPI elevato (DirectWrite)
description: Viene descritto come creare una finestra visualizzata correttamente su schermi a DPI elevato.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317eb3379963cec600ab9bac7deb3778f0874e59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338254"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Come verificare che l'applicazione venga visualizzata correttamente su schermi con DPI elevato

Anche se [DirectWrite](direct-write-portal.md) risolve molti problemi ad alta risoluzione dei problemi, è necessario eseguire due passaggi per assicurarsi che l'applicazione funzioni correttamente con schermi a DPI elevato:

-   [Passaggio 1: usare il valore DPI di sistema durante la creazione di Windows](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [GDI](#gdi)
-   [Passaggio 2: dichiarare che l'applicazione è compatibile con DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Argomenti correlati](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Passaggio 1: usare il valore DPI di sistema durante la creazione di Windows

Questa operazione può essere eseguita tramite [Direct2D](../direct2d/direct2d-portal.md) o tramite [GDI](../gdi/windows-gdi.md).

### <a name="direct2d"></a>Direct2D

L'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornisce il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per il recupero del valore dpi del sistema. Fornisce le dimensioni orizzontali e verticali dello schermo in punti per pollice (DPI). Per utilizzare questi valori per impostare la larghezza di una finestra, utilizzare la formula seguente:

<*dpi* >  \* orizzontale  < *larghezza*, in pixel>/<*DPI orizzontale predefinito*>

... dove *DPI orizzontale* è il valore recuperati da GETDPI e *DPI orizzontale predefinito* è 96. La formula è simile alla dimensione verticale:

<*dpi* >  \* verticale  < *altezza*, in pixel>/<*dpi verticale predefinito*>

... dove *dpi verticale* è il valore recuperato dal metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e il valore *dpi verticale predefinito* è 96.

Il codice seguente usa il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per creare una finestra 640 x 480, ridimensionata in base al valore dpi del sistema. Nel codice seguente, *m \_ spD2DFactory* è un puntatore intelligente a un'istanza di [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .


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

[GDI](interoperating-with-gdi.md) fornisce la funzione [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) per il recupero delle informazioni sul dispositivo. È possibile recuperare le informazioni DPI passando i valori di indice *LOGPIXELSX* e *LOGPIXELSY* . La formula per determinare le dimensioni orizzontali e verticali di una finestra è identica a quella dell'esempio [Direct2D](../direct2d/direct2d-portal.md) precedente.

Il codice seguente usa la funzione [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) per creare una finestra 640 x 480, ridimensionata in base al valore dpi del sistema.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Passaggio 2: dichiarare che l'applicazione è DPI-Aware

Quando un'applicazione dichiara se stessa in modo che sia compatibile con DPI, si tratta di un'istruzione che specifica che l'applicazione si comporta bene alle impostazioni DPI fino a 200 DPI. In Windows Vista e Windows 7, quando è abilitata la virtualizzazione DPI, le applicazioni che non sono compatibili con DPI vengono ridimensionate e le applicazioni ricevono dati virtualizzati dalle API di sistema, ad esempio la funzione [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) . Per dichiarare che l'applicazione è compatibile con DPI, completare i passaggi seguenti.

1.  Creare un file denominato DeclareDPIAware. manifest.
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

    

3.  Nel file con estensione vcproj del progetto aggiungere la voce seguente all'interno di ogni elemento di configurazione in Progettovisualstudio/Configurations:
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

 

 