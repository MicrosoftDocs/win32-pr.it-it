---
title: Indicizzazione dinamica con HLSL 5,1
description: L'esempio D3D12DynamicIndexing illustra alcune delle nuove funzionalità di HLSL disponibili nel modello di shader 5,1, in particolare l'indicizzazione dinamica e le matrici non associate, per eseguire il rendering dello stesso mesh più volte, ogni volta che viene eseguito il rendering con un materiale selezionato dinamicamente. Con l'indicizzazione dinamica, è ora possibile indicizzare gli shader in una matrice senza conoscere il valore dell'indice in fase di compilazione. In combinazione con matrici non vincolate, viene aggiunto un altro livello di riferimento indiretto e flessibilità per gli autori dello shader e le pipeline di grafica.
ms.assetid: 9821AEDF-E83D-4034-863A-2B820D9B7455
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e41892e7deff23c8d11f8be1c38dac3fcba1de9
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548823"
---
# <a name="dynamic-indexing-using-hlsl-51"></a>Indicizzazione dinamica con HLSL 5,1

L'esempio **D3D12DynamicIndexing** illustra alcune delle nuove funzionalità di HLSL disponibili nel modello di shader 5,1, in particolare l'indicizzazione dinamica e le matrici non associate, per eseguire il rendering dello stesso mesh più volte, ogni volta che viene eseguito il rendering con un materiale selezionato dinamicamente. Con l'indicizzazione dinamica, è ora possibile indicizzare gli shader in una matrice senza conoscere il valore dell'indice in fase di compilazione. In combinazione con matrici non vincolate, viene aggiunto un altro livello di riferimento indiretto e flessibilità per gli autori dello shader e le pipeline di grafica.

