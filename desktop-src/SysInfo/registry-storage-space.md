---
description: Anche se esistono pochi limiti tecnici al tipo e alle dimensioni dei dati che un'applicazione può archiviare nel Registro di sistema, esistono alcune linee guida pratiche per promuovere l'efficienza del sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Spazio di Archiviazione registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00414edbd34452fd6943a4d73a2ebe85af5d38884ddd0ca77f1d8fb41ae6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885079"
---
# <a name="registry-storage-space"></a>Spazio di Archiviazione registro

Anche se esistono pochi limiti tecnici al tipo e alle dimensioni dei dati che un'applicazione può archiviare nel Registro di sistema, esistono alcune linee guida pratiche per promuovere l'efficienza del sistema. Un'applicazione deve archiviare i dati di configurazione e inizializzazione nel Registro di sistema e archiviare altri tipi di dati altrove.

In genere, i dati costituiti da più di uno o due kilobyte (K) devono essere archiviati come file e a cui si fa riferimento usando una chiave nel Registro di sistema anziché essere archiviati come valore. Anziché duplicare grandi quantità di dati nel Registro di sistema, un'applicazione deve salvare i dati come file e fare riferimento al file. Il codice binario eseguibile non deve mai essere archiviato nel Registro di sistema.

Una voce di valore usa molto meno spazio del Registro di sistema rispetto a una chiave. Per risparmiare spazio, un'applicazione deve raggruppare dati simili come struttura e archiviare la struttura come valore anziché archiviare ognuno dei membri della struttura come chiave separata. L'archiviazione dei dati in formato binario consente a un'applicazione di archiviare i dati in un valore che altrimenti sarebbe costituito da diversi tipi incompatibili.

Le visualizzazioni dei file del Registro di sistema vengono mappate nella memoria del pool di paging.

**Windows Server 2008 per 32 bit, Windows Vista con SP1 per a 32 bit, Windows Vista, Windows Server 2003, Windows XP:** Le visualizzazioni dei file del Registro di sistema vengono mappate nello spazio degli indirizzi della cache del computer. Pertanto, indipendentemente dalle dimensioni dei dati del Registro di sistema, non vengono addebitati più di 4 megabyte (MB).

La dimensione massima di un hive del Registro di sistema è di 2 GB, ad eccezione dell'hive di sistema.

**Windows Server 2003 con SP1, Windows Server 2003 e Windows XP:** Non esistono limiti espliciti alla quantità totale di spazio che può essere utilizzata dagli hive nella memoria del pool di paging e nello spazio su disco, anche se le quote di sistema possono influire sulle dimensioni massime effettive. Le dimensioni massime di un hive del Registro di sistema erano limitate a 2 GB a partire da Windows Server 2003 con Service Pack 2 (SP2).

Le dimensioni massime dell'hive di sistema sono limitate dalla memoria fisica, come illustrato nella tabella seguente. 

| Sistema                      | Dimensioni massime dell'hive di sistema                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistemi basati su x86           | 50% della memoria fisica, fino a 400 MB. **Windows Server 2003 con SP2, Windows Server 2003 con SP1, Windows Server 2003 e Windows XP:** 25% della memoria fisica, fino a 200 MB.<br/>                                    |
| Sistemi basati su x64           | 50% della memoria fisica, fino a 1,5 GB. **Windows Server 2003 con SP2: 25%** della memoria di sistema, fino a 200 MB.<br/> **Windows Server 2003 con SP1, Windows Server 2003 e Windows XP 64-Bit Edition:** 32 MB.<br/> |
| Sistemi basati su Intel Itanium | 50% della memoria fisica, fino a 1 GB. **Windows Server 2008, Windows Vista, Windows Server 2003 con SP2, Windows Server 2003 con SP1, Windows Server 2003 e Windows XP 64-Bit Edition:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

I dati del Registro di sistema vengono archiviati nel pool di paging, un'area di memoria fisica utilizzata per i dati di sistema che possono essere scritti su disco quando non sono in uso. Il **valore RegistrySizeLimit** stabilisce la quantità massima di pool di paging che può essere utilizzata dai dati del Registro di sistema da tutte le applicazioni. Questo valore si trova nella chiave del Registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

Per impostazione predefinita, il limite delle dimensioni del Registro di sistema è il 25% del pool di paging. La dimensione predefinita del pool di paging è 32 MB, quindi 8 MB. Il sistema garantisce che il valore minimo di **RegistrySizeLimit** sia 4 MB e che il valore massimo sia circa l'80% del **valore PagedPoolSize.** Se il valore di questa voce è maggiore dell'80% delle dimensioni del pool di paging, il sistema imposta le dimensioni massime del Registro di sistema sull'80% delle dimensioni del pool di paging. Ciò impedisce al Registro di sistema di utilizzare lo spazio necessario per i processi. Si noti che l'impostazione di questo valore non alloca spazio nel pool di paging, né garantisce che lo spazio sarà disponibile se necessario.

Le dimensioni del pool di paging sono determinate dal **valore PagedPoolSize** nella chiave del Registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Per un esempio di come determinare le dimensioni correnti e massime del Registro di sistema, vedere [Determinazione delle dimensioni del Registro di sistema.](determining-the-registry-size.md)

Il pool di paging massimo è di circa 300.470 MB, quindi il limite delle dimensioni del Registro di sistema è 240-376 MB. Tuttavia, se si usa l'opzione /3GB, la dimensione massima del pool di paging è 192 MB, quindi il Registro di sistema può essere al massimo 153,6 MB.

 

 




