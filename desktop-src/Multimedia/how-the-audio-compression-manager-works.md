---
title: Funzionamento di Gestione compressione audio
description: Funzionamento di Gestione compressione audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimediale, Gestione compressione audio (ACM)
- audio, Gestione compressione audio (ACM)
- Gestione compressione audio (ACM), informazioni
- ACM (Gestione compressione audio), informazioni
- Gestione compressione audio (ACM), driver di codec
- ACM (Gestione compressione audio), driver di codec
- Gestione compressione audio (ACM), driver del convertitore di formato
- ACM (Gestione compressione audio), driver del convertitore di formato
- Gestione compressione audio (ACM), driver di filtro
- ACM (Gestione compressione audio), driver di filtro
- Gestione compressione audio (ACM), driver compressore
- ACM (Gestione compressione audio), driver del compressore
- Gestione compressione audio (ACM), driver di decompressione
- ACM (Gestione compressione audio), driver di decompressione
- driver di codec
- driver del convertitore di formato
- filtrare i driver
- driver compressore
- driver di decompressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330599"
---
# <a name="how-the-audio-compression-manager-works"></a>Funzionamento di Gestione compressione audio

L'ACM utilizza gli hook di interfaccia del driver esistenti per eseguire l'override dell'algoritmo di mapping predefinito per i dispositivi audio waveform. In questo modo, l'ACM può intercettare le chiamate a dispositivi aperti. Dopo l'intercettazione di una chiamata, l'ACM può eseguire una serie di attività per elaborare i dati audio, ad esempio l'inserimento di un compressore esterno o un decompressore nella sequenza.

L'ACM gestisce i tipi di driver seguenti:

-   Driver Compressor e decompressore (codec)
-   Driver del convertitore di formato
-   Filtrare i driver

I commutatori e i decompressori cambiano un tipo di formato in un altro. Ad esempio, un commutatore o un decompressore può modificare un file PCM (Pulse Code Modulation) in un file ADPCM (modulazione del codice Pulse differenziale). I convertitori di formato cambiano il formato, ma non il tipo di dati. Un convertitore può, ad esempio, modificare i dati 44-kHz, a 16 bit a 44-kHz, a 8 bit. I filtri non modificano affatto il formato dati, ma cambiano in qualche modo i dati dell'audio della forma d'onda. Un filtro può ad esempio combinare un flusso di dati e un echo di se stesso. Un driver ACM singolo, o un tag di filtro o di formato all'interno di un driver, potrebbe supportare anche combinazioni dei tipi precedenti.

Per l'output dell'audio della forma d'onda, l'ACM passa ogni buffer di dati al convertitore mentre arriva. Il convertitore decomprime i dati e restituisce i dati decompressi in ACM in un buffer "Shadow". Il modulo ACM passa quindi il buffer di ombreggiatura decompresso al driver audio della forma d'onda. L'ACM alloca i buffer Shadow ogni volta che viene ricevuto un messaggio di preparazione.

Per l'input audio della forma d'onda, l'ACM passa i buffer di ombreggiatura vuoti al driver. Usa un'attività in background per ricevere una notifica dopo che il driver ha riempito il buffer di ombreggiatura. L'ACM passa quindi i buffer al driver per la compressione. Al termine della compressione, il driver passa i dati all'applicazione.

 

 




