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
# <a name="displaying-properly-on-a-high-dpi-display"></a>Visualizzazione corretta in una visualizzazione a DPI elevato

Anche se Direct2D risolve molti problemi di elevata risoluzione dei problemi, è necessario eseguire due passaggi per assicurarsi che l'applicazione funzioni correttamente su schermi a DPI elevato:

-   [Passaggio 1: usare il valore DPI di sistema durante la creazione di Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Passaggio 2: dichiarare che l'applicazione è compatibile con DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Argomenti correlati](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Passaggio 1: usare il valore DPI di sistema durante la creazione di Windows

L'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornisce il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per il recupero del valore dpi del sistema. Fornisce le dimensioni orizzontali e verticali dello schermo in punti per pollice (DPI). Per utilizzare questi valori per impostare la larghezza di una finestra, utilizzare la formula seguente:

<*dpi* >  \* orizzontale  < *larghezza*, in pixel>/<*DPI orizzontale predefinito*>

... dove *DPI orizzontale* è il valore recuperati da [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e *DPI orizzontale predefinito* è 96. La formula è simile alla dimensione verticale:

<*dpi* >  \* verticale  < *altezza*, in pixel>/<*dpi verticale predefinito*>

... dove *dpi verticale* è il valore recuperato dal metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e il valore *dpi verticale predefinito* è 96.

Il codice seguente usa il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per recuperare il valore dpi di sistema e quindi crea una finestra 640 × 480, ridimensionata in base al valore dpi del sistema.


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
> A partire da Windows 8, è possibile usare la classe [**Windows:: graphics::D:D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) per ottenere il valore dpi del sistema.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Passaggio 2: dichiarare che l'applicazione è DPI-Aware

Quando un'applicazione dichiara se stessa in modo che sia compatibile con DPI, si tratta di un'istruzione che specifica che l'applicazione si comporta bene alle impostazioni DPI fino a 200 DPI. In Windows Vista e Windows 7, quando è abilitata la virtualizzazione DPI, le applicazioni che non sono compatibili con DPI vengono ridimensionate e le applicazioni ricevono dati virtualizzati dalle API di sistema, ad esempio la funzione [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Per dichiarare che l'applicazione è compatibile con DPI, completare i passaggi seguenti.

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

[Direct2D e High-DPI](direct2d-and-high-dpi.md)
</dt> </dl>

 

 