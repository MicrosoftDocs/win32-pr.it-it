---
title: Chiave Mappe
description: Chiave Mappe
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Instrument Digital Interface (MIDI), MIDI Mapper
- MIDI (Instrument Digital Interface), MIDI Mapper
- MIDI Mapper, mappe delle chiavi
- mappe delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72197de28a6596efa951b302f0ca351ac187532cd28d431cf1d954b53d841064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140225"
---
# <a name="key-maps"></a>Chiave Mappe

A ogni voce della tabella di conversione della mappa patch può essere associata una mappa delle chiavi. Le mappe delle chiavi influiscono sui messaggi note-on, note-off e polyfoneic-key-aftertouch. Una mappa delle chiavi ha una tabella di conversione con una voce per ognuno dei 128 valori di chiave MIDI. Ad esempio, se la voce per il valore chiave 60 è 72, midi mapper modifica i messaggi di nota MIDI come illustrato nella figura seguente.

![immagine midi mapper](images/mmap-a06.gif)

Le mappe delle chiavi sono utili con i sintetizzatori che hanno strumenti di misura basati su chiavi con un particolare suono acustico a ogni chiave. Le mappe delle chiavi vengono in genere assegnate alla prima patch nelle mappe patch sui canali delle chiavi (10 e 16).

 

 




