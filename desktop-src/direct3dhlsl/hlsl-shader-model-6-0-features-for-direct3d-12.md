---
title: Modello shader HLSL 6.0
description: Descrive le funzioni intrinseche dell'operazione wave aggiunte al modello HLSL Shader 6.0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f0f06050c4c387b8e50c1c0cfb39dc5689d45d0e31bd7df5a81f45c63815a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986541"
---
# <a name="hlsl-shader-model-60"></a>Modello shader HLSL 6.0

Descrive le funzioni intrinseche dell'operazione wave aggiunte al modello HLSL Shader 6.0.

- [Modello shader 6.0](#shader-model-60)
- [Terminologia](#terminology)
- [Intrinseci del linguaggio di ombreggiatura](#shading-language-intrinsics)
    - [Wave Query](#wave-query)
    - [Wave Vote](#wave-vote)
    - [Trasmissione wave](#wave-broadcast)
    - [Riduzione delle onde](#wave-reduction)
    - [Scansione wave e prefisso](#wave-scan-and-prefix)
    - [Operazioni casuali a livello di quadrifoglio](#quad-wide-shuffle-operations)
- [Funzionalità hardware](#hardware-capability)
- [Argomenti correlati](#related-topics)

## <a name="shader-model-60"></a>Modello shader 6.0

Per i modelli shader precedenti, la programmazione HLSL espone un solo thread di esecuzione. Vengono fornite nuove operazioni a livello di ondata, a partire dal modello 6.0, per sfruttare in modo esplicito il parallelismo delle GPU correnti. Molti thread possono essere esecutori in lockstep nello stesso core contemporaneamente. Ad esempio, gli intrinseci del modello 6.0 consentono l'eliminazione dei costrutti di barriera quando l'ambito della sincronizzazione si trova all'interno della larghezza del processore SIMD o di un altro set di thread noti come atomici l'uno rispetto all'altro.

I possibili casi d'uso includono: compattazione del flusso, riduzioni, trasposizione a blocchi, ordinamento bitonico o trasformazioni Fast Fourier (FFT), binning, deduplicazione del flusso e scenari simili.

La maggior parte delle funzioni intrinseche viene visualizzata nei pixel shader e negli shader di calcolo, anche se esistono alcune eccezioni (notate per ogni funzione). Le funzioni sono state aggiunte ai requisiti per DirectX Feature Level 12.0, nel livello API 12.

Il parametro e il valore restituito per queste funzioni implicano il tipo dell'espressione, i tipi supportati sono quelli dell'elenco seguente che sono presenti anche nel modello shader di destinazione *<type>* per l'app: 

- half, half2, half3, half4
- float, float2, float3, float4
- double, double2, double3, double4
- int, int2, int3, int4
- uint, uint2, uint3, uint4
- short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- uint64 \_ t, uint64 \_ t2, uint64 \_ t3, uint64 \_ t4

Alcune operazioni, ad esempio gli operatori bit per bit, supportano solo i tipi Integer.

## <a name="terminology"></a>Terminologia

| **Termine** | **Definizione** |
|-|-|
| corsia | Singolo thread di esecuzione. I modelli shader precedenti alla versione 6.0 espongono solo uno di questi a livello di linguaggio, lasciando l'espansione all'elaborazione SIMD parallela interamente fino all'implementazione. |
| Wave | Set di corsie (thread) eseguite contemporaneamente nel processore. Non sono necessarie barriere esplicite per garantire che siano eseguite in parallelo. Concetti simili includono "warp" e "wavefront". |
| Corsia inattiva | Una corsia che non viene eseguita, ad esempio a causa del flusso di controllo o del lavoro insufficiente per riempire le dimensioni minime dell'onda. |
| Corsia attiva | Corsia per la quale viene eseguita l'esecuzione. Nei pixel shader può includere qualsiasi corsia di pixel helper. |
| Quad | Set di 4 corsie adiacenti corrispondenti ai pixel disposti in un quadrato 2x2. Vengono usati per stimare le sfumature in base a differenze in x o y. Un'onda può essere costituita da più quad. Tutti i pixel in un quad attivo vengono eseguiti (e possono essere "Corsie attive"), ma quelli che non producono risultati visibili sono d'uso come "Corsie helper". |
| Helper Lane | Una corsia che viene eseguita esclusivamente a scopo di sfumature in pixel shader quad. L'output di tale corsia verrà eliminato e quindi non verrà eseguito il rendering sulla superficie di destinazione. |

## <a name="shading-language-intrinsics"></a>Intrinseci del linguaggio di ombreggiatura

Tutte le operazioni di questo modello shader sono state aggiunte in un intervallo di funzioni intrinseche.

### <a name="wave-query"></a>Wave Query

Funzioni intrinseche per l'esecuzione di query su una singola ondata.

| **Intrinsic** | **Descrizione** | **Pixel shader** | **Shader di calcolo** |
|-|-|-|-|
| [**WaveGetLaneCount**](wavegetlanecount.md) | Restituisce il numero di corsie nell'ondata corrente. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Restituisce l'indice della corsia corrente all'interno dell'ondata corrente. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Restituisce true solo per la corsia attiva nell'ondata corrente con l'indice più piccolo | \* | \* |

### <a name="wave-vote"></a>Wave Vote

Questo set di funzioni intrinseche confronta i valori tra i thread attualmente attivi dall'ondata corrente.

| **Intrinsic** | **Descrizione** | **Pixel shader** | **Shader di calcolo** |
|-|-|-|-|
| [**WaveActiveAnyTrue**](waveanytrue.md) | Restituisce true se l'espressione è true in qualsiasi corsia attiva nell'ondata corrente. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Restituisce true se l'espressione è true in tutte le corsie attive nell'ondata corrente. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Restituisce una maschera di bit integer senza segno a 64 bit della valutazione dell'espressione booleana per tutte le corsie attive nell'onda specificata. | \* | \* |

### <a name="wave-broadcast"></a>Trasmissione wave

Questi intrinseci consentono a tutte le corsie attive nell'ondata corrente di ricevere il valore dalla corsia specificata, trasmettendo in modo efficace il valore. Il valore restituito da una corsia non valida non è definito.

| **Intrinsic** | **Descrizione** | **Pixel shader** | **Shader di calcolo** |
|-|-|-|-|
| [**WaveReadLaneAt**](wavereadlaneat.md) | Restituisce il valore dell'espressione per l'indice di corsia specificato all'interno dell'onda specificata. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Restituisce il valore dell'espressione per la corsia attiva dell'ondata corrente con l'indice più piccolo. | \* | \* |

### <a name="wave-reduction"></a>Riduzione delle onde

Questi intrinseci calcolano l'operazione specificata su tutte le corsie attive nell'onda e traslano il risultato finale a tutte le corsie attive. Di conseguenza, l'output finale è garantito uniforme su tutta l'onda.

| **Intrinsic** | **Descrizione** | **Pixel shader** | **Shader di calcolo** |
|-|-|-|-|
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e quindi uniforme su di essa). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Restituisce l'AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Restituisce l'OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Restituisce l'or esclusivo bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Conta il numero di variabili booleane che restituiscono true in tutte le corsie attive nell'ondata corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Calcola il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Calcola il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie nell'onda corrente e replica il risultato in tutte le corsie dell'onda. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Scansione wave e prefisso

Questi intrinseci applicano l'operazione a ogni corsia e lasciano ogni risultato parziale del calcolo nella corsia corrispondente.

| **Intrinsic** | **Descrizione** | **Pixel shader** | **Shader di calcolo** |
|-|-|-|-|
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici inferiori alla corsia corrente. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questa. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Restituisce il prodotto di tutti i valori nelle corsie prima dell'ondata specificata. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Operazioni casuali a livello di quadrifoglio

Questi intrinseci eseguono operazioni di scambio sui valori in un'onda nota per contenere pixel shader quad come definito qui. Gli indici dei pixel nel quad sono definiti in ordine di lettura o riga di analisi, dove le coordinate all'interno di un quad sono:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

S 


Queste routine funzionano in shader di calcolo o pixel shader. Negli shader di calcolo operano in quad definiti come gruppi divisi uniformemente di 4 all'interno di un'onda SIMD. Nei pixel shader devono essere usati sulle onde acquisite da WaveQuadLanes, in caso contrario i risultati non sono definiti.

| **Intrinsic** | **Descrizione** | **Pixel shader** | **Shader di calcolo** |
|-|-|-|-|
| [**QuadReadLaneAt**](quadreadlaneat.md) | Restituisce il valore di origine specificato letto dalla corsia del quad corrente identificato da quadLaneID \[ 0..3 che deve \] essere uniforme sul quad. | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | Restituisce il valore locale specificato letto dalla corsia diagonalmente opposta in questo quad. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione X. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y. | \* | |

## <a name="hardware-capability"></a>Funzionalità hardware

Per verificare che le funzionalità dell'operazione wave siano disponibili in qualsiasi hardware specifico, chiamare [**ID3D12Device::CheckFeatureSupport,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)annotando la descrizione e l'uso della struttura [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1)

## <a name="related-topics"></a>Argomenti correlati

* [Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
* [Funzioni intrinseche del modello shader 6](shader-model-6-0.md)
