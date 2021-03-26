---
title: Modello HLSL shader 6,0
description: Descrive gli intrinseci dell'operazione Wave aggiunti al modello HLSL shader 6,0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d082fc131c7cd08db9eb1861c4af39d600f40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976706"
---
# <a name="hlsl-shader-model-60"></a>Modello HLSL shader 6,0

Descrive gli intrinseci dell'operazione Wave aggiunti al modello HLSL shader 6,0.

- [Modello shader 6,0](#shader-model-60)
- [Terminologia](#terminology)
- [Funzioni intrinseche di linguaggio ombreggiatura](#shading-language-intrinsics)
    - [Query Wave](#wave-query)
    - [Voto Wave](#wave-vote)
    - [Trasmissione Wave](#wave-broadcast)
    - [Riduzione Wave](#wave-reduction)
    - [Analisi Wave e prefisso](#wave-scan-and-prefix)
    - [Operazioni shuffle a tutto il mondo](#quad-wide-shuffle-operations)
- [Funzionalità hardware](#hardware-capability)
- [Argomenti correlati](#related-topics)

## <a name="shader-model-60"></a>Modello shader 6,0

Per i modelli shader precedenti, la programmazione HLSL espone solo un singolo thread di esecuzione. Sono disponibili nuove operazioni a livello di onda, a partire dal modello 6,0, per sfruttare in modo esplicito il parallelismo delle GPU correnti. molti thread possono essere eseguiti in contemporanea contemporaneamente nello stesso core. Ad esempio, le funzioni intrinseche del modello 6,0 consentono l'eliminazione dei costrutti di barriera quando l'ambito della sincronizzazione rientra nella larghezza del processore SIMD o in un altro set di thread noto come atomici l'uno rispetto all'altro.

I potenziali casi d'uso includono: compattazione del flusso, riduzioni, trasformazioni di blocchi, ordinamento bitonico o trasformazioni di Fourier veloce (FFT), suddivisione in contenitori, deduplicazione del flusso e scenari simili.

La maggior parte degli intrinseci viene visualizzata in pixel shader e Compute Shaders, anche se esistono alcune eccezioni (indicate per ogni funzione). Le funzioni sono state aggiunte ai requisiti per il livello di funzionalità DirectX 12,0, in livello API 12.

Il *<type>* parametro e il valore restituito per queste funzioni implicano il tipo di espressione. i tipi supportati sono quelli dell'elenco seguente che sono presenti *anche* nel modello di shader di destinazione per l'app:

- Half, Half2, half3, half4
- float, float2, float3, float4
- Double, Double2, Double3, double4
- int, int2, INT3, INT4
- uint, uint2, uint3, uint4
- Short, Short2, short3, Short4
- ushort, ushort2, ushort3, ushort4
- UInt64 \_ t, UInt64 \_ T2, UInt64 \_ T3, UInt64 \_ T4

Alcune operazioni, ad esempio gli operatori bit per bit, supportano solo i tipi Integer.

## <a name="terminology"></a>Terminologia

| | |
|-|-|
| **Termine** | **Definizione** |
| Lane | Singolo thread di esecuzione. I modelli shader prima della versione 6,0 espongono solo uno di questi a livello di linguaggio, lasciando l'espansione all'elaborazione parallela SIMD interamente fino all'implementazione. |
| Wave | Set di corsie (thread) eseguiti simultaneamente nel processore. Non sono necessarie barriere esplicite per garantire che vengano eseguite in parallelo. I concetti simili includono "Warp" e "fronte d'onda". |
| Corsia inattiva | Una corsia che non viene eseguita, ad esempio a causa del flusso di controllo, oppure di un lavoro insufficiente per riempire la dimensione minima dell'onda. |
| Corsia attiva | Corsia per cui viene eseguita l'esecuzione. In pixel shader, può includere qualsiasi corsia di supporto per i pixel. |
| Quad | Set di 4 corsie adiacenti corrispondenti ai pixel disposti in un quadrato 2x2. Vengono usati per stimare le sfumature mediante differenze in x o y. Un'onda può essere costituita da più quad. Vengono eseguiti tutti i pixel in un quad attivo (e possono essere "corsie attive"), ma quelli che non producono risultati visibili sono denominati "corsie Helper". |
| Corsia Helper | Una corsia che viene eseguita esclusivamente per lo scopo delle sfumature in pixel shader quad. L'output di tale corsia verrà rimosso e pertanto non verrà eseguito il rendering nell'area di destinazione. |

## <a name="shading-language-intrinsics"></a>Funzioni intrinseche di linguaggio ombreggiatura

Tutte le operazioni di questo modello shader sono state aggiunte in un intervallo di funzioni intrinseche.

### <a name="wave-query"></a>Query Wave

Funzioni intrinseche per l'esecuzione di query su una singola onda.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descrizione** | **Pixel shader** | **Compute Shader** |
| [**WaveGetLaneCount**](wavegetlanecount.md) | Restituisce il numero di corsie nell'onda corrente. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Restituisce l'indice della corsia corrente all'interno dell'onda corrente. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Restituisce true solo per la corsia attiva nell'onda corrente con l'indice più piccolo | \* | \* |

### <a name="wave-vote"></a>Voto Wave

Questo set di funzioni intrinseche Confronta i valori tra i thread attualmente attivi dall'onda corrente.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descrizione** | **Pixel shader** | **Compute Shader** |
| [**WaveActiveAnyTrue**](waveanytrue.md) | Restituisce true se l'espressione è true in qualsiasi corsia attiva nell'onda corrente. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Restituisce true se l'espressione è true in tutte le corsie attive nell'onda corrente. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Restituisce una maschera di bit Unsigned Integer a 64 bit della valutazione dell'espressione booleana per tutte le corsie attive nell'onda specificata. | \* | \* |

### <a name="wave-broadcast"></a>Trasmissione Wave

Queste funzioni intrinseche consentono a tutte le corsie attive nell'onda corrente di ricevere il valore dalla corsia specificata, trasmettendo la trasmissione in modo efficace. Il valore restituito da una corsia non valida non è definito.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descrizione** | **Pixel shader** | **Compute Shader** |
| [**WaveReadLaneAt**](wavereadlaneat.md) | Restituisce il valore dell'espressione per l'indice della corsia specificato all'interno dell'onda specificata. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Restituisce il valore dell'espressione per la corsia attiva dell'onda corrente con l'indice più piccolo. | \* | \* |

### <a name="wave-reduction"></a>Riduzione Wave

Queste funzioni intrinseche calcolano l'operazione specificata su tutte le corsie attive nell'onda e trasmettono il risultato finale a tutte le corsie attive. L'output finale viene pertanto garantito uniforme nell'onda.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descrizione** | **Pixel shader** | **Compute Shader** |
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e di conseguenza uniforme). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Restituisce l'OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Restituisce l'oggetto OR esclusivo bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Conta il numero di variabili booleane che restituiscono true tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Calcola il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Calcola il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Analisi Wave e prefisso

Queste funzioni intrinseche applicano l'operazione a ogni corsia e lasciano ogni risultato parziale del calcolo nella corsia corrispondente.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descrizione** | **Pixel shader** | **Compute Shader** |
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questo. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Restituisce il prodotto di tutti i valori nelle corsie precedenti a quello dell'onda specificata. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Operazioni shuffle a tutto il mondo

Queste funzioni intrinseche eseguono operazioni di scambio sui valori in un'onda nota per contenere pixel shader quad come definito qui. Gli indici dei pixel nel quad sono definiti nella riga di analisi o nell'ordine di lettura, in cui le coordinate all'interno di un quad sono:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

S 


Queste routine funzionano in compute shader o pixel shader. In Compute Shaders operano in quad definiti come gruppi divisi uniformemente di 4 all'interno di un SIMD Wave. Nei pixel shader è necessario usare le onde acquisite da WaveQuadLanes. in caso contrario, i risultati non sono definiti.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Descrizione** | **Pixel shader** | **Compute Shader** |
| [**QuadReadLaneAt**](quadreadlaneat.md) | Restituisce il valore di origine specificato letto dalla corsia del Quad corrente identificato da quadLaneID \[ 0.. 3 \] che deve essere uniforme nel quad. | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | Restituisce il valore locale specificato che viene letto dalla corsia opposta in senso diagonale in questo quad. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione X. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y. | \* | |

## <a name="hardware-capability"></a>Funzionalità hardware

Per verificare che le funzionalità dell'operazione Wave siano disponibili in qualsiasi hardware specifico, chiamare [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport), annotando la descrizione e l'utilizzo della [**struttura \_ \_ \_ D3D12 \_ OPTIONS1 data della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) .

## <a name="related-topics"></a>Argomenti correlati

* [Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
* [Oggetti intrinseci del modello di shader 6](shader-model-6-0.md)