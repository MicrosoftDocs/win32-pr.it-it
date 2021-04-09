---
title: file system resiliente
description: file system resiliente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104047539"
---
# <a name="resilient-file-system"></a>file system resiliente

## <a name="platform"></a>Piattaforma

**Server** : Windows Server 2012 

## <a name="description"></a>Descrizione

Resilient file System (ReFS) è un nuovo file system locale. Ottimizza la disponibilità dei dati, nonostante gli errori che potrebbero causare la perdita di dati o tempi di inattività. L'integrità dei dati garantisce che i dati aziendali critici siano protetti da errori e disponibili quando necessario. La sua architettura è progettata per fornire scalabilità e prestazioni in un'era di dimensioni dei set di dati costantemente crescenti e di carichi di lavoro dinamici.

Le funzionalità principali di ReFS sono:

-   **Integrità**: refs archivia i dati in modo che siano protetti da molti degli errori comuni che possono causare la perdita di dati. I metadati del file System sono sempre protetti. Facoltativamente, i dati utente possono essere protetti in base al volume, alla directory o al file. Se si verificano danneggiamenti, ReFS può rilevare e, se configurato con spazi di archiviazione, correggere automaticamente il danneggiamento. In caso di errore di sistema, ReFS è progettato per il ripristino rapido da tale errore, senza perdita di dati utente.
-   **Disponibilità**: refs è progettato per definire la priorità della disponibilità dei dati. Con ReFS, in caso di danneggiamento e non può essere riparato automaticamente, il processo di recupero online viene localizzato nell'area di danneggiamento, che non richiede il tempo di inattività del volume. In breve, se si verificano danneggiamenti, ReFS resterà online.
-   **Scalabilità**: refs è progettato per le dimensioni dei set di dati attuali e per le dimensioni dei set di dati di domani; è ottimizzato per la scalabilità elevata.
-   **Compatibilità delle app**: per massimizzare AppCompat, refs supporta un sottoinsieme di funzionalità NTFS, oltre ad API Win32 ampiamente adottate.
-   **Identificazione proattiva degli errori**: le funzionalità di integrità di refs vengono sfruttate da uno scanner di integrità dei dati (uno "scrubber") che analizza periodicamente il volume, tenta di identificare il danneggiamento latente e quindi attiva in modo proattivo un ripristino dei dati danneggiati.

## <a name="resources"></a>Risorse

-   [Creazione di un post di Blog su Windows 8-Creazione di una nuova generazione file system per Windows: ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Compatibilità delle applicazioni e ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 