---
title: Mapping Waveform-Audio dispositivi
description: Mapping Waveform-Audio dispositivi
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimediale, mapping di dispositivi waveform-audio
- audio, mapping di dispositivi waveform-audio
- gestione compressione audio(ACM), mapping di dispositivi waveform-audio
- ACM (gestione compressione audio), mapping di dispositivi waveform-audio
- mapping di dispositivi waveform-audio
- audio multimediale, mapper
- audio, mapper
- gestione compressione audio(ACM), mapper
- ACM (gestione compressione audio), mapper
- mapper
- audio waveform, mapping dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4204a79eebd5fed3c8f96712aa3cd83c50056b1c194bafe2ce485a5b4b68f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138772"
---
# <a name="mapping-waveform-audio-devices"></a>Mapping Waveform-Audio dispositivi

Windows fornisce un set di funzioni standard per i dispositivi audio. Queste funzioni emettere chiamate ai driver di dispositivo che gestiscono i dispositivi hardware. Il sistema usa un modulo denominato "mapper" per gestire i dispositivi installati. Il mapper usa hook speciali nell'interfaccia del driver per intercettare le chiamate e fungere da intermediario tra il sistema e i driver installati nel sistema. Il mapper è responsabile della corrispondenza delle richieste di accesso di un'applicazione a un dispositivo con i dispositivi disponibili e della ricerca di un dispositivo che soddisfi i requisiti audio dell'applicazione corrente. Il sistema fornisce mapper per i tipi di driver standard: waveform-audio, MIDI (Musical Instrument Digital Interface) e dispositivi ausiliari.

ACM è un'estensione del sistema multimediale di base e viene installato come mapper. Ciò significa che ACM usa gli hook del mapper dell'interfaccia driver per i dispositivi waveform-audio. L'uso di questi hook consente a ACM di decodificare o codificare i dati audio della forma d'onda prima di passarlo a o da un driver di dispositivo waveform-audio. La differenza tra ACM e il mapper di sistema standard è che ACM può cercare un dispositivo audio-forma d'onda che supporti un formato specificato o trovare una combinazione di un dispositivo waveform-audio e un dispositivo di compressione o decompressore ACM che supporta un formato specificato.

Quando un'applicazione richiede al sistema di aprire un dispositivo waveform-audio per l'input o l'output, la richiesta specifica il formato e il dispositivo. Quando il dispositivo specificato è il mapper, il mapper deve trovare un dispositivo che supporta il formato specificato. Il mapper implementato in ACM cerca un dispositivo waveform-audio installato che supporta il formato specificato. Se ACM non riesce a trovare un dispositivo di questo tipo, cerca un dispositivo waveform-audio e un dispositivo di compressione o decompressore che insieme supportano il formato. In particolare, ACM cerca un compressore o un decompressore che converte il formato specificato in un formato supportato da un dispositivo waveform-audio installato. Dopo aver individuato un dispositivo che supporta il formato convertito, ACM può rispettare le richieste di riproduzione o registrazione del formato originariamente richiesto, anche se nessun dispositivo waveform-audio installato supporta direttamente tale formato.

Oltre alla conversione del formato, ACM offre anche servizi per supportare la compressione, la decompressione, il filtro, la selezione del formato e la selezione dei filtri. Fornisce un'API standard che supporta chiamando i propri driver.

 

 




