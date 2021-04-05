---
title: Aggiornamento della cache degli schemi
description: Tutte le informazioni scritte in un server di Active Directory vengono convalidate in base allo schema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Aggiornamento dell'annuncio della cache degli schemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707516"
---
# <a name="updating-the-schema-cache"></a>Aggiornamento della cache degli schemi

Tutte le informazioni scritte in un server di Active Directory vengono convalidate in base allo schema. Lo schema viene mantenuto in memoria nei server di directory (controller di dominio) per motivi di prestazioni. La versione in memoria viene aggiornata automaticamente dopo l'aggiornamento della versione su disco. L'aggiornamento automatico si verifica cinque minuti dopo l'applicazione dell'Ultima modifica. Se si applica un'altra modifica allo schema nella finestra di 5 minuti, il timer viene reimpostato per altri 5 minuti. Questo comportamento mantiene la coerenza della cache, ma può creare confusione, perché le modifiche non vengono visualizzate nello schema finché la cache non viene aggiornata, anche se sono state applicate su disco.

Per aggiornare la cache dello schema Active Directory dopo un aggiornamento dello schema oppure se si desidera utilizzare immediatamente l'aggiornamento dello schema per le operazioni non dello schema, aggiungere l'attributo **schemaUpdateNow** (è un attributo operativo) al DSE radice (DN vuoto) con il valore 1. Un aggiornamento della cache dello schema viene avviato immediatamente. La chiamata è in blocco. Se la chiamata restituisce senza errori, la cache viene aggiornata e tutti gli aggiornamenti dello schema sono pronti per l'utilizzo. Un errore restituito indica che l'aggiornamento della cache non è riuscito. Le applicazioni che devono utilizzare questa funzionalità devono essere progettate per supportare la scrittura di blocco, in particolare per fornire commenti e suggerimenti degli utenti, se il programma o lo script viene eseguito in modo interattivo.

L'esempio di codice seguente è uno script LDIFDE di esempio che illustra come attivare un ricaricamento della cache.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Per ulteriori informazioni su come aggiornare la cache dello schema a livello di programmazione, vedere [codice di esempio per l'aggiornamento della cache dello schema](example-code-for-updating-the-schema-cache.md).

 

 




