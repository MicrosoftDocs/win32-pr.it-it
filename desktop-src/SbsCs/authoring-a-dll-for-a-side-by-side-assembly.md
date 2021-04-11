---
description: Quando si creano assembly affiancati, seguire le linee guida per la creazione di assembly affiancati.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Creazione di dll per assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa15f3876c60ce55be00d60d8f417eb0c2cbf6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232051"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Creazione di dll per assembly affiancati

Quando si creano assembly affiancati, seguire le [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md) e creare eventuali dll usate nell'assembly in base alle linee guida seguenti:

-   Le dll devono essere progettate in modo da consentire l'esecuzione di più versioni contemporaneamente e nello stesso processo senza interferire tra loro. Molte applicazioni, ad esempio, ospitano più plug-in, ognuno dei quali richiede una versione diversa di un componente. Lo sviluppatore deve progettare e testare l'assembly affiancato per assicurarsi che più versioni del componente funzionino correttamente quando vengono eseguite contemporaneamente nello stesso processo.

-   Se si prevede di fornire il componente come componente condiviso nei sistemi precedenti a Windows XP, è necessario continuare a installare il componente in questi sistemi come componente condiviso a istanza singola. In questo caso, è necessario assicurarsi che il componente sia compatibile con le versioni precedenti.

-   Valutare l'uso di oggetti quando più di una versione dell'assembly viene eseguita nel sistema. Determinare se versioni diverse dell'assembly richiedono strutture di dati separate, ad esempio file mappati alla memoria, named pipe, messaggi e classi di Windows registrate, memoria condivisa, semafori, mutex e driver hardware. Tutte le strutture di dati utilizzate nelle versioni degli assembly devono essere compatibili con le versioni precedenti. Decidere quali strutture di dati possono essere usate tra le versioni e quali strutture di dati devono essere private di una versione. Determinare se le strutture di dati condivise richiedono oggetti di sincronizzazione distinti, ad esempio semafori e mutex.

-   Alcuni oggetti, come le classi e gli atomi della finestra, sono denominati in modo univoco per ogni processo. Per ogni assembly che utilizza il manifesto è necessario che siano presenti oggetti quali le classi finestra. Per gli oggetti, ad esempio gli atomi, usare gli identificatori specifici della versione, a meno che non si preveda di condividere diverse versioni. Se si usano identificatori specifici della versione, usare il numero di versione in quattro parti.

-   Non includere codice di registrazione automatica in qualsiasi DLL. Una DLL in un assembly side-by-side non può eseguire la registrazione automatica.

-   Definire tutti i nomi specifici della versione nella DLL con le \# istruzioni define. In questo modo è possibile modificare tutte le chiavi del registro di sistema da una posizione. Quando si rilascia una nuova versione dell'assembly, è sufficiente modificare questa \# istruzione define. Ad esempio:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Archiviare i dati non permanenti nella directory Temp.

-   Non inserire i dati utente in percorsi globali. Mantieni i dati dell'applicazione separati dai dati utente.

-   Assegnare a tutti i file condivisi una versione del file che dipende dal nome dell'applicazione.

-   Assegnare tutti i messaggi e le strutture di dati usati nei processi di una versione per impedire la condivisione involontaria tra processi.

-   La DLL non deve dipendere dalla condivisione tra versioni che potrebbero non esistere, ad esempio sezioni di memoria condivisa non condivise tra versioni diverse dell'assembly.

-   Se si aggiungono nuove funzionalità che non seguono il contratto di compatibilità dell'interfaccia binaria della DLL originale, è necessario assegnare un nuovo nome CLSID, ProgId e file. Le versioni future dell'assembly affiancato sono quindi necessarie per usare il CLSID, il ProgId e il nome del file. In questo modo si evita un conflitto quando una versione della DLL non affiancata viene registrata su una versione affiancata.

-   Se si riutilizza lo stesso CLSID o ProgId, testare per verificare che l'assembly sia compatibile con le versioni precedenti.

-   Inizializzare e impostare le impostazioni predefinite per l'assembly nel codice dell'assembly. Non salvare le impostazioni predefinite nel registro di sistema.

-   Assegnare le versioni a tutte le strutture di dati.

-   La DLL deve archiviare lo stato dell'assembly affiancato come descritto in [creazione dell'archiviazione dello stato per gli assembly affiancati](authoring-state-storage-for-side-by-side-assemblies.md).

 

 



