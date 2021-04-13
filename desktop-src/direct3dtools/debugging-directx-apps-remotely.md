---
title: Debug di app DirectX in modalità remota
description: È possibile usare Visual Studio e Windows 8 SDK per eseguire il debug remoto di app DirectX.
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55548cd282bf643e16f22177e46643c6e283a909
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399699"
---
# <a name="debugging-directx-apps-remotely"></a>Debug di app DirectX in modalità remota

È possibile usare Visual Studio e Windows 8 SDK per eseguire il debug remoto di app DirectX. Windows 8 SDK fornisce un set di componenti che supportano lo sviluppo DirectX e forniscono il controllo degli errori e la convalida dei parametri oltre al debug fornito da Visual Studio. Questi componenti sono D3D11 \_1SDKLayers.dll, D2D1Debug1.dll e Dxgidebug.dll.

Se si desidera eseguire il debug in modalità remota in un computer senza Windows 8 SDK installato e si desidera questa funzionalità di debug aggiuntiva, è necessario installare il pacchetto di debug remoto appropriato per l'architettura in cui si desidera eseguire il debug. I pacchetti Windows Installer in `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` installano il supporto appropriato.

Per abilitare le funzionalità di debug aggiuntive per le app Direct2D, usare il codice seguente:

```cpp
    D2D1_FACTORY_OPTIONS options;
    ZeroMemory(&options, sizeof(D2D1_FACTORY_OPTIONS));

#if defined(_DEBUG)
     // If the project is in a debug build, enable Direct2D debugging via SDK Layers.
    options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
#endif

    DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );         
```

Per abilitare le funzionalità di debug aggiuntive per le app Direct3D, usare il codice seguente:

```cpp
    // This flag supports surfaces with a different color channel ordering than the API default.
    // It is recommended usage, and is required for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    ComPtr<IDXGIDevice> dxgiDevice;

#if defined(_DEBUG)
    // If the project is in a debug build, enable debugging via SDK Layers with this flag.
    creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          // leave as 0 unless software device
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of entries in above list
            D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION for modern
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );
```

Per altre informazioni sul debug di applicazioni Direct2D, vedere [livello di debug Direct2D](/windows/desktop/Direct2D/direct2ddebuglayer-portal).

Per altre informazioni sul debug di app Direct3D, vedere [livello di debug Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).