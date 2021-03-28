---
title: Funzionalità di Direct3D 11,4
description: In Direct3D 11,4 sono state aggiunte le funzionalità seguenti.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963241"
---
# <a name="direct3d-114-features"></a>Funzionalità di Direct3D 11,4

In Direct3D 11,4 sono state aggiunte le funzionalità seguenti.

Vedere anche [dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Rimozione del dispositivo Direct3D

I metodi [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)e [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) sono supportati da una nuova interfaccia, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), per supportare la ricezione di una notifica di evento asincrono quando un dispositivo Direct3D è stato rimosso.

## <a name="multithreaded-protection"></a>Protezione multithreading

Per assicurarsi che i comandi grafici in particolare vengano eseguiti in un ordine specifico, l'interfaccia [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) dispone di metodi per attivare e disattivare la protezione multithread e i metodi per immettere e lasciare codice critico che richiede la protezione.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Barriere per la sincronizzazione di più dispositivi e l'interoperabilità con Direct3D 12

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) e [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) forniscono le stesse funzionalità di recinzione di Direct3D 12 per Direct3D 11. Le recinzioni vengono usate per sincronizzare più dispositivi Direct3D11 e per l'interoperabilità tra Direct3D 11 e Direct3D 12. Gli schermi sono supportati in Windows 10 Creators Update.

## <a name="extended-nv12-texture-support"></a>Supporto per la trama NV12 estesa

Le trame NV12 con funzionalità di acquisizione e codifica video supportano ora la condivisione. I flag di trama D3D11 precedenti per la codifica e l'acquisizione video sono deprecati per NV12, in quanto verranno impostati continuamente per i nuovi driver. Tali trame possono essere condivise non solo con D3D11, ma anche con D3D12. In D3D12 non sono presenti nuovi flag che rappresentano queste funzionalità di trama.

Vedere l'impostazione booleana nei [**\_ dati della funzionalità d3d11 \_ \_ d3d11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Caching dello shader

I driver possono supportare la memorizzazione nella cache shader gestita dal sistema operativo per le applicazioni Direct3D11 in Windows 10 Creators Update.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 