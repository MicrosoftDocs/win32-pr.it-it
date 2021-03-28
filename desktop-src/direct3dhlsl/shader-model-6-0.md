---
title: Modello shader 6
description: Il modello di shader 6,0 aggiunge una gamma di funzioni intrinseche delle operazioni Wave per i pixel e i compute shader.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33eb4eab2a92e929bdefdc1df0f9cb1e0d84909a
ms.sourcegitcommit: 39fe65a8a7c1cbea382c78820663c548f4e77079
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118658"
---
# <a name="shader-model-6"></a>Modello shader 6

Tutte le funzioni intrinseche Wave correlate non quadre sono disponibili in tutte le fasi dello shader. Gli intrinseci Wave quad sono disponibili solo in pixel e compute shader.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | Restituisce il valore locale specificato che viene letto dalla corsia opposta in senso diagonale in questo quad.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Restituisce il valore di origine specificato dalla corsia identificata dall'ID della corsia all'interno del Quad corrente.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Restituisce il valore locale specificato letto dall'altra corsia in questo quad nella direzione X.<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e di conseguenza uniforme).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Restituisce l'OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Restituisce l'oggetto XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Conta il numero di variabili booleane che restituiscono true tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Restituisce il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Restituisce il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente che viene replicato nuovamente in tutte le corsie attive. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie nell'onda corrente.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Restituisce true se l'espressione è true in tutte le corsie attive nell'onda corrente.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Restituisce true se l'espressione è true in una delle corsie attive nell'onda corrente.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Restituisce una maschera di bit Unsigned Integer a 4 bit della valutazione dell'espressione booleana per tutte le corsie attive nell'onda specificata. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Restituisce il numero di corsie in un'onda in questa architettura. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Restituisce l'indice della corsia corrente all'interno dell'onda corrente. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Restituisce true solo per la corsia attiva nell'onda corrente con l'indice più piccolo. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Restituisce il prodotto di tutti i valori nelle corsie attive in questa Wave con indici inferiori a questa corsia.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questo.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Restituisce il valore dell'espressione per la corsia attiva dell'onda corrente con l'indice più piccolo. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Restituisce il valore dell'espressione per l'indice della corsia specificato all'interno dell'onda specificata.<br/>                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





