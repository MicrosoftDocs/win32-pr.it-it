---
description: In questa sezione vengono descritte le nuove funzionalità aggiunte ai contatori delle prestazioni per ogni versione.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Novità (contatori delle prestazioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c86a6a9ea644f1c650137cc392a2d54b6e8eedb34881d6b759d7b6c51635d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674701"
---
# <a name="whats-new-with-performance-counters"></a>Novità dei contatori delle prestazioni

In questa sezione vengono descritte le nuove funzionalità aggiunte ai contatori delle prestazioni per ogni versione.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Lo [strumento CTRPP](ctrpp.md) è stato modificato per migliorare e semplificare la generazione del codice. Lo strumento ora genera solo un file di intestazione e di risorse. Se si desidera un comportamento di generazione del codice precedente (scelta non consigliata), è possibile usare il nuovo `-legacy` argomento .

- È ora necessario specificare i nuovi argomenti e che specificano rispettivamente il nome e `-o` `-rc` il percorso dell'intestazione e del file di risorse.
- È possibile usare il nuovo argomento facoltativo per specificare una stringa da aggiungere all'inizio delle variabili globali e delle funzioni `-prefix` definite nel file di intestazione generato.
- Se è necessario aggiornare il manifesto dei contatori, l'uso della nuova generazione di codice elimina la necessità di unire l'implementazione del callback precedente con il nuovo codice generato perché i callback non sono più inclusi nel codice generato.

È disponibile `symbol` un nuovo attributo per gli elementi del manifesto seguenti:

- [Provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [Counterset](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [Contatore](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

`symbol`L'attributo è obbligatorio per [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) [e counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)ed è facoltativo per [il contatore](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). L'attributo consente di specificare un nome simbolico che è possibile usare per fare riferimento a ogni elemento quando si chiamano le funzioni del provider ( ad esempio, è possibile usare il nome simbolico del set di contatori quando si chiama [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

L'architettura dei contatori delle prestazioni per fornire i dati dei contatori è stata completamente modificata per questa versione.

In precedenza è stato usato un file INI per definire i dati dei contatori ed è stata implementata una DLL delle prestazioni eseguita nel processo del consumer per fornire i dati quando un consumer lo ha richiesto. Questa architettura è deprecata e non è consigliata per il nuovo codice a causa di problemi significativi di prestazioni e affidabilità.

La nuova architettura usa un manifesto per definire i dati del contatore ed esegue il codice nel processo del provider per fornire i dati quando un consumer lo richiede. Per altri dettagli, vedere [Fornire dati dei contatori usando la versione 2.0.](providing-counter-data-using-version-2-0.md)

Per questa versione sono state aggiunte le funzioni seguenti:

- [ControlCallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [PerfDeleteInstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [PerfQueryInstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [PerfSetCounterSetInfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [PerfSetULongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [PerfSetULongLongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [PerfSetCounterRefValue](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [PerfStartProvider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [PerfStopProvider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

Per questa versione sono state aggiunte le strutture seguenti:

- [IDENTITÀ DEL \_ CONTATORE DI PERF \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [INFORMAZIONI SUI \_ CONTATORI DI PERF \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [PERF \_ COUNTERSET \_ INFO](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [ISTANZA \_ COUNTERSET DI PERF \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Per un elenco degli elementi XML utilizzati nel manifesto per definire i contatori, vedere [Schema dei contatori delle prestazioni](performance-counters-schema.md).

Per informazioni sullo strumento preprocessore CTRPP che analizza il manifesto e genera il codice utilizzato come punto di partenza per il provider, vedere [CTRPP](ctrpp.md).
