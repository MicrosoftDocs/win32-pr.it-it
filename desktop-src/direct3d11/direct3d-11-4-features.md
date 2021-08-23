---
title: Funzionalità di Direct3D 11.4
description: In Direct3D 11.4 è stata aggiunta la funzionalità seguente.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57190dbd244a565d579e807f7b7b2322ebfec0216d8a6862c4772c4cd4ebe142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124536"
---
# <a name="direct3d-114-features"></a>Funzionalità di Direct3D 11.4

In Direct3D 11.4 è stata aggiunta la funzionalità seguente.

Vedere anche [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Rimozione di dispositivi Direct3D

I metodi [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)e [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) sono supportati da una nuova interfaccia, [**ID3D11Device4,**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)per supportare la ricezione di una notifica di evento asincrona quando un dispositivo Direct3D è stato rimosso.

## <a name="multithreaded-protection"></a>Protezione multithreading

Per garantire che i comandi grafici in particolare vengono eseguiti in un ordine specifico, l'interfaccia [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) include metodi per attivare e disattivare la protezione multithread e metodi per immettere e lasciare codice critico che richiede questa protezione.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Recinti per la sincronizzazione e l'interoperabilità tra più dispositivi con Direct3D 12

[**ID3D11Fence,**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence) [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) e [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) forniscono la stessa funzionalità di decisto di Direct3D 12 per Direct3D 11. I recinti vengono usati per sincronizzare più dispositivi Direct3D11 e per l'interoperabilità tra Direct3D 11 e Direct3D 12. I recinti sono supportati nella Windows 10 Creators Update.

## <a name="extended-nv12-texture-support"></a>Supporto esteso delle trame NV12

Le trame NV12 con funzionalità di acquisizione e codifica video ora supportano la condivisione. I flag di trama D3D11 meno recenti per la codifica e l'acquisizione di video sono deprecati per NV12, perché verranno impostati sempre per i nuovi driver. Tali trame possono essere condivise non solo con D3D11, ma anche con D3D12. In D3D12, nessun nuovo flag rappresenta queste funzionalità di trama.

Vedere l'impostazione booleana in [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Shader Caching

I driver possono supportare la memorizzazione nella cache dello shader gestita dal sistema operativo delle applicazioni Direct3D11 nell'aggiornamento Windows 10 Creators.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 