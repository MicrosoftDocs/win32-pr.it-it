---
title: Funzionamento dell'esempio Echo
description: Funzionamento dell'esempio Echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Windows Media Player plug-in, panoramica dell'esempio Echo
- plug-in, panoramica dell'esempio Echo
- plug-in di elaborazione del segnale digitale,Panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290cb56bbf1900dbcc09874213490f80cdc3af179ff243a2867bb232c3bb85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338956"
---
# <a name="how-the-echo-sample-works"></a>Funzionamento dell'esempio Echo

Il codice crea l'effetto echo allocando un buffer sufficientemente grande da contenere esattamente la quantità di dati audio di cui è possibile eseguire il rendering nell'intervallo di tempo specificato dal valore di tempo di ritardo. Le dimensioni del buffer vengono calcolate, in byte, dalla formula seguente:

dimensioni del buffer = frequenza \* di campionamento del tempo di ritardo/allineamento del blocco 1000 \*

Il tempo di ritardo è espresso in millisecondi. La frequenza di campionamento e i valori di allineamento dei blocchi sono specificati in una struttura WAVEFORMATEX. La frequenza di campionamento è in campioni al secondo. dividendo per 1000 produce campioni al millisecondo. L'allineamento dei blocchi è uguale al prodotto del numero di canali (1 per mono, 2 per stereo) e del numero di bit per campione (8 o 16) divisi per 8 (bit per byte).

Oltre alla variabile puntatore che punta all'inizio del buffer di ritardo, il codice crea un puntatore mobile che scorre i dati nel buffer in sincronizzazione con il ciclo di elaborazione nella funzione **DoProcessOutput.** Quando il puntatore mobile raggiunge la fine del buffer di ritardo, torna alla parte superiore del buffer. Un buffer usato in questo modo è detto buffer circolare.

Una volta che il buffer di ritardo esiste e Windows Media Player ha allocato un buffer di input per fornire dati audio e un buffer di output per ricevere i dati audio elaborati, l'elaborazione echo procede come questa:

1.  Immettere un ciclo che consenta l'elaborazione di ogni campione audio nel buffer di input.
2.  Recuperare un esempio dal buffer di input. Spostare quindi il puntatore del buffer di input in avanti all'esempio successivo per preparare l'iterazione del ciclo successiva.
3.  Recuperare un campione dal buffer di ritardo.
4.  Copiare l'esempio dal buffer di input nella stessa posizione nel buffer di ritardo da cui è stato recuperato l'ultimo esempio di ritardo.
5.  Spostare il puntatore del buffer di ritardo in avanti all'esempio successivo. Se il puntatore si sposta oltre la fine del buffer, spostarlo nella parte superiore del buffer.
6.  Combinare l'esempio dal buffer di input con l'esempio del buffer di ritardo.
7.  Copiare il risultato nel buffer di output. Spostare quindi il puntatore del buffer di output in avanti nell'unità successiva per preparare l'iterazione del ciclo successiva.
8.  Ripetere l'operazione fino a quando non vengono elaborati tutti gli esempi.

Quando un esempio di input recuperato nel passaggio 2 viene copiato nel buffer di ritardo nel passaggio 4, rimane in questa posizione fino a quando il puntatore mobile non passa attraverso ogni campione nel buffer di ritardo e infine torna alla stessa posizione. Poiché le dimensioni del buffer di ritardo sono progettate per corrispondere al tempo di ritardo, il tempo trascorso tra il campione copiato nel buffer di ritardo e il campione recuperato ancora una volta equivale al ritardo specificato (più qualsiasi latenza introdotta dall'elaborazione effettiva).

All'avvio di un flusso, non vengono generati dati di ritardo fino a quando non è trascorso il tempo di ritardo. Pertanto, è importante che il buffer di ritardo contenga inizialmente il silenzio. Se il buffer di ritardo contiene dati casuali, l'utente sentirà un rumore bianco finché il plug-in non genera dati di ritardo sufficienti per sovrascrivere l'intero buffer di ritardo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'esempio Echo**](echo-sample-overview.md)
</dt> </dl>

 

 




