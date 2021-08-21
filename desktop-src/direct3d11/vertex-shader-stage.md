---
title: Fase vertex shader
description: La fase vertex shader (VS) elabora i vertici dell'assembler di input, eseguendo operazioni per vertice, ad esempio trasformazioni, skinning, morphing e illuminazione per vertice.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3815f4c26c97e68ac0b4b20b72849052710f2f6adc0722bb3e42f5c8bf7a1c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530409"
---
# <a name="vertex-shader-stage"></a>Fase vertex shader

La fase vertex shader (VS) elabora i vertici dell'assembler di input, eseguendo operazioni per vertice, ad esempio trasformazioni, skinning, morphing e illuminazione per vertice. I vertex shader operano sempre su un singolo vertice di input e producono un singolo vertice di output. La fase vertex shader deve essere sempre attiva per l'esecuzione della pipeline. Se non è necessaria alcuna modifica o trasformazione del vertice, è necessario creare e impostare un vertex shader pass-through sulla pipeline.

## <a name="the-vertex-shader"></a>The Vertex Shader

Ogni vertice di input vertex shader può essere costituito da fino a 16 vettori a 32 bit (fino a 4 componenti ciascuno) e ogni vertice di output può essere costituito da fino a 16 vettori a 32 bit a 4 componenti. Tutti i vertex shader devono avere almeno un input e un output, che possono avere un solo valore scalare.

La fase vertex shader può utilizzare due valori generati dal sistema dall'assembler di input: VertexID e InstanceID (vedere Valori di sistema e semantica). Poiché VertexID e InstanceID sono entrambi significativi a livello di vertice e gli ID generati dall'hardware possono essere immessi solo nella prima fase che li comprende, questi valori ID possono essere immessi solo nella fase vertex shader.

I vertex shader vengono sempre eseguiti su tutti i vertici, inclusi i vertici adiacenti nelle topologie primitive di input con adizia. Il numero di volte in cui è stato eseguito il vertex shader può essere sottoposto a query dalla CPU usando la statistica della pipeline VSInvocations.

Un vertex shader può eseguire operazioni di campionamento del carico e della trama in cui non sono necessari derivati dello spazio dello schermo (usando funzioni intrinseche HLSL: [Sample (DirectX HLSL Texture Object),](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample) [SampleCmpLevelZero (DirectX HLSL Texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)e [SampleGrad (Oggetto trama DirectX HLSL).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 