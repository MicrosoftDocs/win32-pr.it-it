---
description: VSS è progettato per risolvere i problemi descritti nei problemi comuni di backup del volume.
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: Modello VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307188"
---
# <a name="the-vss-model"></a>Modello VSS

VSS è progettato per risolvere i problemi descritti nei [problemi comuni di backup del volume](common-volume-backup-issues.md).

Il modello VSS include quanto segue:

-   Meccanismo di copia shadow. VSS offre un'acquisizione rapida del volume dello stato di un disco in un istante nel tempo, ovvero una [*Copia Shadow*](vssgloss-s.md) del volume. Questa copia del volume esiste side-by-side con il volume Live e contiene copie di tutti i file su disco salvati e disponibili come dispositivo separato.
-   Stato del file coerente tramite il coordinamento delle applicazioni. VSS fornisce un meccanismo di comunicazione tra processi basato su COM e basato su eventi che può essere utilizzato dai processi partecipanti per determinare lo stato del sistema in relazione alle operazioni di backup, ripristino e copia shadow (acquisizione volume). Questi eventi definiscono le fasi in base alle quali le applicazioni che modificano i dati su disco ([*writer*](vssgloss-w.md)) possono riportare tutti i file in uno stato coerente prima della creazione della copia shadow.
-   Riduzione del tempo di inattività dell'applicazione. La copia shadow VSS esiste in parallelo con una copia in tempo reale del volume di cui eseguire il backup, ad eccezione del breve periodo di preparazione e creazione della copia shadow, un'applicazione può continuare a funzionare. Il tempo necessario per creare effettivamente una copia shadow, che si verifica tra gli eventi [*Freeze*](vssgloss-f.md) e [*scongela*](vssgloss-t.md) , richiede in genere circa un minuto.

    Sebbene la preparazione di un writer per una copia shadow, incluso lo scaricamento di I/O e il salvataggio dello stato (vedere [Panoramica delle attività di pre-backup](overview-of-pre-backup-tasks.md)), possa essere non banale, è molto più breve del tempo necessario per eseguire effettivamente il backup di un volume, che per volumi di grandi dimensioni può richiedere ore.

-   Interfaccia unificata per VSS. VSS estrae i meccanismi di copia shadow all'interno di un'interfaccia comune, consentendo a un fornitore di hardware di aggiungere e gestire le funzionalità univoche dei propri provider. Qualsiasi applicazione di backup ([*richiedente*](vssgloss-r.md)) e qualsiasi writer deve essere in grado di essere eseguita su qualsiasi sistema di archiviazione su disco che supporta l'interfaccia VSS.
-   Backup multivolume. VSS supporta [*set*](vssgloss-s.md)di copie shadow, ovvero raccolte di copie shadow, su più tipi di volumi di dischi di più fornitori. Tutte le copie shadow in un set di copie shadow verranno create con lo stesso timestamp e presenteranno lo stesso stato del disco per uno stato del disco multivolume.
-   Supporto per copie shadow native. A partire da Windows XP, il supporto per le copie shadow è disponibile tramite VSS come parte nativa del sistema operativo Windows. Fino a quando in un sistema è presente almeno un disco NTFS, questi sistemi possono essere configurati in modo da supportare copie shadow di tutti i sistemi disco montati su di essi.

 

 



