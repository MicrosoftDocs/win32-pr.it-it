---
title: Modello shader 6
description: Il modello shader 6.0 aggiunge un intervallo di funzioni intrinseche dell'operazione wave per i pixel e gli shader di calcolo.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609f0a9d36fbf7414e724cd31bc05a8e4d6abdefa5c842f30934feba0dffb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790700"
---
# <a name="shader-model-6"></a>Modello shader 6

Tutti gli intrinseci Wave non correlati ai quad sono disponibili in tutte le fasi dello shader. Gli intrinseci delle onde quadre sono disponibili solo negli shader pixel e di calcolo.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | Restituisce il valore locale specificato letto dalla corsia diagonalmente opposta in questo quad.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Restituisce il valore di origine specificato dalla corsia identificata dall'ID corsia all'interno del quad corrente.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Restituisce il valore locale specificato letto dall'altra corsia in questo quad nella direzione X.<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e quindi uniforme su di essa).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Restituisce l'AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Restituisce l'OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Restituisce l'XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Conta il numero di variabili booleane che restituiscono true in tutte le corsie attive nell'ondata corrente e replica il risultato in tutte le corsie dell'onda.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Restituisce il valore massimo dell'espressione in tutte le corsie attive nell'ondata corrente e la replica in tutte le corsie attive. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Restituisce il valore minimo dell'espressione in tutte le corsie attive nell'ondata corrente e la replica in tutte le corsie attive. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Moltiplica i valori dell'espressione tra tutte le corsie attive nell'ondata corrente e la replica in tutte le corsie attive.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie nell'ondata corrente.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Restituisce true se l'espressione è true in tutte le corsie attive nell'ondata corrente.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Restituisce true se l'espressione è true in una delle corsie attive nell'ondata corrente.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Restituisce una maschera di bit di interi senza segno a 4 bit della valutazione dell'espressione booleana per tutte le corsie attive nell'ondata specificata. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Restituisce il numero di corsie in un'onda su questa architettura. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Restituisce l'indice della corsia corrente all'interno dell'ondata corrente. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Restituisce true solo per la corsia attiva nell'ondata corrente con l'indice più piccolo. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici inferiori alla corsia corrente. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Restituisce il prodotto di tutti i valori nelle corsie attive in questa ondata con indici inferiori a questa corsia.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questa.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Restituisce il valore dell'espressione per la corsia attiva dell'ondata corrente con l'indice più piccolo. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Restituisce il valore dell'espressione per l'indice di corsia specificato all'interno dell'onda specificata.<br/>                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelli shader e profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





