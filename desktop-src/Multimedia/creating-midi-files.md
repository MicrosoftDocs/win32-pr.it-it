---
title: Creazione di file MIDI
description: Creazione di file MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows multimediali, creazione di file MIDI
- multimediali, creazione di file MIDI
- audio multimediale, creazione di file MIDI
- audio, creazione di file MIDI
- Instrument Digital Interface (MIDI), creazione di file
- MIDI (Instrument Digital Interface), creazione di file
- creazione di file MIDI, informazioni
- MIDI Manufacturers Association (MMA)
- MMA (MIDI Manufacturers Association)
- SPECIFICA MIDI dettagliata
- Specifica dei file MIDI standard
- Specifica GENERALE MIDI (GM)
- Specifica GM (General MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e2a229a8e9208645fa7ffae296c004b833156b240f063066be2a8732175054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144610"
---
# <a name="creating-midi-files"></a>Creazione di file MIDI

Le specifiche midi (Digital Interface) di Digital Instrument (MIDI) sono pubblicate da e sono materiale protetto da copyright della MIDI Manufacturers Association (MMA). L'elenco seguente descrive le specifiche di maggiore interesse generale:

## <a name="midi-detailed-specification"></a>Specifica dettagliata MIDI

MidI Detailed Specification (Specifica dettagliata MIDI) illustra i protocolli hardware e software MIDI. Ciò è utile per gli utenti che sviluppano applicazioni multimediali che implementano il supporto MIDI usando le funzioni MIDI per registrare, modificare e/o riprodurre dati MIDI.

## <a name="standard-midi-files-10"></a>File MIDI standard 1.0

La specifica Standard MIDI Files definisce un modo per interscambiare dati MIDI con timestamp tra applicazioni diverse nella stessa piattaforma hardware o in piattaforme hardware diverse. Ciò è utile per gli sviluppatori che scrivono applicazioni che leggono e analizzano file su disco contenenti dati MIDI e/o scrivono file di dati MIDI su disco.

## <a name="general-midi-system---level-1"></a>Sistema MIDI generale - Livello 1

La specifica MIDI generale definisce una configurazione MIDI minima di un "sistema MIDI generale". Questo sistema è costituito da una classe specifica di dispositivi di riproduzione MIDI ed è di interesse per gli sviluppatori di contenuti multimediali che sistono nella creazione di file MIDI. La maggior parte delle schede audio PC e dei sintetizzatori MIDI prodotti oggi è compatibile con la specifica GM. I file MIDI creati in base alla specifica GM dovrebbero in genere sembrare come previsto, indipendentemente dal dispositivo compatibile con GM su cui vengono riprodotti.

Per consentire ai file MIDI di essere un formato valido per la rappresentazione di musica nel computing multimediale, Windows la specifica generale MIDI System Level 1. Gli argomenti seguenti forniscono linee guida aggiuntive per la creazione midi:

-   [Linee guida per la creazione di file MIDI](authoring-guidelines-for-midi-files.md)
-   [Assegnazioni di patch MIDI standard](standard-midi-patch-assignments.md)
-   [Assegnazioni di chiavi MIDI standard](standard-midi-key-assignments.md)

 

 




