---
title: Visualizzazione corretta su uno schermo con valori DPI elevati
description: Descrive i passaggi per creare una finestra per l'applicazione che viene visualizzata correttamente nei display con valori DPI elevati.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8ebc6a7621623307d9b2cfd953a5fa3f3387fbacb3faeb345375d925044cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259961"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a>Visualizzazione corretta su uno schermo con valori DPI elevati

Anche se Direct2D risolve automaticamente molti problemi di DPI elevati, è necessario eseguire due passaggi per assicurarsi che l'applicazione funzioni correttamente su schermi con valori DPI elevati:

-   [Passaggio 1: Usare l'interfaccia DPI di sistema durante la creazione Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Passaggio 2: Dichiarare che l'applicazione è in grado di riconoscere DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Argomenti correlati](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Passaggio 1: Usare l'interfaccia DPI di sistema durante la creazione Windows

[**L'interfaccia ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornisce il [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per il recupero dell'interfaccia DPI di sistema. Fornisce le dimensioni orizzontali e verticali della visualizzazione in punti per pollice (DPI). Per usare questi valori per impostare la larghezza di una finestra, usare la formula seguente:

<*DPI orizzontale* >  \*  < *width*, in pixel>/<*valore DPI orizzontale predefinito*>

... dove *DPI orizzontale* è il valore ritentato da [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e *il valore DPI orizzontale* predefinito è 96. La formula è simile per le dimensioni verticali:

<*DPI verticale* >  \*  < *height*, in pixel>/<*valore DPI verticale predefinito*>

... dove *DPI verticale* è il valore recuperato dal [**metodo GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e *il valore DPI verticale* predefinito è 96.

Il codice seguente usa il metodo [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) per recuperare il valore DPI di sistema e quindi crea una finestra di 640 × 480, ridimensionata in base al valore DPI di sistema.


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
> A partire da Windows 8, è possibile usare la [**classe Windows::Graphics::D isplay::D isplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) per ottenere il valore DPI di sistema.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Passaggio 2: Dichiarare che l'applicazione è DPI-Aware

Quando un'applicazione si dichiara in grado di riconoscere DPI, si tratta di un'istruzione che specifica che l'applicazione si comporta bene in base alle impostazioni DPI fino a 200 DPI. In Windows Vista e Windows 7, quando è abilitata la virtualizzazione DPI, le applicazioni che non supportano DPI vengono ridimensionate e le applicazioni ricevono dati virtualizzati dalle API di sistema, ad esempio la [**funzione GetSystemMetric.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Per dichiarare che l'applicazione è in grado di riconoscere DPI, seguire questa procedura.

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

[Direct2D e High-DPI](direct2d-and-high-dpi.md)
</dt> </dl>

 

 