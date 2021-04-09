---
title: Creazione di file MIDI
description: Creazione di file MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Multimedia di Windows, creazione di file MIDI
- Multimedia, creazione di file MIDI
- audio multimediale, creazione di file MIDI
- audio, creazione di file MIDI
- MIDI (Musical Instrument Digital Interface), creazione di file
- MIDI (Musical Instrument Digital Interface), creazione di file
- creazione di file MIDI, informazioni
- Associazione MIDI Manufacturers (MMA)
- MMA (associazione MIDI Manufacturers)
- Specifica MIDI dettagliata
- Specifica dei file MIDI standard
- Specifica MIDI (GM) generale
- Specifica GM (MIDI generale)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044434"
---
# <a name="creating-midi-files"></a>Creazione di file MIDI

Le specifiche MIDI (Musical Instrument Digital Interface) sono pubblicate da e sono materiale protetto da copyright di MIDI Manufacturers Association (MMA). Nell'elenco seguente vengono descritte le specifiche che hanno il maggior interesse generale:

## <a name="midi-detailed-specification"></a>Specifica MIDI dettagliata

La specifica MIDI descrive i protocolli hardware e software MIDI. Questa operazione è utile per gli utenti che sviluppano applicazioni multimediali che implementano il supporto MIDI usando funzioni MIDI per registrare, modificare e/o riprodurre dati MIDI.

## <a name="standard-midi-files-10"></a>File MIDI standard 1,0

La specifica dei file MIDI standard definisce un modo per interscambiare i dati MIDI con timestamp tra applicazioni diverse su piattaforme hardware identiche o diverse. Questa operazione è utile per gli sviluppatori che scrivono applicazioni che leggono e analizzano i file su disco contenenti dati MIDI e/o scrivono file di dati MIDI su disco.

## <a name="general-midi-system---level-1"></a>Sistema MIDI generale di livello 1

La specifica generale MIDI (GM) definisce una configurazione MIDI minima di un "sistema MIDI generale". Questo sistema è costituito da una classe specifica di dispositivi di riproduzione MIDI ed è di particolare interesse per gli sviluppatori di contenuti multimediali che creano file MIDI. La maggior parte delle schede audio e dei sintetizzatori MIDI del PC prodotti attualmente sono compatibili con la specifica GM. I file MIDI che vengono creati nella specifica GM dovrebbero in genere suonare come se fossero progettati per il suono, indipendentemente dal dispositivo compatibile con GM su cui sono stati riprodotti.

Per consentire ai file MIDI di essere un formato valido per rappresentare la musica nell'elaborazione multimediale, Windows segue la specifica generale MIDI System Level 1. Negli argomenti seguenti vengono fornite linee guida per la creazione di MIDI aggiuntive:

-   [Linee guida per la creazione di file MIDI](authoring-guidelines-for-midi-files.md)
-   [Assegnazioni di patch MIDI standard](standard-midi-patch-assignments.md)
-   [Assegnazioni di chiavi MIDI standard](standard-midi-key-assignments.md)

 

 




