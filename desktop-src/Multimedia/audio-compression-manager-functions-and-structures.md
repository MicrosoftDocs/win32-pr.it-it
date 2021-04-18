---
title: Funzioni e strutture di Gestione compressione audio
description: Funzioni e strutture di Gestione compressione audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimediale, funzioni ACM
- audio, funzioni ACM
- Gestione compressione audio (ACM), funzioni
- ACM (Gestione compressione audio), funzioni
- audio multimediale, strutture ACM
- audio, strutture ACM
- Gestione compressione audio (ACM), strutture
- ACM (Gestione compressione audio), strutture
- Strutture di ACM
- Funzioni ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299628"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funzioni e strutture di Gestione compressione audio

Le funzioni ACM rientrano in diverse categorie. Le convenzioni di denominazione per le funzioni facilitano l'identificazione di queste categorie. I nomi delle funzioni (con due eccezioni) sono nel formato *acmGroupFunction*, dove *Group* designa la categoria ACM (ad esempio "driver", "Format", "FormatTag", "Filter", "FilterTag" o "Stream") e *Function* descrive l'azione eseguita dalla funzione.

Le funzioni nei gruppi di filtro e di formato sono molto simili. Quasi tutte le funzioni che agiscono sui filtri hanno una funzione parallela che agisce sui formati.

Nel gruppo Format alcune funzioni usano tag di formato Waveform-Audio (il membro **wFormatTag** di una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), mentre altri richiedono formati audio completi per la forma d'onda (la struttura **WAVEFORMATEX** completa). Per informazioni di riferimento sulla struttura **WAVEFORMATEX** , vedere [Error](error.md).

Nel gruppo di filtri alcune funzioni usano i tag del filtro per la forma d'onda-audio (il membro **dwFilterTag** di una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), mentre altri richiedono filtri audio e di forma d'onda completi (la struttura **WAVEFILTER** completa).

Le funzioni del gruppo Stream rappresentano i molti passaggi necessari per una conversione: l'apertura di un'istanza di conversione, la preparazione per la conversione, la conversione, la pulizia al termine della conversione e la chiusura dell'istanza di conversione.

 

 