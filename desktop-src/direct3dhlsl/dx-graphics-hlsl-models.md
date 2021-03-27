---
title: Modelli shader rispetto ai profili shader
description: Modelli shader rispetto ai profili shader
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856677"
---
# <a name="shader-models-vs-shader-profiles"></a>Modelli shader rispetto ai profili shader

Il linguaggio di ombreggiatura di alto livello per DirectX implementa una serie di modelli shader. Con HLSL è possibile creare shader programmabili di tipo C per la pipeline Direct3D. Ogni modello di shader si basa sul funzionalità del modello prima di esso, implementando una maggiore funzionalità con meno restrizioni.

Il modello di shader 1 è stato avviato con DirectX 8 ed è stato incluso il livello di assembly e le istruzioni di tipo C. Questo modello presenta molte limitazioni dovute all'hardware Shader programmabile. Il modello di shader 2 e 3 si espande notevolmente sul numero di istruzioni e le costanti shader possono usare. Sono molto più potenti rispetto al modello di shader 1, ma presentano comunque alcune delle limitazioni esistenti del primo modello di shader.

A partire da Windows Vista, Shader Model 4 è una riprogettazione completa. Consente istruzioni e costanti illimitate (all'interno dei vincoli hardware del computer), dispone di oggetti basati su modelli per rendere più semplice il campionamento della trama e più efficiente e presenta il minor numero di restrizioni di qualsiasi modello di shader. Richiede tuttavia la Windows Driver Model che è disponibile solo nel sistema operativo Windows Vista (o versioni successive).

## <a name="shader-profiles"></a>Profili shader

Un profilo shader è la destinazione per la compilazione di uno shader; Questa tabella elenca i profili shader supportati da ogni modello shader.



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modello di shader                                       | Profili shader                                                                                                                                                                                                                                                                                       |
| [Modello Shader 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Modello Shader 2](dx-graphics-hlsl-sm2.md)         | PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ level \_ 9 0 \_ , PS \_ 4 \_ 0 \_ level \_ 9 \_ 1, PS \_ 4 \_ 0 \_ level \_ 9 \_ 3, vs \_ 4 \_ 0 \_ level \_ 9 \_ 0, vs \_ 4 \_ 0 \_ level \_ 9 \_ 1, vs \_ 4 \_ 0 \_ level \_ 9 \_ 3, lib \_ 4 \_ 0 \_ level \_ 9 \_ 1, lib \_ 4 \_ 0 \_ \_ \_ Level 9 3                                                                      |
| [Modello Shader 3](dx-graphics-hlsl-sm3.md)         | PS \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)         | cs \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Modello Shader 5](d3d11-graphics-reference-sm5.md) | cs \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (sebbene GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 sono stati introdotti nel modello di Shader 4,0, Shader Model 5 aggiunge il supporto per i profili shader per i buffer strutturati e i buffer degli indirizzi byte).<br/> |
| [Modello shader 6](shader-model-6-0.md)             | cs \_ 6 \_ 0, DS \_ 6 0 \_ , GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 9 sono stati introdotti i modelli shader 1, 2 e 3.<br/> Direct3D 10 ha introdotto il modello di Shader 4.<br/> Direct3D 10,1 ha introdotto il modello di Shader 4,1.<br/> |



 

## <a name="effect-profiles"></a>Profili effetti

Un profilo di effetto è la destinazione per la compilazione di un effetto/shader; Questa tabella elenca i profili degli effetti supportati da ogni versione di Direct3D.



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 9 è stato introdotto Effect-framework Profiles FX \_ 1 \_ 0 e FX \_ 2 \_ 0.<br/> In Direct3D 10 è stato introdotto un effetto del profilo del Framework FX \_ 4 \_ 0.<br/> Direct3D 10,1 ha introdotto Effect-framework profile FX \_ 4 \_ 1.<br/> In Direct3D 11 è stato introdotto Effect-framework profile FX \_ 5 \_ 0.<br/> |



 

> [!Note]  
> Questi profili degli effetti legacy sono deprecati.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento per HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





