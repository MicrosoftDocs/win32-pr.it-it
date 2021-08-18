---
description: La funzionalità partizioni COM+ include una cache delle partizioni. Questa cache archivia i mapping utente-partizione ed è progettata per evitare l'accesso ripetitivo ad Active Directory.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configurazione della cache delle partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906e36065244ab7f2ffa54cad5a7aca33a0c152744af2b6017edb95a8a960b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128963"
---
# <a name="configuring-the-partition-cache"></a>Configurazione della cache delle partizioni

La funzionalità partizioni COM+ include una cache delle partizioni. Questa cache archivia i mapping utente-partizione ed è progettata per evitare l'accesso ripetitivo ad Active Directory.

## <a name="changing-cache-size"></a>Modifica delle dimensioni della cache

La cache delle partizioni è costituita da tre tabelle, le cui dimensioni possono essere modificate per migliorare le prestazioni. Queste tabelle sono costituite dal numero di voci SID nella cache, dal numero di voci di unità organizzative nella cache e dal numero di voci di partizione nella cache.

Per modificare queste dimensioni delle tabelle, gli amministratori possono modificare i valori di una chiave del Registro di sistema. La chiave del Registro di sistema e i relativi valori sono i seguenti:

**HKLM \\ SOFTWARE \\ Microsoft \\ COM3 \\ PartitionCache**



| Valori chiave                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contiene il valore \_ DWORD REG per il numero di voci SID nella cache (valore predefinito= 512). Questo valore deve essere impostato su un valore maggiore del numero di identità univoche che verranno servite da un computer nell'intervallo di tempo di invalidamento della cache.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contiene il valore DWORD REG per il numero di voci del nome dell'unità organizzativa \_ nella cache (valore predefinito= 64). Questo valore deve essere impostato su un valore maggiore del numero di nomi di unità organizzative univoci che verranno serviti da un computer nell'intervallo di tempo di invalidamento della cache.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contiene il valore \_ DWORD REG per il numero di voci di partizione nella cache (valore predefinito= 1024).<br/> Nell'intervallo di tempo di invalidamento della cache, il valore DWORD deve essere impostato su un numero maggiore del numero di partizioni univoche che verranno servite da un computer. Ciò è dovuto al fatto che il contesto di un componente può includere un ID di partizione per una partizione che non risiede in tale computer. <br/> |
| **EntryExpiration**<br/>     | Contiene il valore DWORD REG per il conteggio dei tick (ogni tick = ~7 minuti) fino a quando una voce della cache non diventa non valida \_ (valore predefinito= 4 (~28 minuti)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Scaricamento della cache

Poiché COM+ memorizza nella cache la partizione predefinita per gli utenti, potrebbe essere necessario chiamare questo metodo dopo aver modificato la partizione predefinita per un utente in Active Directory. Gli amministratori possono eseguire questa operazione a livello di codice chiamando [**il metodo FlushPartitionCache.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche delle partizioni](collecting-partition-metrics.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione delle partizioni all'interno di Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




