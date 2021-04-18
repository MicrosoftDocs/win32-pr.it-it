---
title: Funzionamento del campione Echo
description: Funzionamento del campione Echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Plug-in di Windows Media Player, panoramica dell'esempio Echo
- plug-in, Panoramica di esempio Echo
- plug-in di elaborazione dei segnali digitali, panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298351"
---
# <a name="how-the-echo-sample-works"></a>Funzionamento del campione Echo

Il codice crea l'effetto Echo allocando un buffer sufficientemente grande da contenere esattamente la quantità di dati audio di cui è possibile eseguire il rendering nell'intervallo di tempo specificato dal valore di tempo di ritardo. La dimensione del buffer viene calcolata in byte dalla formula seguente:

dimensioni del buffer = frequenza di campionamento del tempo di attesa \* / \* allineamento del blocco 1000

Il tempo di ritardo è in millisecondi. I valori di frequenza di campionamento e allineamento blocchi sono forniti in una struttura WAVEFORMATEX. La frequenza di campionamento è in campioni al secondo; la divisione per 1000 restituisce campioni per millisecondo. L'allineamento a blocchi è uguale al prodotto del numero di canali (1 per mono, 2 per stereo) e al numero di bit per campione (8 o 16) diviso per 8 (bit per byte).

Oltre alla variabile puntatore che punta all'inizio del buffer di ritardo, il codice crea un puntatore mobile che scorre i dati nel buffer in sincronizzazione con il ciclo di elaborazione nella funzione **DoProcessOutput** . Quando il puntatore mobile raggiunge la fine del buffer di ritardo, viene spostato di nuovo all'inizio del buffer. Un buffer utilizzato in questo modo è denominato buffer circolare.

Una volta che il buffer di ritardo esiste e Windows Media Player ha allocato un buffer di input per fornire dati audio e un buffer di output per la ricezione di dati audio elaborati, l'elaborazione ECHO procede come segue:

1.  Immettere un ciclo che consente l'elaborazione di ogni esempio audio nel buffer di input.
2.  Recuperare un campione dal buffer di input. Spostare quindi il puntatore del buffer di input in avanti nell'esempio successivo per prepararsi alla successiva iterazione del ciclo.
3.  Recuperare un campione dal buffer di ritardo.
4.  Copiare l'esempio dal buffer di input nella stessa posizione del buffer di ritardo dal quale è stato recuperato l'ultimo campione di ritardo.
5.  Spostare il puntatore del buffer di ritardo in avanti nell'esempio successivo. Se il puntatore viene spostato oltre la fine del buffer, spostarlo all'inizio del buffer.
6.  Combinare l'esempio dal buffer di input con l'esempio dal buffer di ritardo.
7.  Copiare il risultato nel buffer di output. Spostare quindi il puntatore del buffer di output all'unità successiva per prepararsi alla successiva iterazione del ciclo.
8.  Ripetere l'elaborazione fino a quando non vengono elaborati tutti gli esempi.

Quando un esempio di input recuperato nel passaggio 2 viene copiato nel buffer di ritardo nel passaggio 4, rimane disponibile fino a quando il puntatore mobile passa attraverso ogni campione nel buffer di ritardo e infine torna alla stessa posizione. Poiché la dimensione del buffer di ritardo è progettata per corrispondere al ritardo, il tempo trascorso tra l'esempio copiato nel buffer di ritardo e l'esempio recuperato ancora una volta equivale al ritardo specificato (più qualsiasi latenza introdotta dall'elaborazione effettiva).

Quando viene avviato un flusso, non vengono generati dati di ritardo fino a quando non è trascorso il tempo di ritardo. Pertanto, è importante che il buffer di ritardo includa inizialmente il silenzio. Se il buffer di ritardo contiene dati casuali, l'utente riceverà un rumore bianco fino a quando il plug-in genera un numero sufficiente di dati di ritardo per sovrascrivere l'intero buffer di ritardo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'esempio Echo**](echo-sample-overview.md)
</dt> </dl>

 

 




