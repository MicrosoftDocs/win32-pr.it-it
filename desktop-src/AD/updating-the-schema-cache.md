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
# <a name="updating-the-schema-cache"></a><span data-ttu-id="5a3e6-104">Aggiornamento della cache degli schemi</span><span class="sxs-lookup"><span data-stu-id="5a3e6-104">Updating the Schema Cache</span></span>

<span data-ttu-id="5a3e6-105">Tutte le informazioni scritte in un server di Active Directory vengono convalidate in base allo schema.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="5a3e6-106">Lo schema viene mantenuto in memoria nei server di directory (controller di dominio) per motivi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="5a3e6-107">La versione in memoria viene aggiornata automaticamente dopo l'aggiornamento della versione su disco.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="5a3e6-108">L'aggiornamento automatico si verifica cinque minuti dopo l'applicazione dell'Ultima modifica. Se si applica un'altra modifica allo schema nella finestra di 5 minuti, il timer viene reimpostato per altri 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="5a3e6-109">Questo comportamento mantiene la coerenza della cache, ma può creare confusione, perché le modifiche non vengono visualizzate nello schema finché la cache non viene aggiornata, anche se sono state applicate su disco.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="5a3e6-110">Per aggiornare la cache dello schema Active Directory dopo un aggiornamento dello schema oppure se si desidera utilizzare immediatamente l'aggiornamento dello schema per le operazioni non dello schema, aggiungere l'attributo **schemaUpdateNow** (è un attributo operativo) al DSE radice (DN vuoto) con il valore 1.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="5a3e6-111">Un aggiornamento della cache dello schema viene avviato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="5a3e6-112">La chiamata è in blocco.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-112">The call is blocking.</span></span> <span data-ttu-id="5a3e6-113">Se la chiamata restituisce senza errori, la cache viene aggiornata e tutti gli aggiornamenti dello schema sono pronti per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="5a3e6-114">Un errore restituito indica che l'aggiornamento della cache non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="5a3e6-115">Le applicazioni che devono utilizzare questa funzionalità devono essere progettate per supportare la scrittura di blocco, in particolare per fornire commenti e suggerimenti degli utenti, se il programma o lo script viene eseguito in modo interattivo.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="5a3e6-116">L'esempio di codice seguente è uno script LDIFDE di esempio che illustra come attivare un ricaricamento della cache.</span><span class="sxs-lookup"><span data-stu-id="5a3e6-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="5a3e6-117">Per ulteriori informazioni su come aggiornare la cache dello schema a livello di programmazione, vedere [codice di esempio per l'aggiornamento della cache dello schema](example-code-for-updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="5a3e6-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




