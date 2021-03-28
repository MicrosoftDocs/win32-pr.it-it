---
title: Caricamenti Unordered Access View tipizzati
description: Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0958b3563ab8001fd7b34ae62c9bcc37ad75c07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337902"
---
# <a name="typed-unordered-access-view-loads"></a>Caricamenti Unordered Access View tipizzati

Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .

-   [Overview](#overview)
-   [Formati supportati e chiamate API](#supported-formats-and-api-calls)
-   [Uso dei caricamenti UAV tipizzati da HLSL](#using-typed-uav-loads-from-hlsl)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Una visualizzazione di accesso non ordinato (UAV) è una vista di una risorsa di accesso non ordinato (che può includere buffer, trame e matrici di trama, sebbene senza campionamento multiplo). Un UAV consente un accesso in lettura/scrittura temporaneamente non ordinato da più thread. Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria. Questo accesso simultaneo viene gestito tramite l'utilizzo di [funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 e D3D 11.3 si espande nell'elenco dei formati che possono essere usati con i caricamenti UAV tipizzati.

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
-   8G8 \_ Sint
-   \_UNORM R16
-   R16 \_ russare
-   R8 \_ russamento
-   \_UNORM a8
-   \_UNORM B5G6R5
-   \_UNORM B5G5R5A1
-   \_UNORM B4G4R4A4

Per determinare il supporto per qualsiasi formato aggiuntivo, chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con i [**\_ dati della funzionalità d3d11 d3d11 struttura \_ \_ \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) come primo parametro. Il `TypedUAVLoadAdditionalFormats` bit verrà impostato se è supportato l'elenco "supportato come set". Eseguire una seconda chiamata a **CheckFeatureSupport**, usando una [**struttura \_ \_ SUPPORT2 del \_ formato \_ dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (controllando la struttura restituita rispetto al formato D3D12 \_ SUPPORT2 il \_ \_ \_ membro di caricamento tipizzato UAV \_ del [**\_ formato \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) d3d11 enum) per determinare il supporto nell'elenco di formati eventualmente supportati, ad esempio:

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 