---
description: Il servizio Replica file è deprecato in Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Il servizio Replica file è deprecato in Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72940d2b73b807d5420aface3096714ac132df2095d154fc7563717c33fa6e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759941"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>Il servizio Replica file è deprecato in Windows Server 2008 R2

## <a name="platform"></a>Piattaforma

 **Server -** Windows Server 2008 R2  

## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità:** alto  
**Frequenza:** alto  


## <a name="description"></a>Descrizione

In Windows Server 2008 R2, il servizio Replica file non può essere usato per la replica di cartelle file system distribuito (DFS) o dati personalizzati (non SYSVOL). Un controller di dominio di Windows Server 2008 R2 può comunque usare il servizio Replica file per replicare il contenuto della condivisione SYSVOL in un dominio che usa il servizio Replica file per la replica della condivisione SYSVOL tra controller di dominio. Tuttavia, Windows server Server 2008 R2 non possono usare il servizio Replica file per replicare il contenuto di qualsiasi set di repliche a parte la condivisione SYSVOL. Il Replica DFS è una sostituzione del servizio Replica file e può essere usato per replicare il contenuto della condivisione SYSVOL, delle cartelle DFS e di altri dati personalizzati (non SYSVOL). Eseguire la migrazione di tutti i set di repliche FRS non SYSVOL Replica DFS. È anche consigliabile eseguire la migrazione della replica della condivisione SYSVOL dal servizio Replica file a Replica DFS perché Replica DFS è più affidabile, scalabile e offre prestazioni di replica migliori rispetto al servizio Replica file.

## <a name="manifestation"></a>Manifestazione

La replica FRS dei dati personalizzati verrà erta in modo irreversibile durante l'aggiornamento sul posto. L'unico modo per eseguire il ripristino da questa situazione è reinstallare un sistema operativo precedente nel server e reinizializzare la replica frs. I server aggiornati a Windows Server 2008 R2 non possono partecipare ai gruppi di replica frs esistenti.

## <a name="mitigation-of-impact"></a>Mitigazione dell'impatto

Per evitare problemi che potrebbero verificarsi in seguito a queste modifiche, eseguire la migrazione di set di replica FRS personalizzati Replica DFS. Il Replica DFS offre numerosi vantaggi rispetto al servizio Replica file, tra cui strumenti di gestione migliorati, prestazioni superiori e gestione delegata.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Panoramica del servizio Replica file](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Replica DFS (Distributed File System): domande frequenti](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guida alla migrazione della replica SYSVOL: Replica da FRS a DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
