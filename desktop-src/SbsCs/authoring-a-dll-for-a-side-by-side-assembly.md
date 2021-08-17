---
description: Quando si creano assembly side-by-side personalizzati, seguire le linee guida per la creazione di assembly side-by-side.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Creazione di DLL per assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb83ba1d788d82e8d4fa7ab5f657170875b5deee6921aec3013406328dc2fcf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142454"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Creazione di DLL per assembly side-by-side

Quando si creano assembly side-by-side personalizzati, seguire le linee guida per la creazione di assembly [side-by-side](guidelines-for-creating-side-by-side-assemblies.md) e creare tutte le DLL usate nell'assembly in base alle linee guida seguenti:

-   Le DLL devono essere progettate in modo che più versioni possano essere eseguite contemporaneamente e nello stesso processo senza interferire tra loro. Ad esempio, molte applicazioni ospitano più plug-in che richiedono una versione diversa di un componente. Lo sviluppatore dell'assembly side-by-side deve progettare e testare per garantire che più versioni del componente funzionino correttamente quando vengono eseguite contemporaneamente nello stesso processo.

-   Se si prevede di fornire il componente come componente condiviso nei sistemi precedenti Windows XP, è necessario continuare a installare il componente in questi sistemi come componente condiviso a istanza singola. In questo caso, è necessario assicurarsi che il componente sia compatibile con le versioni precedenti.

-   Valutare l'uso di oggetti quando nel sistema vengono eseguite più versioni dell'assembly. Determinare se versioni diverse dell'assembly richiedono strutture di dati separate, ad esempio file mappati alla memoria, named pipe, classi e messaggi Windows registrati, memoria condivisa, semafori, mutex e driver hardware. Tutte le strutture di dati usate nelle versioni degli assembly devono essere compatibili con le versioni precedenti. Decidere quali strutture di dati possono essere usate tra le versioni e quali strutture di dati devono essere private per una versione. Determinare se le strutture di dati condivise richiedono oggetti di sincronizzazione separati, ad esempio semafori e mutex.

-   Alcuni oggetti, ad esempio le classi window e Atoms, sono denominati in modo univoco per ogni processo. Gli oggetti, ad esempio le classi finestra, devono essere con controllo delle versioni per ogni assembly usando il manifesto. Per oggetti come Atoms, usare identificatori specifici della versione, a meno che non si prevede di condividerli tra versioni diverse. Se si usano identificatori specifici della versione, usare il numero di controllo delle versioni in quattro parti.

-   Non includere codice autoregistrato in alcuna DLL. Una DLL in un assembly side-by-side non può essere autoregistrazione.

-   Definire tutti i nomi specifici della versione nella DLL con \# istruzioni define. In questo modo tutte le chiavi del Registro di sistema possono essere modificate da un'unica posizione. Quando si rilascia una nuova versione dell'assembly, è necessario modificare solo questa \# istruzione define. Esempio:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Archiviare tutti i dati non disistenti nella directory Temp.

-   Non inserire i dati utente in posizioni globali. Mantenere i dati dell'applicazione separati dai dati utente.

-   Assegnare a tutti i file condivisi una versione del file che dipende dal nome dell'applicazione.

-   Assegnare a tutti i messaggi e alle strutture di dati usate tra i processi una versione per impedire la condivisione non intenzionale tra processi.

-   La DLL non deve dipendere dalla condivisione tra versioni che potrebbero non esistere, ad esempio sezioni di memoria condivisa non condivise tra versioni diverse dell'assembly.

-   Se si aggiungono nuove funzionalità che non seguono il contratto di compatibilità dell'interfaccia binaria della DLL originale, è necessario assegnare un nuovo CLSID, ProgId e nome file. Le versioni future dell'assembly side-by-side devono quindi usare questo CLSID, ProgId e nome file. In questo modo si evita un conflitto quando una versione della DLL non side-by-side viene registrata in una versione side-by-side.

-   Se si riutilizza lo stesso CLSID o ProgId, testare per assicurarsi che l'assembly sia compatibile con le versioni precedenti.

-   Inizializzare e impostare le impostazioni predefinite per l'assembly nel codice dell'assembly. Non salvare le impostazioni predefinite nel Registro di sistema.

-   Assegnare versioni a tutte le strutture di dati.

-   La DLL deve archiviare lo stato dell'assembly side-by-side come descritto in [Authoring State Archiviazione for Side-by-Side Assemblies](authoring-state-storage-for-side-by-side-assemblies.md).

 

 



