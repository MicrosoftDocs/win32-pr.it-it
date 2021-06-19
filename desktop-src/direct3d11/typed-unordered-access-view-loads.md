---
title: Carichi Unordered Access View tipi
description: Informazioni sul Unordered Access View (UAV) in Direct3D 11. Il caricamento tipidato UAV consente a uno shader di leggere da un UAV con un DXGI_FORMAT.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396286"
---
# <a name="typed-unordered-access-view-loads"></a>Carichi Unordered Access View tipi

Unordered Access View (UAV) Typed Load è la possibilità per uno shader di leggere da un UAV con un formato DXGI \_ specifico.

-   [Panoramica](#overview)
-   [Formati supportati e chiamate API](#supported-formats-and-api-calls)
-   [Uso dei caricamenti UAV tipiati da HLSL](#using-typed-uav-loads-from-hlsl)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Una visualizzazione di accesso non ordinato (UAV) è una visualizzazione di una risorsa di accesso non ordinata (che può includere buffer, trame e matrici di trame, anche se senza campionamento multiplo). Un UAV consente l'accesso in lettura/scrittura non ordinato a livello temporale da più thread. Questo significa che questo tipo di risorsa può essere letto/scritto contemporaneamente da più thread senza generare conflitti di memoria. Questo accesso simultaneo viene gestito tramite l'uso di [Funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 e D3D11.3 si espandono nell'elenco dei formati che è possibile usare con carichi UAV tipici.

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
-   SINT 8G8 \_
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Per determinare il supporto per eventuali formati aggiuntivi, chiamare [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la struttura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) come primo parametro. Il `TypedUAVLoadAdditionalFormats` bit verrà impostato se è supportato l'elenco "supportato come set" precedente. Eseguire una seconda chiamata a **CheckFeatureSupport** usando una struttura [**D3D11 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (verificando la struttura restituita rispetto al membro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD dell'enumerazione \_ \_ \_ \_ \_ [**D3D11 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) per determinare il supporto nell'elenco dei formati supportati in precedenza, ad esempio:

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11.3](direct3d-11-3-features.md)
</dt> <dt>

[Modello shader 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 