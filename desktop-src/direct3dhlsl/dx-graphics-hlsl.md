---
title: High-Level Shader Language (HLSL)
description: HLSL è il linguaggio shader di alto livello di tipo C usato con shader programmabili in DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981042"
---
# <a name="high-level-shader-language-hlsl"></a>High-Level Shader Language (HLSL)

HLSL è il linguaggio shader di alto livello di tipo C usato con shader programmabili in DirectX.

Ad esempio, è possibile usare HLSL per scrivere un [vertex shader](../direct3d11/vertex-shader-stage.md)o un [pixel shader](../direct3d11/pixel-shader-stage.md)e usare gli shader nell'implementazione del renderer nell'applicazione [Direct3D](../direct3d12/directx-12-programming-guide.md) .

In alternativa, è possibile usare HLSL per scrivere un compute shader, ad esempio per implementare una simulazione fisica. Tuttavia, se, ad esempio, si è inclini a scrivere un proprio operatore di convoluzione (per l'elaborazione di immagini) come HLSL in un compute shader, si otterranno prestazioni migliori in tale scenario se si usa [Direct Machine Learning (DirectML)](../direct3d12/dml.md) .

HLSL è stato creato (a partire da DirectX 9) per configurare la [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programmabile. È possibile programmare l'intera pipeline con le istruzioni HLSL.

## <a name="where-to-go-next"></a>Dove andare avanti

* [Guida per programmatori per HLSL](./dx-graphics-hlsl-pguide.md)
* [Riferimento per HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Guida per programmatori per HLSL

Per un'introduzione concettuale a HLSL, vedere la [Guida alla programmazione di HLSL](./dx-graphics-hlsl-pguide.md).

Nella Guida alla programmazione vengono illustrati i diversi tipi di fasi dello shader e viene illustrato come creare, compilare, ottimizzare, associare e collegare shader.

Sono inoltre disponibili panoramiche e note sulla versione per le generazioni successive di versioni del modello shader rilasciate, tornando a HLSL Shader Model 5 (informazioni su).

### <a name="reference-for-hlsl"></a>Riferimento per HLSL

Per la documentazione di riferimento di HLSL, vedere il [riferimento per HLSL](./dx-graphics-hlsl-reference.md).

La sezione di riferimento include un elenco completo della sintassi del linguaggio e delle funzioni intrinseche integrate in HLSL per semplificare i requisiti di codifica.

È disponibile anche una discussione sui modelli di shader e i profili e il contenuto di riferimento del modello shader che torna a HLSL Shader Model 1. Sono disponibili anche le istruzioni per gli assembly, lo strumento D3DCompiler e informazioni sugli errori e gli avvisi che possono essere restituiti da uno shader.