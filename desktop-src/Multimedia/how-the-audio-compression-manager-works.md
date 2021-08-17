---
title: Funzionamento di Gestione compressione audio
description: Funzionamento di Gestione compressione audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimediale, gestione compressione audio
- audio, gestione compressione audio (ACM)
- gestione compressione audio,informazioni
- ACM (audio compression manager),about
- gestione compressione audio,driver codec
- ACM (Audio Compression Manager),driver codec
- gestione compressione audio,driver convertitore di formati
- ACM (Audio Compression Manager),driver convertitore di formati
- gestione compressione audio,driver di filtro
- ACM (Gestione compressione audio),driver di filtro
- gestione compressione audio(ACM, Audio Compression Manager), driver di driver
- ACM (audio compression manager),driver driver
- gestione compressione audio,driver decompressore
- ACM (Audio Compression Manager),driver decompressore
- driver codec
- driver del convertitore di formati
- driver di filtro
- driver di tutto il sistema
- driver decompressore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb3d94feee3da290bf9c1cc90cab92f2aade083effd8a01cb17906c22e0f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140998"
---
# <a name="how-the-audio-compression-manager-works"></a>Funzionamento di Gestione compressione audio

ACM usa hook di interfaccia driver esistenti per eseguire l'override dell'algoritmo di mapping predefinito per i dispositivi audio waveform. Ciò consente ad ACM di intercettare le chiamate aperte dal dispositivo. Dopo l'intercettazione di una chiamata, ACM può eseguire una serie di attività per elaborare i dati audio, ad esempio l'inserimento di un dispositivo esterno o un decompressore nella sequenza.

ACM gestisce i tipi di driver seguenti:

-   Driver Dispressore e decompressore (codec)
-   Driver del convertitore di formati
-   Filtrare i driver

I tipi di formato e i decompressori cambiano in un altro. Ad esempio, unprimere o un decompressore può modificare un file PCM (Pulse Code Modulation) in un file ADPCM (Adaptive Differential Pulse Code Modulation). I convertitori di formato modificano il formato, ma non il tipo di dati. Ad esempio, un convertitore può modificare i dati a 44 kHz, a 16 bit in dati a 44 kHz e a 8 bit. I filtri non modificano affatto il formato dei dati, ma modificano in qualche modo i dati audio della forma d'onda. Ad esempio, un filtro può combinare un flusso di dati e un'eco di se stesso. Un singolo driver ACM, o un tag di filtro o di formato all'interno di un driver, potrebbe supportare anche combinazioni dei tipi precedenti.

Per l'output audio-waveform, ACM passa ogni buffer di dati al convertitore non appena arriva. Il convertitore decomprime i dati e restituisce i dati decompressi all'ACM in un buffer "shadow". ACM passa quindi il buffer ombreggiatura decompresso al driver audio waveform. ACM alloca i buffer shadow ogni volta che riceve un messaggio di preparazione.

Per l'input audio waveform, ACM passa buffer ombreggiati vuoti al driver. Usa un'attività in background per ricevere una notifica dopo che il driver ha riempito il buffer ombreggiatura. ACM passa quindi i buffer al driver per la compressione. Al termine della compressione, il driver passa i dati all'applicazione.

 

 




