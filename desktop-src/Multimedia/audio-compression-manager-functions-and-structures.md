---
title: Funzioni e strutture di Gestione compressione audio
description: Funzioni e strutture di Gestione compressione audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimediale, funzioni ACM
- audio, funzioni ACM
- gestione compressione audio(ACM), funzioni
- ACM (gestione compressione audio),funzioni
- audio multimediale, strutture ACM
- audio, strutture ACM
- gestione compressione audio(ACM), strutture
- ACM (gestione compressione audio),strutture
- Strutture di ACM
- Funzioni di ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd9a66bee13c02c87df95565744eb973283baedb7e955449feb2ddad3005a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808381"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funzioni e strutture di Gestione compressione audio

Le funzioni ACM rientrano in diverse categorie. Le convenzioni di denominazione per le funzioni semplificano l'identificazione di queste categorie. I nomi delle funzioni (con due eccezioni) hanno il formato *acmGroupFunction*, dove *Group* definisce la categoria ACM (ad esempio "Driver", "Format", "FormatTag", "Filter", "FilterTag" o "Stream") e *Function* descrive l'azione eseguita dalla funzione.

Le funzioni nei gruppi di filtri e di formato sono molto simili. Quasi ogni funzione che agisce sui filtri ha una funzione parallela che agisce sui formati.

Nel gruppo di formati alcune funzioni usano tag di formato waveform-audio (il membro **wFormatTag** di una struttura [**WAVEFORMATEX),**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) mentre altre richiedono formati audio-forma d'onda completi (la struttura **WAVEFORMATEX** completa). Per informazioni di riferimento sulla **struttura WAVEFORMATEX,** vedere [Errore](error.md).

Nel gruppo di filtri alcune funzioni usano tag di filtro waveform-audio (membro **dwFilterTag** di una struttura [**WAVEFILTER),**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) mentre altre richiedono filtri audio-forma d'onda completi (la struttura **WAVEFILTER** completa).

Le funzioni nel gruppo di flussi rappresentano i numerosi passaggi necessari per una conversione: apertura di un'istanza di conversione, preparazione per la conversione, esecuzione della conversione, pulizia al termine della conversione e chiusura dell'istanza di conversione.

 

 