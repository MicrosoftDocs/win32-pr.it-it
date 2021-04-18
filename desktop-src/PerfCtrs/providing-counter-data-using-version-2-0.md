---
description: Con la versione 2,0, i contatori delle prestazioni hanno modificato l'architettura per semplificare il processo di invio dei dati dei contatori ai consumer.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Fornire dati del contatore usando la versione 2,0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 67976c8a0b6c77582ed8c50c2e5cf753c77fcf6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312094"
---
# <a name="providing-counter-data-using-version-20"></a>Fornire dati del contatore usando la versione 2,0

I provider di dati delle prestazioni moderni utilizzano un manifesto per definire i dati del contatore e utilizzare le API del provider del contatore delle prestazioni per gestire i dati all'interno del contesto del provider. I provider implementati utilizzando un manifesto e le API del provider del contatore delle prestazioni vengono spesso chiamati **provider v2**. Windows supporta i provider v2 in modalità utente in Windows Vista o versioni successive e i provider in modalità kernel v2 in Windows 7 o versioni successive.

Questa pagina descrive i provider v2 in modalità utente. Per informazioni sui provider v2 in modalità kernel, vedere [monitoraggio delle prestazioni in modalità kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

In fase di esecuzione, i provider v2 funzionano come segue:

- Il processo del provider viene registrato con il sistema di contatori delle prestazioni Windows chiamando PerfStartProvider e PerfSetCounterSetInfo. Il provider fornisce facoltativamente una funzione di callback che riceverà una notifica relativa alle richieste del consumer.
- Il processo del provider aggiunge o rimuove le istanze in base alle esigenze usando PerfCreateInstance e PerfDeleteInstance. Il provider aggiorna i valori dei contatori quando vengono modificati usando le API PerfSet * * _.
- Un consumer effettua una richiesta di dati da un contatore. Il sistema verifica che il chiamante disponga delle autorizzazioni per la raccolta dei dati. Il sistema usa quindi un thread di lavoro in esecuzione nel processo del provider per gestire la richiesta, richiamando la funzione di callback del provider, se appropriato. Il thread di lavoro copia i dati raccolti in un buffer gestito dal sistema, quindi i dati vengono restituiti al consumer.

## <a name="steps-to-creating-a-provider"></a>Passaggi per la creazione di un provider

1. Scrivere un manifesto che definisce i dati del contatore che il provider fornirà. Per informazioni dettagliate sulla scrittura del manifesto, vedere [schema dei contatori delle prestazioni](performance-counters-schema.md).
2. Usare [CTRPP](ctrpp.md) per generare il codice del modello incluso nel provider. Il codice del modello include le strutture che definiscono gli insiemi di contatori, le funzioni [_ *CounterInitialize* *](counterinitialize.md) e [**CounterCleanup**](countercleanup.md) e le stringhe di risorsa.

   Il provider deve chiamare le funzioni [**CounterInitialize**](counterinitialize.md) e [**CounterCleanup**](countercleanup.md) . **CounterInitialize** chiama la funzione [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) per registrare il provider e chiama anche la funzione [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) per inizializzare l'insieme di contatori. **CounterCleanup** chiama la funzione [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) per rimuovere la registrazione del provider.

3. Includere il codice del modello del passaggio precedente nel progetto e completare il provider.

   Per completare il provider, è necessario chiamare la funzione [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) per ogni istanza dell'insieme di contatori fornito.

   Per impostare i valori del contatore, chiamare una delle funzioni seguenti:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   Il vantaggio dell'utilizzo di [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) consiste nel fatto che non è necessario effettuare una chiamata di funzione per impostare o aggiornare il valore del contatore, ma è sufficiente aggiornare la variabile del contatore locale (la variabile a cui puntano i punti di riferimento) e i contatori delle prestazioni utilizzano il puntatore per accedere al valore del contatore.

   Se non si utilizza [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), è possibile utilizzare le funzioni seguenti per incrementare o decrementare il valore del contatore:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Prima della chiusura del provider, deve chiamare il [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) per ogni istanza dell'insieme di contatori creata.

   Se è [**stato**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) specificato l'attributo **callback** nell'elemento provider nel manifesto oppure è stato usato l'argomento **-NotificationCallback** quando si chiama [CTRPP](ctrpp.md), è necessario implementare la funzione di callback [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) . La funzione di callback viene passata a [**CounterInitialize**](counterinitialize.md).

   Se è stato usato il **-MemoryRoutines** quando si chiama [CTRPP](ctrpp.md), è necessario implementare le funzioni di callback [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) e [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Le funzioni di callback vengono passate a [**CounterInitialize**](counterinitialize.md).

4. Quando si installa il provider, usare lo strumento LodCtr per scrivere il nome del file binario che contiene le stringhe di risorsa localizzate e gli ID risorsa nel registro di sistema. Per informazioni dettagliate sull'uso di LodCtr, vedere [schema dei contatori delle prestazioni](performance-counters-schema.md).

5. Quando si disinstalla il provider, usare lo strumento UnlodCtr per rimuovere le informazioni del provider dal registro di sistema.
