---
title: Carichi UAV (unordered Access View) tipizzati
description: Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548818"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Carichi UAV (unordered Access View) tipizzati

Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)specifico.

-   [Overview](#overview)
-   [Formati supportati e chiamate API](#supported-formats-and-api-calls)
-   [Uso dei caricamenti UAV tipizzati da HLSL](#using-typed-uav-loads-from-hlsl)
-   [Uso di UNORM e di un UAV tipizzato da HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Una visualizzazione di accesso non ordinato (UAV) è una vista di una risorsa di accesso non ordinato (che può includere buffer, trame e matrici di trama, sebbene senza campionamento multiplo). Un UAV consente un accesso in lettura/scrittura temporaneamente non ordinato da più thread. Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria. Questo accesso simultaneo viene gestito tramite l'utilizzo di [funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (e D3D 11.3) si espande nell'elenco dei formati che possono essere usati con i caricamenti UAV tipizzati.

## <a name="supported-formats-and-api-calls"></a>Formati supportati e chiamate API

In precedenza, i tre formati seguenti supportano i caricamenti UAV tipizzati e sono necessari per l'hardware D3D 11.0. Sono supportati per tutti i componenti hardware di D3D 11.3 e D3D12.

-   \_Float R32
-   R32 \_ uint
-   R32 \_ Sint

I formati seguenti sono supportati come set nell'hardware D3D12 o D3D 11.3, quindi se ne è supportato uno tutti sono supportati.

-   \_Float R32G32B32A32
-   R32G32B32A32 \_ uint
-   R32G32B32A32 \_ Sint
-   \_Float R16G16B16A16
-   R16G16B16A16 \_ uint
-   R16G16B16A16 \_ Sint
-   \_UNORM R8G8B8A8
-   R8G8B8A8 \_ uint
-   R8G8B8A8 \_ Sint
-   \_Float R16
-   R16 \_ uint
-   R16 \_ Sint
-   R8 \_ UNORM
-   R8 \_ uint
-   R8 \_ Sint

I formati seguenti sono facoltativamente supportati individualmente nell'hardware D3D12 e D3D 11.3, quindi è necessario eseguire una singola query su ogni formato per verificare il supporto.

-   \_UNORM R16G16B16A16
-   R16G16B16A16 \_ russare
-   \_Float R32G32
-   R32G32 \_ uint
-   R32G32 \_ Sint
-   \_UNORM R10G10B10A2
-   R10G10B10A2 \_ uint
-   \_Float R11G11B10
-   R8G8B8A8 \_ russare
-   \_Float R16G16
-   \_UNORM R16G16
-   R16G16 \_ uint
-   R16G16 \_ russare
-   R16G16 \_ Sint
-   \_UNORM R8G8
-   R8G8 \_ uint
-   R8G8 \_ russare
-   R8G8 \_ Sint
-   \_UNORM R16
-   R16 \_ russare
-   R8 \_ russamento
-   \_UNORM a8
-   \_UNORM B5G6R5
-   \_UNORM B5G5R5A1
-   \_UNORM B4G4R4A4

Per determinare il supporto per qualsiasi formato aggiuntivo, chiamare [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la struttura di [**\_ \_ \_ \_ Opzioni D3D12 dei dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) come primo parametro (vedere l'articolo relativo all' [esecuzione di query sulle funzionalità](capability-querying.md)). Il campo *TypedUAVLoadAdditionalFormats* verrà impostato se è supportato l'elenco "supportato come set". Eseguire una seconda chiamata a **CheckFeatureSupport**, usando una struttura di [**\_ \_ \_ \_ supporto del formato dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (controllando la struttura restituita rispetto al \_ formato D3D12 SUPPORT2 il \_ \_ \_ \_ membro di caricamento tipizzato UAV del [**\_ formato \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) per determinare il supporto nell'elenco dei formati eventualmente supportati sopra indicati, ad esempio:

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Uso dei caricamenti UAV tipizzati da HLSL

Per i UAV tipizzati, il flag HLSL è D3D \_ shader \_ richiede un \_ UAV tipizzato per \_ \_ caricare \_ \_ formati aggiuntivi.

Di seguito è riportato un esempio di codice shader per elaborare un carico di UAV tipizzato:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Uso di UNORM e di un UAV tipizzato da HLSL

Quando si usano i caricamenti UAV tipizzati per leggere da una risorsa UNORM o RUSSAr, è necessario dichiarare correttamente il tipo di elemento dell'oggetto HLSL come `unorm` o `snorm` . Viene specificato come comportamento non definito in modo che non corrisponda al tipo di elemento dichiarato in HLSL con il tipo di dati della risorsa sottostante. Ad esempio, se si usano i caricamenti UAV tipizzati in una risorsa di buffer con \_ i dati di R8 UNORM, è necessario dichiarare il tipo di elemento come `unorm float` :

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering](rendering.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 