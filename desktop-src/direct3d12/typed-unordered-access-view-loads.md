---
title: Caricamento della visualizzazione di accesso non ordinato (UAV) tipi
description: Informazioni sul carico Unordered Access View (UAV) in Direct3D 12. Il caricamento tipidato UAV consente a uno shader di leggere da un UAV con un DXGI_FORMAT.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394766"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Caricamento della visualizzazione di accesso non ordinato (UAV) tipi

Unordered Access View (UAV) Typed Load è la possibilità per uno shader di leggere da un UAV con un formato [**DXGI \_ specifico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   [Panoramica](#overview)
-   [Formati supportati e chiamate API](#supported-formats-and-api-calls)
-   [Uso dei caricamenti UAV tipiati da HLSL](#using-typed-uav-loads-from-hlsl)
-   [Uso dei caricamenti UAV tipiati UNORM e SNORM da HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Una visualizzazione di accesso non ordinato (UAV) è una visualizzazione di una risorsa di accesso non ordinata (che può includere buffer, trame e matrici di trame, anche se senza campionamento multiplo). Un UAV consente l'accesso in lettura/scrittura non ordinato a livello temporale da più thread. Questo significa che questo tipo di risorsa può essere letto/scritto contemporaneamente da più thread senza generare conflitti di memoria. Questo accesso simultaneo viene gestito tramite l'uso di [Funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (e D3D11.3) si espande nell'elenco dei formati che possono essere usati con carichi UAV tipici.

## <a name="supported-formats-and-api-calls"></a>Formati supportati e chiamate API

In precedenza, i tre formati seguenti supportavano i caricamenti UAV tipiati ed erano necessari per l'hardware D3D11.0. Sono supportati per tutto l'hardware D3D11.3 e D3D12.

-   R32 \_ FLOAT
-   R32 \_ UINT
-   R32 \_ SINT

I formati seguenti sono supportati come set nell'hardware D3D12 o D3D11.3, quindi se ne è supportato uno qualsiasi, sono supportati tutti.

-   R32G32B32A32 \_ FLOAT
-   R32G32B32A32 \_ UINT
-   R32G32B32A32 \_ SINT
-   R16G16B16A16 \_ FLOAT
-   R16G16B16A16 \_ UINT
-   R16G16B16A16 \_ SINT
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ UINT
-   R8G8B8A8 \_ SINT
-   R16 \_ FLOAT
-   R16 \_ UINT
-   R16 \_ SINT
-   R8 \_ UNORM
-   R8 \_ UINT
-   R8 \_ SINT

I formati seguenti sono supportati facoltativamente e singolarmente nell'hardware D3D12 e D3D11.3, quindi per testare il supporto è necessario eseguire una singola query su ogni formato.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ FLOAT
-   R32G32 \_ UINT
-   R32G32 \_ SINT
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ UINT
-   R11G11B10 \_ FLOAT
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ FLOAT
-   R16G16 \_ UNORM
-   R16G16 \_ UINT
-   R16G16 \_ SNORM
-   R16G16 \_ SINT
-   R8G8 \_ UNORM
-   R8G8 \_ UINT
-   R8G8 \_ SNORM
-   R8G8 \_ SINT
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Per determinare il supporto per eventuali formati aggiuntivi, chiamare [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la struttura [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) come primo parametro (vedere [Capability Querying](capability-querying.md)). Il *campo TypedUAVLoadAdditionalFormats* verrà impostato se è supportato l'elenco "supportato come set" precedente. Eseguire una seconda chiamata a **CheckFeatureSupport** usando una struttura [**D3D12 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (verificando la struttura restituita rispetto al membro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD dell'enumerazione \_ \_ \_ \_ \_ [**D3D12 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) per determinare il supporto nell'elenco dei formati supportati elencati in precedenza, ad esempio:

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

## <a name="using-typed-uav-loads-from-hlsl"></a>Uso dei caricamenti UAV tipiati da HLSL

Per le UAV tipive, il flag HLSL è D3D SHADER REQUIRES TYPED UAV LOAD ADDITIONAL FORMATS (RICHIEDE FORMATI AGGIUNTIVI DI CARICAMENTO \_ \_ \_ \_ UAV \_ \_ \_ TIPISTI).

Di seguito è riportato un esempio di codice shader per elaborare un carico UAV tipiato:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Uso dei caricamenti UAV tipiati UNORM e SNORM da HLSL

Quando si usano caricamenti UAV tipiati per la lettura da una risorsa UNORM o SNORM, è necessario dichiarare correttamente il tipo di elemento dell'oggetto HLSL come `unorm` o `snorm` . Viene specificato come comportamento non definito per non trovare la corrispondenza tra il tipo di elemento dichiarato in HLSL e il tipo di dati della risorsa sottostante. Ad esempio, se si usa il caricamento UAV tipiato in una risorsa buffer con dati R8 UNORM, è necessario dichiarare il tipo di elemento \_ come `unorm float` :

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

[Modello shader 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 