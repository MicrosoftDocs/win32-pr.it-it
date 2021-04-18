---
description: Sebbene esistano pochi limiti tecnici per il tipo e le dimensioni dei dati che un'applicazione può archiviare nel registro di sistema, sono disponibili alcune linee guida pratiche per promuovere l'efficienza del sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Spazio di archiviazione del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313260"
---
# <a name="registry-storage-space"></a>Spazio di archiviazione del registro di sistema

Sebbene esistano pochi limiti tecnici per il tipo e le dimensioni dei dati che un'applicazione può archiviare nel registro di sistema, sono disponibili alcune linee guida pratiche per promuovere l'efficienza del sistema. Un'applicazione deve archiviare i dati di configurazione e di inizializzazione nel registro di sistema e archiviare altri tipi di dati altrove.

In genere, i dati costituiti da più di uno o due kilobyte (K) devono essere archiviati come file e a cui viene fatto riferimento tramite una chiave nel registro di sistema anziché essere archiviati come valore. Anziché duplicare grandi quantità di dati nel registro di sistema, un'applicazione deve salvare i dati come file e fare riferimento al file. Il codice binario eseguibile non deve mai essere archiviato nel registro di sistema.

Una voce di valore usa molto meno spazio del registro di sistema rispetto a una chiave. Per risparmiare spazio, un'applicazione deve raggruppare dati simili come una struttura e archiviare la struttura come valore anziché archiviare ogni membro della struttura come chiave separata. L'archiviazione dei dati in formato binario consente a un'applicazione di archiviare i dati in un valore che altrimenti sarebbe costituito da diversi tipi incompatibili.

Viene eseguito il mapping delle visualizzazioni dei file del registro di sistema nella memoria del pool di paging.

**Windows server 2008 per 32 bit, Windows Vista con SP1 per 32 bit, Windows Vista, Windows server 2003, Windows XP:** Le visualizzazioni dei file del registro di sistema vengono mappate nello spazio degli indirizzi della cache del computer. Di conseguenza, indipendentemente dalle dimensioni dei dati del registro di sistema, non viene addebitato più di 4 megabyte (MB).

La dimensione massima di un hive del registro di sistema è di 2 GB, ad eccezione dell'hive di sistema.

**Windows server 2003 con SP1, Windows server 2003 e Windows XP:** Non sono previsti limiti espliciti sulla quantità totale di spazio che può essere utilizzata dagli hive nella memoria del pool di paging e nello spazio su disco, anche se le quote di sistema possono influire sulle dimensioni massime effettive. Le dimensioni massime di un hive del registro di sistema sono limitate a 2 GB a partire da Windows Server 2003 con Service Pack 2 (SP2).

La dimensione massima dell'hive di sistema è limitata dalla memoria fisica, come illustrato nella tabella seguente. 

| Sistema                      | Dimensioni massime dell'hive di sistema                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sistemi basati su x86           | 50% della memoria fisica, fino a 400 MB. **Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 e Windows XP:** 25% della memoria fisica, fino a 200 MB.<br/>                                    |
| sistemi basati su x64           | 50% della memoria fisica, fino a 1,5 GB. **Windows Server 2003 con SP2:** 25% della memoria di sistema, fino a 200 MB.<br/> **Windows server 2003 con SP1, Windows server 2003 e Windows XP 64-bit Edition:** 32 MB.<br/> |
| Sistemi basati su Intel Itanium | 50% della memoria fisica, fino a 1 GB. **Windows server 2008, Windows Vista, Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 e Windows XP 64-bit Edition:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

I dati del registro di sistema vengono archiviati nel pool di paging, un'area di memoria fisica usata per i dati di sistema che possono essere scritti su disco quando non sono in uso. Il valore **RegistrySizeLimit** stabilisce la quantità massima di pool di paging che può essere utilizzata dai dati del registro di sistema di tutte le applicazioni. Questo valore si trova nella seguente chiave del registro di sistema:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

Per impostazione predefinita, il limite di dimensioni del registro di sistema è pari al 25% del pool di paging. (La dimensione predefinita del pool di paging è 32 MB, quindi è 8 MB). Il sistema garantisce che il valore minimo di **RegistrySizeLimit** sia 4 MB e il valore massimo sia pari a circa il 80% del valore di **PagedPoolSize** . Se il valore di questa voce è maggiore del 80% delle dimensioni del pool di paging, il sistema imposta le dimensioni massime del registro di sistema sul 80% delle dimensioni del pool di paging. In questo modo si impedisce al registro di sistema di usare lo spazio necessario per i processi. Si noti che l'impostazione di questo valore non consente di allocare spazio nel pool di paging, né garantisce che lo spazio sarà disponibile se necessario.

Le dimensioni del pool di paging sono determinate dal valore **PagedPoolSize** nella seguente chiave del registro di sistema:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Per un esempio di come determinare le dimensioni correnti e massime del registro di sistema, vedere [determinazione delle dimensioni del registro](determining-the-registry-size.md)di sistema.

Il pool di paging massimo è di circa 300.470 MB, pertanto il limite delle dimensioni del registro di sistema è 240-376 MB. Tuttavia, se si usa l'opzione/3GB, le dimensioni massime del pool di paging sono pari a 192 MB, quindi il registro di sistema può avere un massimo di 153,6 MB.

 

 




