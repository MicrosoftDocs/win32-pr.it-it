---
title: Funzioni file system distribuito (DFS)
description: Le funzioni file system distribuito (DFS) offrono la possibilità di raggruppare in modo logico le condivisioni su più server e di collegare in modo trasparente le condivisioni in un singolo spazio dei nomi gerarchico. DFS organizza le risorse condivise in una rete in una struttura treelike.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73738d4f503d10e7668f0f323583f49604e3a90d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225752"
---
# <a name="distributed-file-system-dfs-functions"></a>Funzioni file system distribuito (DFS)

Le funzioni file system distribuito (DFS) offrono la possibilità di raggruppare in modo logico le condivisioni su più server e di collegare in modo trasparente le condivisioni in un singolo spazio dei nomi gerarchico. DFS organizza le risorse condivise in una rete in una struttura treelike.

DFS supporta spazi dei nomi DFS *autonomi,* quelli con un server host e spazi dei nomi *basati su dominio* con più server host e disponibilità elevata. I *dati della topologia* DFS per gli spazi dei nomi basati su dominio vengono archiviati in Active Directory. I dati includono la radice DFS, i collegamenti DFS e le destinazioni DFS.

Ogni struttura ad albero DFS ha una o più *destinazioni radice*. La destinazione radice è un server host che esegue il servizio DFS. Una struttura ad albero DFS può contenere uno o più *collegamenti DFS*. Ogni collegamento DFS punta a una o più cartelle condivise nella rete. È possibile aggiungere, modificare ed eliminare collegamenti DFS da uno spazio dei nomi DFS. Quando si rimuove l'ultima destinazione associata a un collegamento DFS, DFS Elimina il collegamento DFS nello spazio dei nomi DFS. Nella documentazione precedente i collegamenti DFS erano denominati punti di giunzione.

Un collegamento DFS può puntare a una o più cartelle condivise. le cartelle sono denominate *destinazioni*. Quando gli utenti accedono a un collegamento DFS, il server DFS seleziona un set di destinazioni in base alle informazioni del sito del client. Il client accede alla prima destinazione disponibile nel set. In questo modo è possibile distribuire le richieste client tra le destinazioni possibili e fornire un'accessibilità continua per gli utenti anche in caso di errore di alcuni server.

Un'applicazione può utilizzare le funzioni DFS per:

- Aggiungere un collegamento DFS a una radice DFS.
- Creare o rimuovere spazi dei nomi DFS basati su dominio e autonomo.
- Aggiungere destinazioni a un collegamento DFS esistente.
- Rimuovere un collegamento DFS da una radice DFS.
- Rimuovere una destinazione da un collegamento DFS.
- Visualizzare e configurare le informazioni sulle radici e i collegamenti DFS.

Per un elenco delle funzioni DFS, vedere [funzioni file System distribuito](distributed-file-system-functions.md).

Per un elenco delle strutture DFS, vedere [file System distribuito Structures](distributed-file-system-structures.md).

Le destinazioni nei computer che eseguono Microsoft Windows possono essere pubblicate in uno spazio dei nomi DFS. È inoltre possibile pubblicare eventuali condivisioni non Microsoft per le quali i redirector client sono disponibili in uno spazio dei nomi DFS. Tuttavia, a differenza di una condivisione pubblicata in un server che esegue Windows Server, non possono ospitare una radice DFS o fornire riferimenti ad altre destinazioni DFS.

DFS usa il servizio Replica file di Windows Server per copiare le modifiche tra le destinazioni replicate. Gli utenti possono modificare i file archiviati in una destinazione e il servizio Replica file propaga le modifiche alle altre destinazioni designate. Il servizio conserva la modifica più recente di un documento o di un file.
