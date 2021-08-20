---
title: Uso di livelli a tempo
description: Uso di livelli a tempo
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualizzazioni, eventi a tempo
- visualizzazioni personalizzate, eventi temporizzazione
- visualizzazioni,matrice di frequenze
- visualizzazioni personalizzate, matrice di frequenze
- visualizzazioni,matrice di forme d'onda
- visualizzazioni personalizzate, matrice waveform
- visualizzazioni, variabile di stato
- visualizzazioni personalizzate, variabile di stato
- visualizzazioni,variabile timeStamp
- visualizzazioni personalizzate, variabile timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6ce4d675fa37a519952f1b31d3c52cd93005a82eef977b7bd7d77623f1e508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116938"
---
# <a name="using-timed-levels"></a>Uso di livelli a tempo

La **struttura TimedLevel** è costituita da due matrici bidimensionali, un valore di stato e un valore di timestamp.

## <a name="frequency-array"></a>Matrice di frequenze

La matrice di frequenza è una matrice bidimensionale. La prima dimensione di ogni matrice corrisponde al canale audio stereo (a sinistra o a destra) e la seconda ai livelli di frequenza (in byte) dello snapshot, in cui lo spettro audio è suddiviso in 1024 aree.

È possibile ottenere i dati della matrice di frequenza forniti dal Windows Media Player nel modo seguente:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



Il valore di snapshot è per il canale sinistro e contiene il valore della parte più bassa dello spettro di frequenza. Ad esempio, se lo snapshot ha un valore elevato, indica che la parte più bassa 1024 dello spettro di frequenza è ricca di frequenza. Il valore zero indica che non sono presenti valori di bassa frequenza in quella parte dello spettro per il canale sinistro. Se si ha un segnale monofonico, solo la prima dimensione ha valori validi.

Se il segnale non è stereo, la seconda matrice conterrà una copia del segnale mono. In altri casi, la frequenza 0 n e la frequenza 1 n conterranno gli stessi dati, dove n è \[ \] \[  \] \[ \] \[  \] l'indice in una determinata cella. 

## <a name="waveform-array"></a>Matrice di forme d'onda

La matrice della forma d'onda è anche una matrice bidimensionale. La prima dimensione della matrice corrisponde al canale (a sinistra o a destra) e la seconda ai livelli di alimentazione (in byte) dello snapshot, in cui la potenza audio viene suddivisa in 1024 segmenti temporici contigui.

È possibile ottenere i dati della matrice waveform da Windows Media Player nel modo seguente:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



Il valore di snapshot è per il canale sinistro e contiene il primo valore dello snapshot quantizzato dei valori di potenza. Quando viene creato uno snapshot, è costituito da 1024 piccole misurazioni incrementali della potenza audio. Il valore più basso della matrice viene generato dalla prima misurazione incrementale della potenza audio. Si noti che i valori della potenza vengono misurati da -128 a +127, ma i valori nella matrice sono da 0 a 255. Se si ha un'ondata monofonico, solo la prima dimensione avrà valori validi.

Se il segnale non è stereo, la seconda matrice conterrà una copia del segnale mono. In altri casi, la forma d'onda 0 n e la forma d'onda 1 n conterranno gli stessi dati, dove n è l'indice \[ \] \[  \] \[ in una determinata \] \[  \] cella. 

## <a name="state"></a>State

La variabile state riflette lo stato di riproduzione audio Windows Media Player. I valori dell'enumerazione PlayerState sono


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



È possibile usare questa variabile per eseguire azioni diverse a seconda dello stato di riproduzione audio. Ad esempio, è possibile riprodurre un tipo di visualizzazione durante la riproduzione dell'audio e un altro quando viene arrestato.

## <a name="time-stamp"></a>Timestamp

La variabile timeStamp riflette l'ora corrente in cui viene creato lo snapshot. Può essere usato per misurare la frequenza di creazione degli snapshot.

È possibile usare questa variabile per impostare il tempo delle animazioni. Se gli snapshot sono troppo frequenti, è possibile ridurre normalmente l'immagine per visualizzarla nel modo scelto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del rendering**](implementing-render.md)
</dt> </dl>

 

 




