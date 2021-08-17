---
title: Modelli di shader e profili shader
description: Modelli di shader e profili shader
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7f6a37b1d37225425a60cc42887d5e587d9522929bc78a28dbb5bf5854493f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726151"
---
# <a name="shader-models-vs-shader-profiles"></a>Modelli di shader e profili shader

Il linguaggio di ombreggiatura di alto livello per DirectX implementa una serie di modelli di shader. Con HLSL è possibile creare shader programmabili simili a C per la pipeline Direct3D. Ogni modello shader si basa sulle funzionalità del modello precedente, implementando più funzionalità con meno restrizioni.

Il modello shader 1 è stato avviato con DirectX 8 e include istruzioni a livello di assembly e simili a C. Questo modello presenta molte limitazioni causate dall'hardware dello shader programmabile in anticipo. Il modello di shader 2 e 3 è notevolmente espanso in base al numero di istruzioni e gli shader costanti possono usare. Sono molto più potenti del modello shader 1, ma presentano comunque alcune delle limitazioni esistenti del primo modello shader.

A partire da Windows Vista, il modello shader 4 è una riprogettazione completa. Consente istruzioni e costanti illimitate (all'interno dei vincoli hardware del computer), dispone di oggetti modellati per rendere il campionamento delle trame più pulito e più efficiente e presenta il numero minimo di restrizioni di qualsiasi modello shader. Richiede tuttavia il modello Windows Driver, disponibile solo nel sistema operativo Windows Vista (o versioni successive).

## <a name="shader-profiles"></a>Profili shader

Un profilo shader è la destinazione per la compilazione di uno shader. Questa tabella elenca i profili di shader supportati da ogni modello di shader.



| Modello shader                                                   | Profili shader                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modello shader 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Modello shader 2](dx-graphics-hlsl-sm2.md)         | ps \_ 2 \_ 0, ps \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 \_ level \_ 9 \_ 0, ps \_ 4 \_ 0 level \_ \_ 9 \_ 1, ps \_ 4 \_ 0 level \_ \_ 9 \_ 3, vs \_ 4 \_ 0 level \_ \_ \_ 9 0, vs \_ \_ \_ \_ 4 0 level \_ 9 1, vs \_ 4 \_ 0 level \_ \_ 9 \_ 3, lib \_ 4 \_ 0 \_ level \_ 9 \_ 1, lib \_ 4 \_ 0 level \_ \_ 9 \_ 3                                                                      |
| [Modello shader 3](dx-graphics-hlsl-sm3.md)         | ps \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)         | cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Modello shader 5](d3d11-graphics-reference-sm5.md) | cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (anche se gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps 4 1, vs 4 0 e vs 4 1 \_ \_ \_ \_ \_ \_ sono stati introdotti nel modello shader 4.0, il modello shader 5 aggiunge il supporto a questi profili shader per buffer strutturati e buffer di indirizzi byte).<br/> |
| [Modello shader 6](shader-model-6-0.md)             | cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |

Differenze tra Direct3D 9 e Direct3D 10:

- Direct3D 9 ha introdotto i modelli di shader 1, 2 e 3.
- Direct3D 10 ha introdotto il modello shader 4.
- Direct3D 10.1 ha introdotto il modello shader 4.1.



 

## <a name="effect-profiles"></a>Profili di effetto

Un profilo di effetto è la destinazione per la compilazione di un effetto/shader. Questa tabella elenca i profili di effetto supportati da ogni versione di Direct3D.

Differenze tra Direct3D 9 e Direct3D 10:

- Direct3D 9 ha introdotto i profili del framework degli effetti fx \_ 1 \_ 0 e fx \_ 2 \_ 0.
- Direct3D 10 ha introdotto effect-framework profile fx \_ 4 \_ 0.
- Direct3D 10.1 ha introdotto effect-framework profile fx \_ 4 \_ 1.
- Direct3D 11 ha introdotto effect-framework profile fx \_ 5 \_ 0.

> [!Note]  
> Questi profili di effetti legacy sono deprecati.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





