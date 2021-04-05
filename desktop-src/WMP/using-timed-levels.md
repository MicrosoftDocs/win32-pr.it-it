---
title: Utilizzo di livelli temporizzati
description: Utilizzo di livelli temporizzati
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- Visualizzazioni, eventi temporizzati
- Visualizzazioni personalizzate, eventi temporizzati
- Visualizzazioni, matrice di frequenza
- Visualizzazioni personalizzate, matrice di frequenza
- Visualizzazioni, matrice di forme d'onda
- Visualizzazioni personalizzate, matrice di forme d'onda
- Visualizzazioni, variabile di stato
- Visualizzazioni personalizzate, variabile di stato
- Visualizzazioni, variabile timeStamp
- Visualizzazioni personalizzate, variabile timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044739"
---
# <a name="using-timed-levels"></a>Utilizzo di livelli temporizzati

La struttura **TimedLevel** è costituita da matrici 2 2-dimensionali, da un valore di stato e da un valore di timestamp.

## <a name="frequency-array"></a>Matrice di frequenza

La matrice di frequenze è una matrice bidimensionale. La prima dimensione di ogni matrice corrisponde al canale audio stereo (a sinistra o a destra) e il secondo corrisponde ai livelli di frequenza (in byte) dello snapshot, in cui lo spettro audio è diviso in 1024 aree.

È possibile ottenere i dati della matrice di frequenza forniti dal Media Player Windows nel modo seguente:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



Il valore dello snapshot è per il canale sinistro e contiene il valore della parte più bassa dello spettro di frequenza. Se, ad esempio, lo snapshot ha un valore elevato, significa che la parte 1024th più bassa dello spettro di frequenza è ricca di frequenza. Un valore pari a zero indica che non sono presenti valori a bassa frequenza in tale parte dello spettro per il canale sinistro. Se si dispone di un segnale monofonico, solo la prima dimensione ha valori validi.

Se il segnale non è stereo, la seconda matrice conterrà una copia del segnale mono. Ovvero la frequenza \[ 0 \] \[ *n* \] e la frequenza \[ 1 n conterranno \] \[  \] gli stessi dati, dove *n* è l'indice in una cella particolare.

## <a name="waveform-array"></a>Matrice di forme d'onda

Anche la matrice di forme d'onda è una matrice bidimensionale. La prima dimensione della matrice corrisponde al canale (a sinistra o a destra) e il secondo corrisponde ai livelli di risparmio energia (in byte) dello snapshot, in cui la potenza audio viene suddivisa in 1024 segmenti di tempo contigui.

È possibile ottenere i dati della matrice di forme d'onda da Windows Media Player nel modo seguente:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



Il valore dello snapshot è per il canale sinistro e contiene il primo valore dello snapshot quantizzato dei valori di risparmio energia. Quando viene eseguito uno snapshot, è costituito da 1024 misure incrementali minime della potenza audio. Il valore più basso della matrice viene generato dalla prima misurazione incrementale della potenza audio. Si noti che i valori della potenza sono misurati da-128 a + 127, ma i valori nella matrice variano da 0 a 255. Se si dispone di un'onda monofonica, solo la prima dimensione avrà valori validi.

Se il segnale non è stereo, la seconda matrice conterrà una copia del segnale mono. Ovvero, la forma \[ d'onda 0 \] \[ *n* \] e la forma \[ d'onda 1 n conterranno \] \[  \] gli stessi dati, dove *n* è l'indice in una cella particolare.

## <a name="state"></a>State

La variabile di stato riflette lo stato di riproduzione audio di Windows Media Player. I valori di enumerazione PlayerState sono


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



È possibile usare questa variabile per eseguire azioni diverse a seconda dello stato di riproduzione audio. Ad esempio, è possibile riprodurre un tipo di visualizzazione quando l'audio viene riprodotto e un altro quando viene arrestato.

## <a name="time-stamp"></a>Timestamp

La variabile timeStamp riflette l'ora corrente in cui viene eseguita la snapshot. Questa operazione può essere usata per misurare la frequenza con cui vengono effettuati gli snapshot.

È possibile usare questa variabile per ora le animazioni. Se gli snapshot sono troppo frequenti, è possibile ridurre normalmente l'immagine per visualizzarla nel modo scelto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di rendering**](implementing-render.md)
</dt> </dl>

 

 




