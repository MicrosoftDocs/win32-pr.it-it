---
title: Modello shader 4
description: Il modello shader 4 è un superset delle funzionalità del modello shader 3, ad eccezione del fatto che il modello shader 4 non supporta le funzionalità del modello shader 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c863d952990cd05394244fe662650df59568eeaf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466968"
---
# <a name="shader-model-4"></a>Modello shader 4

Il modello shader 4 è un superset delle funzionalità del modello shader [3,](dx-graphics-hlsl-sm3.md)ad eccezione del fatto che il modello shader 4 non supporta le funzionalità del modello shader 1. È stato progettato usando un core di shader comune che fornisce un set comune di funzionalità a tutti gli shader programmabili, che sono programmabili solo tramite HLSL.




| Caratteristica | Funzionalità | 
|---------|------------|
| Set di istruzioni | <a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a> | 
| Set di registri | Il set di registri è accessibile tramite membri in buffer costanti e trame usando la semantica HLSL per elementi come la creazione di un pacchetto di componenti.<ul><li>Registri pixel shader (vedere <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registri - ps_4_0</a> e Registri - <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">ps_4_1</a>)</li><li>Registri vertex shader (vedere <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registri - vs_4_0</a> e Registri - <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">vs_4_1</a>)</li><li>Registri geometry shader (vedere <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registri - gs_4_0</a> e Registri - <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">gs_4_1</a>)</li></ul> | 
| Vertex Shader Max | Nessuna restrizione | 
| Pixel Shader Max | Nessuna restrizione | 
| Nuovi profili shader aggiunti | gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1* | 
| Aggiunta Effect-Framework nuovo profilo | fx_4_0, fx_4_1* | 




 

\* - gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1 e fx \_ 4 \_ 1 sono supportati in Direct3D 10.1 o versione successiva.

Il modello di shader 4 supporta una nuova fase della pipeline, ovvero la fase geometry shader, che può essere usata per creare o modificare la geometria esistente. Include anche due nuovi tipi di oggetto: un oggetto di output del flusso progettato per trasmettere i dati dalla fase geometrica e un oggetto trama basato su modelli che implementa le funzioni di campionamento delle trame.

-   [Common-Shader Core](dx-graphics-hlsl-common-core.md)
-   [Costanti](dx-graphics-hlsl-constants.md)
-   [Oggetto Geometry Shader](dx-graphics-hlsl-geometry-shader.md)
-   [Oggetto Stream-Output](dx-graphics-hlsl-so-type.md)
-   [Oggetto Texture](dx-graphics-hlsl-to-type.md)

Il modello shader 4 supporta regole di creazione di un pacchetto che determinano la rigida disposta dei dati quando vengono archiviati. Queste regole sono descritte in [Regole di creazione pacchetto per le variabili costanti](dx-graphics-hlsl-packing-rules.md)

La [sezione Shader Model 4 Assembly (Assembly](dx-graphics-hlsl-sm4-asm.md) modello shader 4) descrive le istruzioni per l'assembly supportate da Shader Model 4 e Shader Model 4.1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di shader e profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




