---
title: Fase vertex shader
description: La fase vertex-shader (VS) elabora i vertici dall'assembler di input, eseguendo operazioni per vertice, ad esempio le trasformazioni, il skinning, il morphing e l'illuminazione per vertice.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a291b4abed572da54f9a2616ce19e926e1c6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046772"
---
# <a name="vertex-shader-stage"></a>Fase vertex shader

La fase vertex-shader (VS) elabora i vertici dall'assembler di input, eseguendo operazioni per vertice, ad esempio le trasformazioni, il skinning, il morphing e l'illuminazione per vertice. I vertex shader operano sempre su un singolo vertice di input e producono un singolo vertice di output. Per eseguire la pipeline è necessario che la fase vertex shader sia sempre attiva. Se non è richiesta alcuna modifica o trasformazione del vertice, è necessario creare un vertex shader pass-through e impostarlo sulla pipeline.

## <a name="the-vertex-shader"></a>Vertex shader

Ogni vertice di input del vertex shader può essere composto da un massimo di vettori a 16 32 bit (fino a 4 componenti ciascuno) e ogni vertice di output può essere costituito da un numero di vettori di 4 componenti a 16 32 bit. Tutti i vertex shader devono contenere almeno un input e un output, che può essere un valore scalare.

La fase vertex shader può utilizzare due valori generati dal sistema dall'assembler di input: VertexID e InstanceID (vedere valori di sistema e semantica). Poiché VertexID e InstanceID sono entrambi significativi a livello di vertice e gli ID generati dall'hardware possono essere inseriti solo nella prima fase che li comprende, questi valori ID possono essere inseriti solo nella fase vertex shader.

I vertex shader vengono sempre eseguiti su tutti i vertici, inclusi i vertici adiacenti nelle topologie primitive di input con adiacenza. Il numero di volte in cui è stato eseguito il vertex shader può essere sottoposto a query dalla CPU utilizzando le statistiche della pipeline VSInvocations.

Un vertex shader può eseguire operazioni di campionamento del carico e della trama in cui i derivati dello spazio dello schermo non sono obbligatori (usando funzioni intrinseche HLSL: [Sample (oggetto trama di DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [SampleCmpLevelZero (oggetto trama di DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)e [SampleGrad (oggetto trama di DirectX HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 