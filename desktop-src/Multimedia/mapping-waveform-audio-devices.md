---
title: Mapping di dispositivi Waveform-Audio
description: Mapping di dispositivi Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimediale, mapping della forma d'onda-dispositivi audio
- audio, mapping della forma d'onda-dispositivi audio
- Gestione compressione audio (ACM), mapping di forme d'onda-dispositivi audio
- ACM (Gestione compressione audio), mapping di forme d'onda-dispositivi audio
- mapping della forma d'onda-dispositivi audio
- audio multimediale, Mapper
- audio, Mapper
- Gestione compressione audio (ACM), Mapper
- ACM (Gestione compressione audio), Mapper
- mapper
- audio Waveform, mapping dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855862"
---
# <a name="mapping-waveform-audio-devices"></a>Mapping di dispositivi Waveform-Audio

Windows fornisce un set di funzioni standard per i dispositivi audio. Queste funzioni rilasciano chiamate ai driver di dispositivo che gestiscono i dispositivi hardware. Il sistema usa un modulo denominato "Mapper" per gestire i dispositivi installati. Il Mapper utilizza hook speciali nell'interfaccia del driver per intercettare le chiamate e fungere da intermediario tra il sistema e i driver installati nel sistema. Il Mapper è responsabile della corrispondenza delle richieste di un'applicazione per l'accesso a un dispositivo con i dispositivi disponibili e per la ricerca di un dispositivo che soddisfi i requisiti audio dell'applicazione corrente. Il sistema fornisce Mapper per i tipi di driver standard: Waveform-Audio, MIDI (Musical Instrument Digital Interface) e dispositivi ausiliari.

ACM è un'estensione del sistema multimediale di base e viene installato come Mapper. Questo significa che ACM usa i hook del mapper dell'interfaccia del driver per i dispositivi audio e della forma d'onda. L'uso di questi hook consente all'ACM di decodificare o codificare i dati dell'audio della forma d'onda prima di passarli a o da un driver di dispositivo Waveform-Audio. La differenza tra l'ACM e il mapper di sistema standard consiste nel fatto che l'ACM può cercare un dispositivo audio Waveform che supporta un formato specificato o trovare una combinazione di un dispositivo audio e di una forma d'onda, un compressore o un decompressore ACM che supporti un formato specificato.

Quando un'applicazione richiede che il sistema apra un dispositivo audio waveform per l'input o l'output, la richiesta specifica il formato e il dispositivo. Quando il dispositivo specificato è il Mapper, è necessario che il mapper trovi un dispositivo che supporta il formato specificato. Il mapper implementato in ACM Cerca un dispositivo audio Waveform installato che supporta il formato specificato. Se l'ACM non riesce a trovare un dispositivo di questo tipo, Cerca un dispositivo audio e una forma d'onda, un compressore o un decompressore che insieme supporti il formato. In particolare, l'ACM Cerca un compressore o un decompressore che converte il formato specificato in un formato supportato da un dispositivo audio e una forma d'onda installata. Dopo che l'ACM ha individuato un dispositivo che supporta il formato convertito, può rispettare le richieste di riproduzione o registrazione del formato originariamente richiesto, anche se non è supportato direttamente da un dispositivo wave-audio installato.

Oltre alla conversione del formato, ACM offre anche servizi per supportare la compressione, la decompressione, il filtraggio, la selezione del formato e la selezione dei filtri. Fornisce un'API standard che supporta chiamando i relativi driver.

 

 




