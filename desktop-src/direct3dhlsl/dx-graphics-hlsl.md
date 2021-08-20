---
title: Linguaggio shader di alto livello (HLSL)
description: HLSL è il linguaggio shader di alto livello simile a C che si usa con shader programmabili in DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: 9f518102b7b3305103ed85231a791c542418a04c
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812897"
---
# <a name="high-level-shader-language-hlsl"></a>Linguaggio shader di alto livello (HLSL)

HLSL è il linguaggio shader di alto livello simile a C che si usa con shader programmabili in DirectX.

Ad esempio, è possibile usare HLSL per scrivere un [vertex shader](../direct3d11/vertex-shader-stage.md)o [un pixel shader](../direct3d11/pixel-shader-stage.md)e usare tali shader nell'implementazione del renderer nell'applicazione [Direct3D.](../direct3d12/directx-12-programming-guide.md)

Oppure è possibile usare HLSL per scrivere un compute shader, ad esempio per implementare una simulazione fisica. Se, ad esempio, si è in grado di scrivere un operatore di convoluzione personalizzato (per l'elaborazione di immagini) come HLSL in un compute shader, si otterrà prestazioni migliori in questo scenario se si usa [Direct Machine Learning (DirectML).](/windows/ai/directml/dml)

HLSL è stato creato (a partire da DirectX 9) per configurare la pipeline 3D [programmabile.](../direct3d11/overviews-direct3d-11-graphics-pipeline.md) È possibile programmare l'intera pipeline con istruzioni HLSL.

## <a name="where-to-go-next"></a>Dove andare dopo

* [Guida alla programmazione per HLSL](./dx-graphics-hlsl-pguide.md)
* [Informazioni di riferimento per HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Guida alla programmazione per HLSL

Per un'introduzione concettuale a HLSL, vedere la Guida [alla programmazione per HLSL.](./dx-graphics-hlsl-pguide.md)

La guida alla programmazione illustra i diversi tipi di fasi dello shader e come creare, compilare, ottimizzare, associare e collegare gli shader.

Sono disponibili anche panoramiche e note sulla versione relative alle generazioni successive di versione del modello shader rilasciate, fino al modello di shader HLSL 5.

### <a name="reference-for-hlsl"></a>Informazioni di riferimento per HLSL

Per la documentazione di riferimento di HLSL, vedere [Informazioni di riferimento per HLSL.](./dx-graphics-hlsl-reference.md)

La sezione di riferimento include un elenco completo della sintassi del linguaggio e delle funzioni intrinseche incorporate in HLSL per semplificare i requisiti di codifica.

È anche possibile trovare una descrizione dei modelli di shader rispetto ai profili e del contenuto di riferimento del modello shader fino al modello di shader HLSL 1. Sono disponibili anche contenuti relativi alle istruzioni per l'assembly, allo strumento D3DCompiler e alle informazioni sugli errori e gli avvisi che possono essere restituiti da uno shader.