-   [Configurare la pixel shader](#set-up-the-pixel-shader)
-   [Configurare la firma radice](#set-up-the-root-signature)
-   [Creare le trame](#create-the-textures)
-   [Caricare i dati di trama](#upload-the-texture-data)
-   [Caricare la trama diffusa](#load-the-diffuse-texture)
-   [Creare un campionatore](#create-a-sampler)
-   [Modificare dinamicamente l'indice del parametro radice](#dynamically-change-the-root-parameter-index)
-   [Eseguire l'esempio](#run-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="set-up-the-pixel-shader"></a>Configurare la pixel shader

Esaminiamo prima di tutto lo shader, che per questo esempio è un pixel shader.

``` syntax
Texture2D        g_txDiffuse : register(t0);
Texture2D        g_txMats[]  : register(t1);
SamplerState     g_sampler   : register(s0);

struct PSSceneIn
{
    float4 pos : SV_Position;
    float2 tex : TEXCOORD0;
};

struct MaterialConstants
{
    uint matIndex;  // Dynamically set index for looking up from g_txMats[].
};
ConstantBuffer<MaterialConstants> materialConstants : register(b0, space0);

float4 PSSceneMain(PSSceneIn input) : SV_Target
{
    float3 diffuse = g_txDiffuse.Sample(g_sampler, input.tex).rgb;
    float3 mat = g_txMats[materialConstants.matIndex].Sample(g_sampler, input.tex).rgb;
    return float4(diffuse * mat, 1.0f);
}
```

La funzione di matrice non associata è illustrata dalla `g_txMats[]` matrice perché non specifica una dimensione della matrice. L'indicizzazione dinamica viene utilizzata per eseguire l'indicizzazione in `g_txMats[]` `matIndex` , che è definita come costante radice. Lo shader non è a conoscenza della dimensione o della matrice o del valore dell'indice in fase di compilazione. Entrambi gli attributi sono definiti nella firma radice dell'oggetto di stato della pipeline usato con lo shader.

Per sfruttare i vantaggi delle funzionalità di indicizzazione dinamica in HLSL, è necessario che lo shader venga compilato con SM 5,1. Inoltre, per utilizzare le matrici non vincolate, è necessario utilizzare anche il flag **/enable \_ unbounded \_ descrittor \_ Tables** . Le seguenti opzioni della riga di comando vengono usate per compilare questo shader con lo [strumento di compilazione degli effetti](/windows/desktop/direct3dtools/fxc) (FXC):

``` syntax
fxc /Zi /E"PSSceneMain" /Od /Fo"dynamic_indexing_pixel.cso" /ps"_5_1" /nologo /enable_unbounded_descriptor_tables
```

## <a name="set-up-the-root-signature"></a>Configurare la firma radice

Verrà ora esaminata la definizione della firma radice, in particolare il modo in cui si definiscono le dimensioni della matrice senza limiti e si collega una costante radice a `matIndex` . Per l'pixel shader, vengono definiti tre elementi: una tabella dei descrittori per SRVs (Texture2Ds), una tabella dei descrittori per i sampler e una singola costante radice. La tabella descrittore per il SRVs contiene `CityMaterialCount + 1` voci. `CityMaterialCount` costante che definisce la lunghezza di `g_txMats[]` e + 1 è per `g_txDiffuse` . La tabella descrittore per i sampler contiene solo una voce e viene definito solo il valore della costante radice a 1 32 bit tramite **InitAsConstants**(...)., nel metodo **LoadAssets** .

``` syntax
 // Create the root signature.
    {
        CD3DX12_DESCRIPTOR_RANGE ranges[3];
        ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1 + CityMaterialCount, 0);  // Diffuse texture + array of materials.
        ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, 1, 0);
        ranges[2].Init(D3D12_DESCRIPTOR_RANGE_TYPE_CBV, 1, 0);

        CD3DX12_ROOT_PARAMETER rootParameters[4];
        rootParameters[0].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[1].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[2].InitAsDescriptorTable(1, &ranges[2], D3D12_SHADER_VISIBILITY_VERTEX);
        rootParameters[3].InitAsConstants(1, 0, 0, D3D12_SHADER_VISIBILITY_PIXEL);

        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }
```



| Flusso di chiamate                                                             | Parametri                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_Intervallo descrittore CD3DX12 \_**](cd3dx12-descriptor-range.md)        | [**\_Tipo di \_ intervallo descrittore D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**\_Parametro radice \_ CD3DX12**](cd3dx12-root-parameter.md)            | [**\_Visibilità shader D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**\_Descrizione della \_ firma \_ radice CD3DX12**](cd3dx12-root-signature-desc.md) | [**\_Flag di \_ firma \_ radice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_Versione della \_ firma \_ radice D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-textures"></a>Creare le trame

Il contenuto di `g_txMats[]` è costituito da trame generate in una procedura creata in **LoadAssets**. Ogni città di cui viene eseguito il rendering nella scena condivide la stessa trama diffusa, ma ognuna presenta anche una propria trama generata in base a procedura. La matrice di trame spazia dallo spettro arcobaleno per visualizzare facilmente la tecnica di indicizzazione.

``` syntax
 // Create the textures and sampler.
    {
        // Procedurally generate an array of textures to use as city materials.
        {
            // All of these materials use the same texture desc.
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = 1;
            textureDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            textureDesc.Width = CityMaterialTextureWidth;
            textureDesc.Height = CityMaterialTextureHeight;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            // The textures evenly span the color rainbow so that each city gets
            // a different material.
            float materialGradStep = (1.0f / static_cast<float>(CityMaterialCount));

            // Generate texture data.
            vector<vector<unsigned char>> cityTextureData;
            cityTextureData.resize(CityMaterialCount);
            for (int i = 0; i < CityMaterialCount; ++i)
            {
                CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &heapProps,
                    D3D12_HEAP_FLAG_NONE,
                    &textureDesc,
                    D3D12_RESOURCE_STATE_COPY_DEST,
                    nullptr,
                    IID_PPV_ARGS(&m_cityMaterialTextures[i])));

                // Fill the texture.
                float t = i * materialGradStep;
                cityTextureData[i].resize(CityMaterialTextureWidth * CityMaterialTextureHeight * CityMaterialTextureChannelCount);
                for (int x = 0; x < CityMaterialTextureWidth; ++x)
                {
                    for (int y = 0; y < CityMaterialTextureHeight; ++y)
                    {
                        // Compute the appropriate index into the buffer based on the x/y coordinates.
                        int pixelIndex = (y * CityMaterialTextureChannelCount * CityMaterialTextureWidth) + (x * CityMaterialTextureChannelCount);

                        // Determine this row's position along the rainbow gradient.
                        float tPrime = t + ((static_cast<float>(y) / static_cast<float>(CityMaterialTextureHeight)) * materialGradStep);

                        // Compute the RGB value for this position along the rainbow
                        // and pack the pixel value.
                        XMVECTOR hsl = XMVectorSet(tPrime, 0.5f, 0.5f, 1.0f);
                        XMVECTOR rgb = XMColorHSLToRGB(hsl);
                        cityTextureData[i][pixelIndex + 0] = static_cast<unsigned char>((255 * XMVectorGetX(rgb)));
                        cityTextureData[i][pixelIndex + 1] = static_cast<unsigned char>((255 * XMVectorGetY(rgb)));
                        cityTextureData[i][pixelIndex + 2] = static_cast<unsigned char>((255 * XMVectorGetZ(rgb)));
                        cityTextureData[i][pixelIndex + 3] = 255;
                    }
                }
            }
        }
```



<table>
<thead>
<tr class="header">
<th>Flusso di chiamate</th>
<th>Parametri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a><br />
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_dimension)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)<br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></td>
<td><dl><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a><br />
<a href=""></a>[<strong>XMColorHSLToRGB</strong>] (/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="upload-the-texture-data"></a>Caricare i dati di trama

I dati della trama vengono caricati nella GPU tramite un heap di caricamento e vengono creati SRVs per ogni e archiviati in un heap del descrittore SRV.

``` syntax
         // Upload texture data to the default heap resources.
            {
                const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
                const UINT64 uploadBufferStep = GetRequiredIntermediateSize(m_cityMaterialTextures[0].Get(), 0, subresourceCount); // All of our textures are the same size in this case.
                const UINT64 uploadBufferSize = uploadBufferStep * CityMaterialCount;
                CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
                auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &uploadHeap,
                    D3D12_HEAP_FLAG_NONE,
                    &uploadDesc,
                    D3D12_RESOURCE_STATE_GENERIC_READ,
                    nullptr,
                    IID_PPV_ARGS(&materialsUploadHeap)));

                for (int i = 0; i < CityMaterialCount; ++i)
                {
                    // Copy data to the intermediate upload heap and then schedule 
                    // a copy from the upload heap to the appropriate texture.
                    D3D12_SUBRESOURCE_DATA textureData = {};
                    textureData.pData = &cityTextureData[i][0];
                    textureData.RowPitch = static_cast<LONG_PTR>((CityMaterialTextureChannelCount * textureDesc.Width));
                    textureData.SlicePitch = textureData.RowPitch * textureDesc.Height;

                    UpdateSubresources(m_commandList.Get(), m_cityMaterialTextures[i].Get(), materialsUploadHeap.Get(), i * uploadBufferStep, 0, subresourceCount, &textureData);
                    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityMaterialTextures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
                    m_commandList->ResourceBarrier(1, &barrier);
                }
            }
```



<table>
<thead>
<tr class="header">
<th>Flusso di chiamate</th>
<th>Parametri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></td>

</tr>
<tr class="even">
<td><a href="updatesubresources1.md"><strong>Updatesubresources con</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="load-the-diffuse-texture"></a>Caricare la trama diffusa

La trama diffusa, g \_ `txDiffuse` , viene caricata in modo analogo e ottiene anche il proprio SRV, ma i dati della trama sono già definiti in occcity. bin.

``` syntax
// Load the occcity diffuse texture with baked-in ambient lighting.
        // This texture will be blended with a texture from the materials
        // array in the pixel shader.
        {
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = SampleAssets::Textures[0].MipLevels;
            textureDesc.Format = SampleAssets::Textures[0].Format;
            textureDesc.Width = SampleAssets::Textures[0].Width;
            textureDesc.Height = SampleAssets::Textures[0].Height;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &heapProps,
                D3D12_HEAP_FLAG_NONE,
                &textureDesc,
                D3D12_RESOURCE_STATE_COPY_DEST,
                nullptr,
                IID_PPV_ARGS(&m_cityDiffuseTexture)));

            const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
            const UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_cityDiffuseTexture.Get(), 0, subresourceCount);
            CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
            auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &uploadHeap,
                D3D12_HEAP_FLAG_NONE,
                &uploadDesc,
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&textureUploadHeap)));

            // Copy data to the intermediate upload heap and then schedule 
            // a copy from the upload heap to the diffuse texture.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pMeshData + SampleAssets::Textures[0].Data[0].Offset;
            textureData.RowPitch = SampleAssets::Textures[0].Data[0].Pitch;
            textureData.SlicePitch = SampleAssets::Textures[0].Data[0].Size;

            UpdateSubresources(m_commandList.Get(), m_cityDiffuseTexture.Get(), textureUploadHeap.Get(), 0, 0, subresourceCount, &textureData);
            auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityDiffuseTexture.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
            m_commandList->ResourceBarrier(1, &barrier);
        }
```



<table>
<thead>
<tr class="header">
<th>Flusso di chiamate</th>
<th>Parametri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="create-a-sampler"></a>Creare un campionatore

Infine, per **LoadAssets** viene creato un singolo campionatore da campionare dalla trama diffusa o dalla matrice di trame.

``` syntax
 // Describe and create a sampler.
        D3D12_SAMPLER_DESC samplerDesc = {};
        samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
        samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.MinLOD = 0;
        samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
        samplerDesc.MipLODBias = 0.0f;
        samplerDesc.MaxAnisotropy = 1;
        samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
        m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());

        // Create SRV for the city's diffuse texture.
        CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle(m_cbvSrvHeap->GetCPUDescriptorHandleForHeapStart(), 0, m_cbvSrvDescriptorSize);
        D3D12_SHADER_RESOURCE_VIEW_DESC diffuseSrvDesc = {};
        diffuseSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        diffuseSrvDesc.Format = SampleAssets::Textures->Format;
        diffuseSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        diffuseSrvDesc.Texture2D.MipLevels = 1;
        m_device->CreateShaderResourceView(m_cityDiffuseTexture.Get(), &diffuseSrvDesc, srvHandle);
        srvHandle.Offset(m_cbvSrvDescriptorSize);

        // Create SRVs for each city material.
        for (int i = 0; i < CityMaterialCount; ++i)
        {
            D3D12_SHADER_RESOURCE_VIEW_DESC materialSrvDesc = {};
            materialSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
            materialSrvDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            materialSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
            materialSrvDesc.Texture2D.MipLevels = 1;
            m_device->CreateShaderResourceView(m_cityMaterialTextures[i].Get(), &materialSrvDesc, srvHandle);

            srvHandle.Offset(m_cbvSrvDescriptorSize);
        }   
```



<table>
<thead>
<tr class="header">
<th>Flusso di chiamate</th>
<th>Parametri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode"></a><br />
D3D12_FLOAT32_MAX (<a href="constants.md"><strong>costanti</strong></a>)<br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></td>

</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="dynamically-change-the-root-parameter-index"></a>Modificare dinamicamente l'indice del parametro radice

Se dovessimo ora eseguire il rendering della scena, tutte le città verrebbero visualizzate nello stesso modo, perché il valore della nostra costante radice non è stato impostato `matIndex` . Ogni pixel shader indicizzato nello slot 0A di `g_txMats` e la scena avrà un aspetto simile al seguente:

![tutte le città presentano lo stesso colore](images/dynamicindexing-image1.png)

Il valore della costante radice è impostato in **FrameResource::P opulatecommandlists**. Nel ciclo Double **for** , in cui viene registrato un comando di traccia per ogni città, viene registrata una chiamata a [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) che specifica l'indice di parametri radice per quanto riguarda la firma radice, in questo caso 3, il valore dell'indice dinamico e un offset, in questo caso 0. Poiché la lunghezza di `g_txMats` è uguale al numero di città di cui viene eseguito il rendering, il valore dell'indice viene impostato in modo incrementale per ogni città.

``` syntax
 for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            pCommandList->SetPipelineState(pPso);

            // Set the city's root constant for dynamically indexing into the material array.
            pCommandList->SetGraphicsRoot32BitConstant(3, (i * m_cityColumnCount) + j, 0);

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
```



| Flusso di chiamate                                                                                          | Parametri |
|----------------------------------------------------------------------------------------------------|------------|
| [**SetPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)                             |            |
| [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)     |            |
| [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) |            |
| [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)                     |            |

## <a name="run-the-sample"></a>Eseguire l'esempio

A questo punto, quando si esegue il rendering della scena, ogni città avrà un valore diverso per `matIndex` e in questo modo verrà cercata una trama diversa perché `g_txMats[]` l'aspetto della scena è simile al seguente:

![tutte le città vengono visualizzate in colori diversi](images/dynamicindexing-image2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure dettagliate per il codice D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Effect-strumento compilatore](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[Funzionalità del modello HLSL shader 5,1 per Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>
