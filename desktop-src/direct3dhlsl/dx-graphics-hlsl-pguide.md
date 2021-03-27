---
title: Guida per programmatori per HLSL
description: I dati entrano nella pipeline grafica come flusso di primitivi e vengono elaborati dalle fasi dello shader.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "104980975"
---
# <a name="programming-guide-for-hlsl"></a>Guida per programmatori per HLSL

I dati entrano nella pipeline grafica come flusso di primitivi e vengono elaborati dalle fasi dello shader. Le fasi dello shader effettive dipendono dalla versione di Direct3D, ma includono sicuramente le fasi vertex, pixel e Geometry. Altre fasi includono gli shader Hull e Domain shader per lo schema a mosaico e compute shader. Queste fasi sono completamente programmabili utilizzando[HLSL](dx-graphics-hlsl-reference.md)(High Level Shading Language).

Gli shader HLSL possono essere compilati in fase di creazione o di esecuzione e impostati in fase di esecuzione nella fase della pipeline appropriata. Gli shader Direct3D 9 possono essere progettati usando [Shader Model 1](dx-graphics-hlsl-sm1.md), [Shader Model 2](dx-graphics-hlsl-sm2.md) e [Shader Model 3](dx-graphics-hlsl-sm3.md); Gli shader Direct3D 10 possono essere progettati solo in [Shader Model 4](dx-graphics-hlsl-sm4.md). Gli shader Direct3D 11 possono essere progettati in [Shader Model 5](d3d11-graphics-reference-sm5.md). Direct3D 11,3 e Direct3D 12 possono essere progettati in [shader model 5,1](shader-model-5-1.md). Inoltre, è possibile progettare Direct3D 12 su [Shader Model 6](shader-model-6-0.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Uso del collegamento shader](using-shader-linking.md) | Viene illustrato come creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione. |
| [Scrittura di shader HLSL in Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Uso degli shader in Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Uso degli shader in Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Ottimizzazione degli shader HLSL](dx-graphics-hlsl-optimize.md) | |
| [Debug di shader in Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | Lo strumento più recente per il debug degli shader ora viene fornito come funzionalità in Microsoft Visual Studio, denominato debugger grafica di Visual Studio.  |
| [Compilazione di shader](dx-graphics-hlsl-part1.md) | Verranno ora esaminati i vari modi per compilare il codice e le convenzioni dello shader per le estensioni di file per il codice dello shader. |
| [Specifica delle destinazioni del compilatore](specifying-compiler-targets.md) | Qui sono elencate le destinazioni per i vari profili supportati dalle funzioni **D3DCompile \** _ e dal compilatore HLSL. |
| [Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Uso della precisione minima HLSL](using-hlsl-minimum-precision.md) | A partire da Windows 8, i driver grafici possono implementare i [tipi di dati scalari HLSL](dx-graphics-hlsl-scalar.md) precisione minima usando una precisione maggiore o uguale alla precisione dei bit specificata.  |
| [HLSL Shader Model 5](overviews-direct3d-11-hlsl.md) | |
| [Modello HLSL shader 5,1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | In questa sezione vengono descritte le funzionalità del modello shader 5,1 che si applicano in pratica a D3D12 e D3D 11.3. Tutti i componenti hardware DirectX 12 supportano il modello di shader 5,1. |
| [Modello HLSL shader 6,0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Descrive gli intrinseci dell'operazione Wave aggiunti al modello HLSL shader 6,0. |
| [Modello HLSL shader 6,4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Descrive gli intrinseci di Machine Learning aggiunti al modello HLSL shader 6,4. |

## <a name="related-topics"></a>Argomenti correlati

_ [HLSL](dx-graphics-hlsl.md)
* [Riferimento per HLSL](dx-graphics-hlsl-reference.md)
