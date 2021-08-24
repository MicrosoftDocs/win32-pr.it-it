---
title: Shader di calcolo nell'hardware di livello inferiore
description: Questo argomento illustra come usare gli shader di calcolo in un'app Direct3D 11 nell'hardware Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673397d6974d2191acc1f5e30ccf8cae8b5b5f4b0ab5cae305360fef3e7186f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894471"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Shader di calcolo nell'hardware di livello inferiore

Direct3D 11 offre la possibilità di usare [shader](direct3d-11-advanced-stages-compute-shader.md) di calcolo che operano sulla maggior parte dell'hardware Direct3D 10.x, con alcune limitazioni al funzionamento. La tecnologia compute shader è nota anche come tecnologia DirectCompute. Questo argomento illustra come usare gli shader di [calcolo](direct3d-11-advanced-stages-compute-shader.md) in un'app Direct3D 11 nell'hardware Direct3D 10.

Il supporto per gli shader di calcolo nell'hardware di livello inferiore è solo per i dispositivi compatibili con Direct3D 10.x. Gli shader di calcolo non possono essere usati nell'hardware Direct3D 9.x.

Per verificare se l'hardware Direct3D 10.x supporta gli shader di calcolo, chiamare [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Nella chiamata **CheckFeatureSupport** passare il valore D3D11 FEATURE D3D10 X HARDWARE OPTIONS al parametro Feature, passare un puntatore alla struttura \_ \_ \_ \_ \_ [**\_ D3D11 FEATURE \_ DATA \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) al parametro *pFeatureSupportData* e passare le dimensioni della struttura **D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS** al parametro *FeatureSupportDataSize.*  **CheckFeatureSupport** restituisce **TRUE** in **ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via Shader \_ \_ 4 \_ x** membro di **D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS** se l'hardware Direct3D 10.x supporta gli shader di calcolo.

La [sezione 10Level9 Reference](d3d11-graphics-reference-10level9.md) elenca le differenze tra il comportamento dei vari metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a vari livelli di funzionalità 10Level9.

-   [Viste di accesso non ordinate (UAV)](#unordered-access-views-uavs)
-   [Visualizzazioni delle risorse shader (SPV)](#shader-resource-views-srvs)
-   [Gruppi di thread](#thread-groups)
    -   [Dimensioni del gruppo di thread](#thread-group-dimensions)
    -   [Indici di thread bidimensionali](#two-dimensional-thread-indices)
    -   [Memoria condivisa del gruppo di thread (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile con D3DCOMPILE \_ SKIP \_ OPTIMIZATION](/windows)
-   [Argomenti correlati](#related-topics)

## <a name="unordered-access-views-uavs"></a>Viste di accesso non ordinate (UAV)

Le viste di accesso non ordinate raw ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) e Structured ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) sono supportate nell'hardware di livello inferiore, con le limitazioni seguenti:

-   Solo un singolo UAV può essere associato a una pipeline alla volta tramite [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   L'offset di base per un UAV non elaborato deve essere allineato su un limite di 256 byte (anziché sull'allineamento a 16 byte necessario per l'hardware Direct3D 11).

Le UAV tipiche non sono supportate nell'hardware di livello inferiore. Sono inclusi [gli UAV Texture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)e [Texture3D.](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

I pixel shader nell'hardware di livello inferiore non supportano l'accesso non ordinato.

## <a name="shader-resource-views-srvs"></a>Visualizzazioni delle risorse shader (SPV)

I buffer non elaborati e strutturati come visualizzazioni delle risorse shader sono supportati nell'hardware di livello inferiore per l'accesso in sola lettura, come nell'hardware Direct3D 11. Questi tipi di risorse sono supportati per Vertex Shader, Geometry Shader, Pixel Shader e Compute Shader.

## <a name="thread-groups"></a>Gruppi di thread

Un compute shader può essere eseguito su molti thread in parallelo, all'interno di un gruppo di thread.

I gruppi di thread sono supportati nell'hardware di livello inferiore, con le limitazioni seguenti:

### <a name="thread-group-dimensions"></a>Dimensioni del gruppo di thread

I gruppi di thread definiti per l'hardware di livello inferiore sono limitati alle dimensioni X e Y di 768. È minore dei valori massimi di 1024 per l'hardware Direct3D 11. La dimensione Z massima di 64 rimane invariata.

Il numero totale di thread nel gruppo (X × Y × Z) è limitato a 768. Si tratta di un valore inferiore al limite di 1024 per l'hardware Direct3D 11.

Se questi numeri vengono superati, la compilazione dello shader avrà esito negativo.

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional di thread

Un thread specifico all'interno di un gruppo di thread viene indicizzato usando un vettore 3D specificato da (x,y,z).

Per gli shader di calcolo che operano su hardware di livello inferiore, i gruppi di thread supportano solo due dimensioni. Ciò significa che il valore Z nel vettore 3D deve essere sempre 1.

Questa limitazione si applica in modo specifico agli elementi seguenti:

-   [**ID3D11DeviceContext::D ispatch:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) *l'argomento ThreadGroupCountZ* deve essere 1.
-   [**ID3D11DeviceContext::D ispatchIndirect:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)questa funzione non è supportata nell'hardware di livello inferiore.
-   [numthreads:](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)il valore Z deve essere 1.

### <a name="thread-group-shared-memory-tgsm"></a>Memoria condivisa del gruppo di thread (TGSM)

La memoria condivisa del gruppo di thread è limitata a 16 KB nell'hardware di livello inferiore. Si tratta di un valore inferiore a 32 KB disponibile per l'hardware Direct3D 11.

Un thread Compute Shader può scrivere solo nella propria area di TGSM. Questa area di sola scrittura ha dimensioni massime di 256 byte, con il numero massimo di thread dichiarati per il gruppo in aumento.

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



 

Un thread Compute Shader può leggere il TGSM da qualsiasi posizione.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile con D3DCOMPILE \_ SKIP \_ OPTIMIZATION

[**D3DCompile restituisce**](/windows/desktop/direct3dhlsl/d3dcompile) **E \_ NOTIMPL** quando si passa cs 4 0 come destinazione shader insieme all'opzione di compilazione \_ \_ [**D3DCOMPILE \_ SKIP \_ OPTIMIZATION.**](/windows/desktop/direct3dhlsl/d3dcompile-constants) La destinazione dello shader cs \_ 5 \_ 0 funziona con **D3DCOMPILE \_ SKIP \_ OPTIMIZATION**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D 11 in hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 