---
title: Aggiornamento della cache dello schema
description: Tutte le informazioni scritte in un server Active Directory vengono convalidate rispetto allo schema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Aggiornamento di Schema Cache AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff477ce97aab2e0e49522309d386a7e1c37b31e3b8171ef20c626fdaaa5b53a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024529"
---
# <a name="updating-the-schema-cache"></a>Aggiornamento della cache dello schema

Tutte le informazioni scritte in un server Active Directory vengono convalidate rispetto allo schema. Lo schema viene mantenuto in memoria nei server di directory (controller di dominio) per motivi di prestazioni. La versione in memoria viene aggiornata automaticamente dopo l'aggiornamento della versione su disco. L'aggiornamento automatico viene eseguito cinque minuti dopo l'applicazione dell'ultima modifica. L'applicazione di un'altra modifica allo schema nella finestra di 5 minuti reimposta il timer per altri 5 minuti. Questo comportamento mantiene la cache coerente, ma può generare confusione, perché le modifiche non vengono visualizzate nello schema fino a quando la cache non viene aggiornata, anche se sono state applicate su disco.

Per aggiornare la cache dello schema di Active Directory dopo un aggiornamento dello schema o se si vuole usare immediatamente l'aggiornamento dello schema per le operazioni non dello schema, aggiungere l'attributo **schemaUpdateNow** (si tratta di un attributo operativo) al DSE radice (DN vuoto) con valore 1. Un aggiornamento della cache dello schema verrà avviato immediatamente. La chiamata è bloccata. Se la chiamata restituisce senza errori, la cache viene aggiornata e tutti gli aggiornamenti dello schema sono pronti per l'uso. Un errore restituito indica che l'aggiornamento della cache non è riuscito. Le applicazioni che devono usare questa funzionalità devono essere progettate per supportare la scrittura di blocco, in particolare per fornire commenti e suggerimenti all'utente, se il programma o lo script viene eseguito in modo interattivo.

L'esempio di codice seguente è uno script LDIFDE di esempio che illustra come attivare un ricaricamento della cache.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Per altre informazioni su come aggiornare la cache dello schema a livello di codice, vedere Codice di esempio [per l'aggiornamento della cache dello schema](example-code-for-updating-the-schema-cache.md).

 

 




