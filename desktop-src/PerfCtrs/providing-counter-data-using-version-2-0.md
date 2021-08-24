---
description: Con la versione 2.0, i contatori delle prestazioni modificano l'architettura per semplificare il processo per fornire i dati dei contatori ai consumer.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Specifica dei dati dei contatori con la versione 2.0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8e839fb72f8cbd8272f9afd89aa3456e1e0b08fc7197dd992b1069fec7ce108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143794"
---
# <a name="providing-counter-data-using-version-20"></a>Specifica dei dati dei contatori con la versione 2.0

I provider di dati delle prestazioni moderni usano un manifesto per definire i dati dei contatori e usare le API del provider dei contatori delle prestazioni per gestire i dati all'interno del contesto del provider. I provider implementati usando un manifesto e le API del provider dei contatori delle prestazioni sono spesso denominati **provider V2.** Windows supporta i provider in modalità utente V2 in Windows Vista o versioni successive e i provider V2 in modalità kernel in Windows 7 o versioni successive.

Questa pagina descrive i provider V2 in modalità utente. Per informazioni sui provider V2 in modalità kernel, vedere [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

In fase di esecuzione, i provider V2 funzionano come segue:

- Il processo del provider si registra con il Windows contatore delle prestazioni chiamando PerfStartProvider e PerfSetCounterSetInfo. Il provider fornisce facoltativamente una funzione di callback che riceverà una notifica sulle richieste del consumer.
- Il processo del provider aggiunge o rimuove istanze in base alle esigenze usando PerfCreateInstance e PerfDeleteInstance. Il provider aggiorna i valori dei contatori quando cambiano usando le API PerfSet***.
- Un consumer effettua una richiesta di dati da un contatore. Il sistema verifica che il chiamante abbia le autorizzazioni per raccogliere i dati. Il sistema usa quindi un thread di lavoro in esecuzione nel processo del provider per gestire la richiesta, richiamando la funzione di callback del provider, se appropriato. Il thread di lavoro copia i dati raccolti in un buffer gestito dal sistema e quindi restituisce i dati al consumer.

## <a name="steps-to-creating-a-provider"></a>Passaggi per la creazione di un provider

1. Scrivere un manifesto che definisce i dati del contatore che verranno forniti dal provider. Per informazioni dettagliate sulla scrittura del manifesto, vedere [Schema dei contatori delle prestazioni.](performance-counters-schema.md)
2. Usare [CTRPP](ctrpp.md) per generare il codice del modello da includere nel provider. Il codice del modello include le strutture che definiscono gli insiemi di contatori, le funzioni [**CounterInitialize**](counterinitialize.md) [**e CounterCleanup**](countercleanup.md) e le stringhe di risorse.

   Il provider deve chiamare le [**funzioni CounterInitialize**](counterinitialize.md) [**e CounterCleanup.**](countercleanup.md) **CounterInitialize chiama** la [**funzione PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) per registrare il provider e chiama anche [**la funzione PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) per inizializzare l'insieme di contatori. **CounterCleanup** chiama la [**funzione PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) per rimuovere la registrazione del provider.

3. Includere nel progetto il codice del modello del passaggio precedente e completare il provider.

   Per completare il provider, è necessario chiamare la [**funzione PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) per ogni istanza dell'insieme di contatori specificato.

   Per impostare i valori del contatore, chiamare una delle funzioni seguenti:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   Il vantaggio dell'uso di [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) è che non è necessario eseguire una chiamata di funzione per impostare o aggiornare il valore del contatore, ma semplicemente aggiornare la variabile del contatore locale (la variabile a cui punta il riferimento) e i contatori delle prestazioni usano il puntatore per accedere al valore del contatore.

   Se non si usa [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), è possibile usare le funzioni seguenti per incrementare o decrementare il valore del contatore:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Prima che il provider venga chiuso, deve chiamare [**PerfDeleteInstance per**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) ogni istanza dell'insieme di contatori creata.

   Se è stato specificato l'attributo **di callback** nell'elemento [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) nel manifesto o è stato usato l'argomento **-NotificationCallback** quando si chiama [CTRPP,](ctrpp.md)è necessario implementare la funzione di callback [*ControlCallback.*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) La funzione di callback viene passata a [**CounterInitialize.**](counterinitialize.md)

   Se è stato usato **-MemoryRoutines** quando si chiama [CTRPP,](ctrpp.md)è necessario implementare le funzioni di callback [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) e [*FreeMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) Le funzioni di callback vengono passate a [**CounterInitialize.**](counterinitialize.md)

4. Quando si installa il provider, usare lo strumento LodCtr per scrivere nel Registro di sistema il nome del file binario contenente le stringhe di risorsa localizzate e gli ID risorsa. Per informazioni dettagliate sull'uso di LodCtr, vedere [Schema dei contatori delle prestazioni.](performance-counters-schema.md)

5. Quando si disinstalla il provider, usare lo strumento UnlodCtr per rimuovere le informazioni del provider dal Registro di sistema.
