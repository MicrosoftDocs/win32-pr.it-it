---
title: Panoramica di Compute Shader
description: Un compute shader è una fase programmabile dello shader che espande Microsoft Direct3D 11 oltre la programmazione grafica. La tecnologia compute shader è nota anche come tecnologia DirectCompute.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c890e63b468a993e0d08f678d2276d6ce2adad
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734754"
---
# <a name="compute-shader-overview"></a>Panoramica di Compute Shader

Un compute shader è una fase programmabile dello shader che espande Microsoft Direct3D 11 oltre la programmazione grafica. La tecnologia compute shader è nota anche come tecnologia DirectCompute.

Analogamente ad altri shader programmabili (ad esempio, vertex e geometry shader), un compute shader viene progettato e implementato con [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) , ma si tratta solo del punto in cui termina la somiglianza. Un compute shader fornisce un calcolo generale ad alta velocità e sfrutta i vantaggi dell'elevato numero di processori paralleli nell'unità di elaborazione grafica (GPU). Compute Shader fornisce funzionalità di condivisione della memoria e di sincronizzazione dei thread per consentire metodi di programmazione paralleli più efficaci. Chiamare il metodo [**sul ID3D11DeviceContext::D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) [**sul ID3D11DeviceContext::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) per eseguire i comandi in un compute shader. Un compute shader può essere eseguito in molti thread in parallelo.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Uso di compute shader nell'hardware Direct3D 10. x

Un compute shader in Microsoft Direct3D 10 è noto anche come DirectCompute 4. x.

Se si usa l'API Direct3D 11 e i driver aggiornati, il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 10 e l'hardware 10,1 Direct3D possono facoltativamente supportare un formato limitato di DirectCompute che usa i \_ profili CS 4 \_ 0 e cs \_ 4 \_ 1. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Quando si usa DirectCompute in questo hardware, tenere presenti le limitazioni seguenti:

-   Il numero massimo di thread è limitato al numero massimo di thread del gruppo di \_ thread d3d11 cs \_ 4 X per gruppo \_ \_ \_ \_ \_ \_ \_ (768) per gruppo.
-   La dimensione X e Y di **numThreads** è limitata al \_ gruppo di thread d3d11 cs \_ 4 \_ x \_ \_ \_ Max \_ x (768) e al \_ gruppo di thread d3d11 cs \_ 4 \_ x \_ \_ \_ Max \_ Y (768).
-   La dimensione Z di **numThreads** è limitata a 1.
-   La dimensione Z del dispatch è limitata ai \_ gruppi di thread d3d11 cs \_ 4 \_ X \_ Dispatch \_ Max \_ \_ \_ nella \_ \_ dimensione z (1).
-   Allo shader è possibile associare una sola vista di accesso non ordinato (D3D11 \_ cs \_ 4 \_ X \_ UAV \_ Register \_ Count è 1).
-   Solo i [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s e [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)sono disponibili come viste di accesso non ordinato.
-   Un thread può accedere solo alla propria area nella memoria groupshared per la scrittura, anche se può leggere da qualsiasi posizione.
-   [SV \_](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) È necessario usare groupIndex o [SV \_ DispatchThreadID](/windows/desktop/direct3dhlsl/sv-dispatchthreadid) per accedere alla memoria **groupshared** per la scrittura.
-   La memoria **Groupshared** è limitata a 16KB per gruppo.
-   Un singolo thread è limitato a un'area di 256 byte della memoria **groupshared** per la scrittura.
-   Non sono disponibili istruzioni atomiche.
-   Non sono disponibili valori a precisione doppia.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Uso di compute shader nell'hardware Direct3D 11. x

Un compute shader in Direct3D 11 è anche noto come DirectCompute 5,0.

Quando si usa DirectCompute con \_ \_ i [profili](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)CS 5 0, tenere presenti gli elementi seguenti:

-   Il numero massimo di thread è limitato al numero massimo di thread del gruppo di thread D3D11 CS per gruppo \_ \_ \_ \_ \_ \_ \_ (1024) per gruppo.
-   La dimensione X e Y di **numThreads** è limitata al \_ gruppo di thread d3d11 cs \_ \_ \_ Max \_ X (1024) e al \_ gruppo di thread d3d11 cs \_ \_ \_ Max \_ Y (1024).
-   La dimensione Z di **numThreads** è limitata al \_ gruppo di thread d3d11 cs \_ \_ \_ Max \_ Z (64).
-   La dimensione massima del dispatch è limitata ai \_ gruppi di \_ thread max dispatch d3d11 cs \_ \_ \_ \_ per \_ dimensione (65535).
-   Il numero massimo di viste di accesso non ordinato che è possibile associare a uno shader è D3D11 \_ PS \_ cs \_ UAV \_ Register \_ Count (8).
-   Supporta [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)e le visualizzazioni tipizzate con accesso non ordinato ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)e così via).
-   Sono disponibili istruzioni atomiche.
-   Potrebbe essere disponibile un supporto a precisione doppia. Per informazioni su come determinare se è disponibile una doppia precisione, vedere [**d3d11 \_ feature \_ Double**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                              | Descrizione                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nuovi tipi di risorse](direct3d-11-advanced-stages-cs-resources.md)<br/>      | In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.<br/>                                                                                                                                                                                                 |
| [Accesso alle risorse](direct3d-11-advanced-stages-cs-access.md)<br/>        | Sono disponibili diversi modi per accedere alle [risorse](overviews-direct3d-11-resources-types.md).<br/>                                                                                                                                                                   |
| [Funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Per accedere a un nuovo tipo di risorsa o a una memoria condivisa, usare una funzione intrinseca Interlocked. Per le funzioni Interlocked è garantita l'operatività atomica. Ovvero, sono garantiti che si verifichino nell'ordine programmato. In questa sezione sono elencate le funzioni atomiche.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Procedura: creare un compute shader](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

