---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Il servizio Replica file (FRS) è deprecato in Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312700"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>Il servizio Replica file (FRS) è deprecato in Windows Server 2008 R2

## <a name="platform"></a>Piattaforma

 **Server-** Windows Server 2008 R2  

## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità-** Alta  
**Frequenza-** Alta  


## <a name="description"></a>Descrizione

In Windows Server 2008 R2 non è possibile usare il servizio Replica file (FRS) per la replica di cartelle file system distribuito (DFS) o dati personalizzati (non SYSVOL). Un controller di dominio Windows Server 2008 R2 può comunque utilizzare il servizio Replica file per replicare il contenuto della condivisione SYSVOL in un dominio che utilizza FRS per la replica della condivisione SYSVOL tra controller di dominio. Tuttavia, i server Windows Server 2008 R2 non possono usare il servizio Replica file per replicare il contenuto di un set di repliche separato dalla condivisione SYSVOL. Il servizio Replica DFS è una sostituzione per FRS e può essere usato per replicare il contenuto della condivisione SYSVOL, delle cartelle DFS, nonché di altri dati personalizzati (non SYSVOL). Eseguire la migrazione di tutti i set di repliche FRS non SYSVOL a Replica DFS. Si consiglia inoltre di eseguire la migrazione della replica della condivisione SYSVOL da FRS a Replica DFS perché Replica DFS è più affidabile e scalabile e offre prestazioni di replica migliori rispetto a FRS.

## <a name="manifestation"></a>Manifestazione

La replica FRS dei dati personalizzati si interrompe in maniera irreversibile durante l'aggiornamento sul posto. L'unico modo per risolvere questo problema è reinstallare un sistema operativo precedente nel server e reinizializzare la replica FRS. Ai server che sono stati aggiornati a Windows Server 2008 R2 non è consentito partecipare ai gruppi di replica FRS esistenti.

## <a name="mitigation-of-impact"></a>Attenuazione dell'effetto

Per evitare problemi che potrebbero verificarsi in seguito a queste modifiche, eseguire la migrazione di set di replica FRS personalizzati a Replica DFS. Il servizio Replica DFS offre molti vantaggi rispetto a FRS, inclusi strumenti di gestione migliorati, prestazioni superiori e gestione delegata.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Panoramica di FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Replica DFS (Distributed File System): domande frequenti](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guida alla migrazione della replica SYSVOL: Replica da FRS a DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
