---
description: La funzionalità partizioni COM+ include una cache di partizione. Questa cache archivia i mapping da utente a partizione ed è progettata per evitare l'accesso Active Directory ripetitivo.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configurazione della cache della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305225"
---
# <a name="configuring-the-partition-cache"></a>Configurazione della cache della partizione

La funzionalità partizioni COM+ include una cache di partizione. Questa cache archivia i mapping da utente a partizione ed è progettata per evitare l'accesso Active Directory ripetitivo.

## <a name="changing-cache-size"></a>Modifica delle dimensioni della cache

La cache di partizione è costituita da tre tabelle, le cui dimensioni possono essere modificate per migliorare le prestazioni. Queste tabelle sono costituite dal numero di voci SID nella cache, dal numero di voci OU nella cache e dal numero di voci della partizione nella cache.

Per modificare le dimensioni della tabella, gli amministratori possono modificare i valori di una chiave del registro di sistema. La chiave del registro di sistema e i relativi valori sono i seguenti:

**HKLM \\ software \\ Microsoft \\ COM3 \\ PartitionCache**



| Valori chiave                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contiene il \_ valore reg DWORD per il numero di voci SID nella cache (valore predefinito = 512). Questo valore deve essere impostato su un valore maggiore del numero di identità univoche che un computer sarà in grado di gestire nell'intervallo di tempo di invalidamento della cache.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contiene il \_ valore reg DWORD per il numero di voci di nome unità organizzativa nella cache (impostazione predefinita = 64). Questo valore deve essere impostato su un valore maggiore del numero di nomi di unità organizzative univoci che un computer sarà in grado di gestire nell'intervallo di tempo di invalidamento della cache.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contiene il \_ valore reg DWORD per il numero di voci della partizione nella cache (valore predefinito = 1024).<br/> Nell'intervallo di tempo di invalidamento della cache, il valore DWORD deve essere impostato su un numero maggiore del numero di partizioni univoche che un computer sarà in grado di gestire. Questo perché il contesto di un componente può includere un ID di partizione per una partizione che non risiede nel computer. <br/> |
| **EntryExpiration**<br/>     | Contiene il \_ valore reg DWORD per il numero di cicli (ogni segno di indisponibilità = ~ 7 minuti) finché una voce della cache non diventa non valida (impostazione predefinita = 4 (~ 28 minuti)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Scaricamento della cache

Poiché COM+ memorizza nella cache la partizione predefinita per gli utenti, potrebbe essere necessario chiamare questo metodo dopo aver modificato la partizione predefinita per un utente nel Active Directory. Gli amministratori possono eseguire questa operazione a livello di codice chiamando il metodo [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche della partizione](collecting-partition-metrics.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione di partizioni all'interno Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




