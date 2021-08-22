---
title: Panoramica dello shader di calcolo
description: Uno shader di calcolo è una fase shader programmabile che espande Microsoft Direct3D 11 oltre la programmazione grafica. La tecnologia compute shader è nota anche come tecnologia DirectCompute.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6167915a670b6dfb4fffae957ee0121e8e52f639463b0d1132be9dac3552fe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566341"
---
# <a name="compute-shader-overview"></a>Panoramica dello shader di calcolo

Uno shader di calcolo è una fase shader programmabile che espande Microsoft Direct3D 11 oltre la programmazione grafica. La tecnologia compute shader è nota anche come tecnologia DirectCompute.

Come per altri shader programmabili (ad esempio vertex shader e geometry shader), un compute shader è progettato e implementato con [HLSL,](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) ma questo è solo il punto in cui termina la somiglianza. Uno shader di calcolo fornisce un calcolo generico ad alta velocità e sfrutta l'elevato numero di processori paralleli nell'unità di elaborazione grafica (GPU). Lo shader di calcolo fornisce funzionalità di condivisione della memoria e sincronizzazione dei thread per consentire metodi di programmazione paralleli più efficaci. Chiamare il metodo [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) o [**ID3D11DeviceContext::D ispatchIndirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) per eseguire comandi in uno shader di calcolo. Uno shader di calcolo può essere eseguito su molti thread in parallelo.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Uso dello shader di calcolo nell'hardware Direct3D 10.x

Uno shader di calcolo in Microsoft Direct3D 10 è noto anche come DirectCompute 4.x.

Se si usano l'API Direct3D 11 e i driver [aggiornati,](overviews-direct3d-11-devices-downlevel-intro.md) l'hardware Direct3D livello di funzionalità 10 e 10.1 può facoltativamente supportare una forma limitata di DirectCompute che usa i profili cs \_ 4 0 e cs \_ \_ \_ 4 1. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Quando si usa DirectCompute in questo hardware, tenere presenti le limitazioni seguenti:

-   Il numero massimo di thread è limitato a D3D11 \_ CS \_ 4 \_ X THREAD GROUP MAX THREADS PER GROUP \_ \_ \_ \_ \_ \_ (768) per gruppo.
-   La dimensione X e Y dei **numthread è** limitata a D3D11 \_ CS \_ 4 X THREAD GROUP \_ MAX X \_ \_ \_ \_ (768) e D3D11 \_ CS \_ 4 X THREAD GROUP \_ MAX Y \_ \_ \_ \_ (768).
-   La dimensione Z di **numthreads** è limitata a 1.
-   La dimensione Z di dispatch è limitata a D3D11 \_ CS \_ 4 \_ X \_ DISPATCH MAX THREAD GROUPS \_ IN Z DIMENSION \_ \_ \_ \_ \_ (1).
-   Allo shader può essere associata una sola vista di accesso non ordinato (D3D11 \_ CS \_ 4 \_ X \_ UAV REGISTER COUNT è \_ \_ 1).
-   Solo [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)e [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)sono disponibili come viste di accesso non ordinato.
-   Un thread può accedere solo alla propria area in gruppi memoryhared per la scrittura, anche se può leggere da qualsiasi posizione.
-   [SV \_ È necessario usare GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) [o SV \_ GroupThreadID](/windows/desktop/direct3dhlsl/sv-groupthreadid) quando si accede ai gruppi **la memoria** condivisa per la scrittura.
-   **La memoria condivisa dei** gruppi è limitata a 16 KB per gruppo.
-   Un singolo thread è limitato a un'area di 256 byte di **gruppi di** memoria condivisa per la scrittura.
-   Non sono disponibili istruzioni atomiche.
-   Non sono disponibili valori a precisione doppia.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Uso dello shader di calcolo nell'hardware Direct3D 11.x

Uno shader di calcolo in Direct3D 11 è noto anche come DirectCompute 5.0.

Quando si usa DirectCompute con i profili cs \_ \_ 5 0, [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)tenere presenti gli elementi seguenti:

-   Il numero massimo di thread è limitato a D3D11 \_ CS THREAD GROUP MAX THREADS PER GROUP \_ \_ \_ \_ \_ \_ (1024) per gruppo.
-   La dimensione X e Y di **numthreads** è limitata a D3D11 \_ CS THREAD GROUP MAX X \_ \_ \_ \_ (1024) e D3D11 \_ CS THREAD GROUP MAX Y \_ \_ \_ \_ (1024).
-   La dimensione Z di **numthreads** è limitata a D3D11 \_ CS THREAD GROUP MAX Z \_ \_ \_ \_ (64).
-   La dimensione massima di dispatch è limitata a D3D11 \_ CS \_ DISPATCH \_ MAX THREAD GROUPS PER DIMENSION \_ \_ \_ \_ (65535).
-   Il numero massimo di viste di accesso non ordinato che possono essere associate a uno shader è D3D11 \_ PS \_ CS \_ UAV REGISTER COUNT \_ \_ (8).
-   Supporta [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s e viste di accesso non ordinato tipiche ([RWTexture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [RWTexture2D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d) [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)e così via).
-   Sono disponibili istruzioni atomiche.
-   Potrebbe essere disponibile il supporto della precisione doppia. Per informazioni su come determinare se è disponibile la precisione doppia, vedere [**D3D11 \_ FEATURE \_ DOUBLES**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                              | Descrizione                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nuovi tipi di risorse](direct3d-11-advanced-stages-cs-resources.md)<br/>      | In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.<br/>                                                                                                                                                                                                 |
| [Accesso alle risorse](direct3d-11-advanced-stages-cs-access.md)<br/>        | Esistono diversi modi per accedere alle [risorse](overviews-direct3d-11-resources-types.md).<br/>                                                                                                                                                                   |
| [Funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Per accedere a un nuovo tipo di risorsa o a una memoria condivisa, usare una funzione intrinseca interlocked. È garantito che le funzioni interlocked funzionino in modo atomico. In altri modo, è garantito che si verifichino nell'ordine programmato. Questa sezione elenca le funzioni atomiche.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Procedura: Creare uno shader di calcolo](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

