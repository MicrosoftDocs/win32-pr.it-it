---
title: Resiliente file system
description: Resiliente file system
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2938f99e232f37d6f36f575c6c2a419adf3b6dbdc2a06bd9c8e243d6ba4884
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882681"
---
# <a name="resilient-file-system"></a>Resiliente file system

## <a name="platform"></a>Piattaforma

**Server** - Windows Server 2012 

## <a name="description"></a>Descrizione

Resilient File System (ReFS) è un nuovo file system. Ottimizza la disponibilità dei dati, nonostante gli errori che causano una perdita di dati o un tempo di inattività cronologico. L'integrità dei dati garantisce che i dati business critical siano protetti da errori e disponibili quando necessario. L'architettura è progettata per offrire scalabilità e prestazioni in un'era di dimensioni dei set di dati in continua crescita e carichi di lavoro dinamici.

Le funzionalità principali di ReFS sono:

-   **Integrità:** ReFS archivia i dati in modo che sia protetto da molti degli errori comuni che possono causare la perdita di dati. I metadati del file system sono sempre protetti. Facoltativamente, i dati utente possono essere protetti per volume, per directory o per file. In caso di danneggiamento, ReFS può rilevare e, se configurato con Spazi di archiviazione, correggere automaticamente il danneggiamento. In caso di errore di sistema, ReFS è progettato per eseguire rapidamente il ripristino da tale errore, senza perdita di dati utente.
-   **Disponibilità:** ReFS è progettato per classificare in ordine di priorità la disponibilità dei dati. Con ReFS, se si verifica un danneggiamento e non può essere ripristinato automaticamente, il processo di recupero online viene localizzato nell'area di danneggiamento, senza richiedere tempi di inazione del volume. In breve, se si verifica un danneggiamento, ReFS rimarrà online.
-   **Scalabilità:** ReFS è progettato per le dimensioni dei set di dati attuali e per le dimensioni dei set di dati di domani. è ottimizzato per la scalabilità elevata.
-   **Compatibilità delle** app: per ottimizzare AppCompat, ReFS supporta un subset di funzionalità NTFS e API Win32 ampiamente adottate.
-   **Identificazione proattiva** degli errori: le funzionalità di integrità di ReFS vengono sfruttate da uno scanner di integrità dei dati (uno "scrubber") che analizza periodicamente il volume, tenta di identificare il danneggiamento latente e quindi attiva in modo proattivo una correzione dei dati danneggiati.

## <a name="resources"></a>Risorse

-   [Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Compatibilità delle applicazioni e ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 