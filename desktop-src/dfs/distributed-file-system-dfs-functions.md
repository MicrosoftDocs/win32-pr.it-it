---
title: funzioni file system distribuito (DFS)
description: Le file system distribuito (DFS) consentono di raggruppare in modo logico le condivisioni in più server e di collegare in modo trasparente le condivisioni in un singolo spazio dei nomi gerarchico. DFS organizza le risorse condivise in una rete in una struttura ad albero.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898d44ecfaeb99145570230e49156440dc9e2aac02051baa47bb496a0f58b2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380581"
---
# <a name="distributed-file-system-dfs-functions"></a>funzioni file system distribuito (DFS)

Le file system distribuito (DFS) consentono di raggruppare in modo logico le condivisioni in più server e di collegare in modo trasparente le condivisioni in un singolo spazio dei nomi gerarchico. DFS organizza le risorse condivise in una rete in una struttura ad albero.

DFS supporta spazi *dei* nomi DFS autonomi, quelli  con un server host e spazi dei nomi basati su dominio con più server host e disponibilità elevata. I dati della topologia DFS *per* gli spazi dei nomi basati su dominio vengono archiviati in Active Directory. I dati includono la radice DFS, i collegamenti DFS e le destinazioni DFS.

Ogni struttura ad albero DFS ha una o più *destinazioni radice.* La destinazione radice è un server host che esegue il servizio DFS. Una struttura ad albero DFS può contenere uno o più *collegamenti DFS.* Ogni collegamento DFS punta a una o più cartelle condivise nella rete. È possibile aggiungere, modificare ed eliminare collegamenti DFS da uno spazio dei nomi DFS. Quando si rimuove l'ultima destinazione associata a un collegamento DFS, DFS elimina il collegamento DFS nello spazio dei nomi DFS. Nella documentazione precedente i collegamenti DFS erano denominati punti di giunzione.

Un collegamento DFS può puntare a una o più cartelle condivise. Le cartelle sono denominate *destinazioni*. Quando gli utenti accedono a un collegamento DFS, il server DFS seleziona un set di destinazioni in base alle informazioni del sito di un client. Il client accede alla prima destinazione disponibile nel set. Ciò consente di distribuire le richieste client tra le possibili destinazioni e può offrire agli utenti un'accessibilità continua anche in caso di errore di alcuni server.

Un'applicazione può usare le funzioni DFS per:

- Aggiungere un collegamento DFS a una radice DFS.
- Creare o rimuovere spazi dei nomi DFS autonomi e basati su dominio.
- Aggiungere destinazioni a un collegamento DFS esistente.
- Rimuovere un collegamento DFS da una radice DFS.
- Rimuovere una destinazione da un collegamento DFS.
- Consente di visualizzare e configurare informazioni sulle radici DFS e sui collegamenti.

Per un elenco delle funzioni DFS, vedere File system distribuito [Functions](distributed-file-system-functions.md).

Per un elenco delle strutture DFS, vedere file system distribuito [strutture](distributed-file-system-structures.md).

Le destinazioni nei computer che eseguono Microsoft Windows possono essere pubblicate in uno spazio dei nomi DFS. È anche possibile pubblicare qualsiasi condivisione non Microsoft per cui i redirector client sono disponibili in uno spazio dei nomi DFS. Tuttavia, a differenza di una condivisione pubblicata in un server che esegue Windows Server, non può ospitare una radice DFS o fornire riferimenti ad altre destinazioni DFS.

DFS usa il servizio replica Windows server per copiare le modifiche tra destinazioni replicate. Gli utenti possono modificare i file archiviati in una destinazione e il servizio replica file propaga le modifiche alle altre destinazioni designate. Il servizio mantiene la modifica più recente apportata a uno o più documenti.
