---
title: Guida alla programmazione per HLSL
description: I dati entrano nella pipeline grafica come flusso di primitive e vengono elaborati dalle fasi dello shader.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca0b1f93b3c5f56cd7a074571ec6657cedc924688606e3612a66ef0f9e40d51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726070"
---
# <a name="programming-guide-for-hlsl"></a>Guida alla programmazione per HLSL

I dati entrano nella pipeline grafica come flusso di primitive e vengono elaborati dalle fasi dello shader. Le fasi effettive dello shader dipendono dalla versione di Direct3D, ma includono sicuramente le fasi vertice, pixel e geometria. Altre fasi includono gli shader della scafo e del dominio per la tessellazione e il compute shader. Queste fasi sono completamente programmabili usando il linguaggio di ombreggiatura di alto livello[(HLSL).](dx-graphics-hlsl-reference.md)

Gli shader HLSL possono essere compilati in fase di creazione o di runtime e impostati in fase di esecuzione nella fase di pipeline appropriata. Gli shader Direct3D 9 possono essere progettati usando il modello [shader 1,](dx-graphics-hlsl-sm1.md)il modello [shader 2](dx-graphics-hlsl-sm2.md) e [il modello shader 3.](dx-graphics-hlsl-sm3.md) Gli shader Direct3D 10 possono essere progettati solo nel modello [shader 4.](dx-graphics-hlsl-sm4.md) Gli shader Direct3D 11 possono essere progettati nel modello [di shader 5.](d3d11-graphics-reference-sm5.md) Direct3D 11.3 e Direct3D 12 possono essere progettati sul modello [shader 5.1](shader-model-5-1.md)e Direct3D 12 può anche essere progettato sul modello [shader 6.](shader-model-6-0.md)

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Uso del collegamento di shader](using-shader-linking.md) | Viene illustrato come creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione. |
| [Scrittura di shader HLSL in Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Uso degli shader in Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Uso degli shader in Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Ottimizzazione degli shader HLSL](dx-graphics-hlsl-optimize.md) | |
| [Debug di shader in Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | Lo strumento più recente per il debug degli shader è ora disponibile come funzionalità di Microsoft Visual Studio, denominata debugger Visual Studio grafica.  |
| [Compilazione di shader](dx-graphics-hlsl-part1.md) | Si esaminino ora diversi modi per compilare il codice dello shader e le convenzioni per le estensioni di file per il codice dello shader. |
| [Specifica delle destinazioni del compilatore](specifying-compiler-targets.md) | Di seguito sono elencate le destinazioni per i vari profili supportati **dalla funzione \* D3DCompile** e dal compilatore HLSL. |
| [Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Uso della precisione minima HLSL](using-hlsl-minimum-precision.md) | A partire Windows 8, i driver di grafica possono implementare tipi di dati [scalari HLSL](dx-graphics-hlsl-scalar.md) a precisione minima usando qualsiasi precisione maggiore o uguale alla precisione in bit specificata.  |
| [Modello di shader HLSL 5](overviews-direct3d-11-hlsl.md) | |
| [Modello di shader HLSL 5.1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | Questa sezione descrive le funzionalità del modello shader 5.1 applicate in pratica a D3D12 e D3D11.3. Tutto l'hardware DirectX 12 supporta il modello shader 5.1. |
| [Modello di shader HLSL 6.0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Descrive gli intrinseci dell'operazione d'onda aggiunti al modello di shader HLSL 6.0. |
| [Modello di shader HLSL 6.4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Descrive gli intrinseci di Machine Learning aggiunti al modello di shader HLSL 6.4. |

## <a name="related-topics"></a>Argomenti correlati

* [Hlsl](dx-graphics-hlsl.md)
* [Informazioni di riferimento per HLSL](dx-graphics-hlsl-reference.md)
