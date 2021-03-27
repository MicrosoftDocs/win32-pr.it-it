---
title: Compute Shaders su hardware di livello inferiore
description: Questo argomento illustra come usare Compute Shaders in un'app Direct3D 11 su hardware Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047570"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Compute Shaders su hardware di livello inferiore

Direct3D 11 consente di usare i [compute shader](direct3d-11-advanced-stages-compute-shader.md) che operano sulla maggior parte dell'hardware Direct3D 10. x, con alcune limitazioni per il funzionamento. La tecnologia compute shader è nota anche come tecnologia DirectCompute. Questo argomento illustra come usare [Compute Shaders](direct3d-11-advanced-stages-compute-shader.md) in un'app Direct3D 11 su hardware Direct3D 10.

Il supporto per Compute Shaders su hardware di livello inferiore è solo per i dispositivi compatibili con Direct3D 10. x. Non è possibile usare Compute Shaders nell'hardware Direct3D 9. x.

Per verificare se l'hardware Direct3D 10. x supporta Compute Shader, chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Nella chiamata a **CheckFeatureSupport** passare il valore d3d11 \_ feature \_ D3D10 \_ x \_ hardware Options al parametro \_ *feature* , passare un puntatore alla struttura [**d3d11 \_ feature \_ \_ D3D10 \_ x \_ hardware \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) al parametro *pFeatureSupportData* e passare le dimensioni della struttura **d3d11 \_ Data features D3D10 x la struttura \_ delle \_ \_ \_ \_ Opzioni hardware** al parametro *FeatureSupportDataSize* . **CheckFeatureSupport** restituisce **true** in **ComputeShaders \_ Plus RawAndStructuredBuffers tramite il membro \_ \_ \_ shader \_ 4 \_ x** di **d3d11 \_ feature \_ data \_ D3D10 \_ x \_ \_ Opzioni hardware** se l'hardware Direct3D 10. x supporta Compute Shader.

Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.

-   [Viste di accesso non ordinate (UAV)](#unordered-access-views-uavs)
-   [Viste risorse shader (SRVs)](#shader-resource-views-srvs)
-   [Gruppi di thread](#thread-groups)
    -   [Dimensioni del gruppo di thread](#thread-group-dimensions)
    -   [Indici di thread bidimensionali](#two-dimensional-thread-indices)
    -   [Memoria condivisa del gruppo di thread (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile con \_ ottimizzazione Skip \_ D3DCompile](/windows)
-   [Argomenti correlati](#related-topics)

## <a name="unordered-access-views-uavs"></a>Viste di accesso non ordinate (UAV)

Le visualizzazioni di accesso non ordinato ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) e strutturate ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) non elaborate sono supportate nell'hardware di livello inferiore, con le limitazioni seguenti:

-   È possibile associare un singolo UAV a una pipeline alla volta tramite [**sul ID3D11DeviceContext:: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   L'offset di base per un UAV non elaborato deve essere allineato su un limite di 256 byte (anziché sull'allineamento a 16 byte necessario per l'hardware Direct3D 11).

I UAV tipizzati non sono supportati nell'hardware di livello inferiore. Sono inclusi [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)e [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAV.

I pixel shader sull'hardware di livello inferiore non supportano l'accesso non ordinato.

## <a name="shader-resource-views-srvs"></a>Viste risorse shader (SRVs)

I buffer non elaborati e strutturati come viste delle risorse dello shader sono supportati nell'hardware di livello inferiore per l'accesso in sola lettura, così come sono nell'hardware Direct3D 11. Questi tipi di risorse sono supportati per vertex shader, geometry shader, pixel shader e compute shader.

## <a name="thread-groups"></a>Gruppi di thread

Un compute shader può essere eseguito su molti thread in parallelo, all'interno di un gruppo di thread.

I gruppi di thread sono supportati nell'hardware di livello inferiore, con le limitazioni seguenti:

### <a name="thread-group-dimensions"></a>Dimensioni del gruppo di thread

I gruppi di thread definiti per l'hardware di livello inferiore sono limitati alle dimensioni X e Y di 768. È inferiore ai valori massimi di 1024 per l'hardware Direct3D 11. La dimensione massima della Z di 64 è invariata.

Il numero totale di thread nel gruppo (X × Y × Z) è limitato a 768. Questo è inferiore al limite di 1024 per l'hardware Direct3D 11.

Se questi numeri vengono superati, la compilazione dello shader avrà esito negativo.

### <a name="two-dimensional-thread-indices"></a>Indici Two-Dimensional thread

Un thread specifico all'interno di un gruppo di thread viene indicizzato usando un vettore 3D fornito da (x, y, z).

Per i compute shader che operano su hardware di livello inferiore, i gruppi di thread supportano solo due dimensioni. Ciò significa che il valore Z nel vettore 3D deve sempre essere 1.

Questa limitazione si applica specificamente a quanto segue:

-   [**Sul ID3D11DeviceContext::D la patch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)-l'argomento *ThreadGroupCountZ* deve essere 1.
-   [**Sul ID3D11DeviceContext::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)-questa funzione non è supportata nell'hardware di livello inferiore.
-   [numThreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads): il valore Z deve essere 1.

### <a name="thread-group-shared-memory-tgsm"></a>Memoria condivisa del gruppo di thread (TGSM)

La memoria condivisa del gruppo di thread è limitata a 16Kb su hardware di livello inferiore. Questo è inferiore a quello di 32 KB disponibile per l'hardware Direct3D 11.

Un thread compute shader può scrivere solo nella propria area di TGSM. Questa area di sola scrittura ha una dimensione massima di 256 byte o meno, con la riduzione massima con l'aumentare del numero di thread dichiarati per il gruppo.

La tabella seguente definisce le dimensioni massime per thread di un'area TGSM per il numero di thread nel gruppo:



| Numero di thread nel gruppo | Dimensioni massime TGSM per thread |
|----------------------------|------------------------------|
| 0-64                       | 256                          |
| 65-68                      | 240                          |
| 69-72                      | 224                          |
| 73-76                      | 208                          |
| 77-84                      | 192                          |
| 85-92                      | 176                          |
| 93-100                     | 160                          |
| 101-112                    | 144                          |
| 113-128                    | 128                          |
| 129-144                    | 112                          |
| 145-168                    | 96                           |
| 169-204                    | 80                           |
| 205-256                    | 64                           |
| 257-340                    | 48                           |
| 341-512                    | 32                           |
| 513-768                    | 16                           |



 

Un thread compute shader può leggere il TGSM da qualsiasi percorso.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile con \_ ottimizzazione Skip \_ D3DCompile

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) restituisce **E \_ NOTIMPL** quando si passa cs \_ 4 \_ 0 come destinazione dello shader insieme all'opzione di compilazione [**D3DCompile \_ Skip \_ Optimization**](/windows/desktop/direct3dhlsl/d3dcompile-constants) . La \_ destinazione dello shader CS 5 \_ 0 funziona con **l' \_ \_ ottimizzazione di D3DCOMPILE Skip**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 