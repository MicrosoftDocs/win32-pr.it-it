---
description: In questa sezione vengono descritte le nuove funzionalità aggiunte ai contatori delle prestazioni per ogni versione.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Novità (contatori delle prestazioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312104"
---
# <a name="whats-new-with-performance-counters"></a>Novità dei contatori delle prestazioni

In questa sezione vengono descritte le nuove funzionalità aggiunte ai contatori delle prestazioni per ogni versione.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Lo strumento [CTRPP](ctrpp.md) è stato modificato per migliorare e semplificare la generazione di codice. Lo strumento ora genera solo un file di intestazione e di risorse. Se si vuole un comportamento di generazione del codice obsoleto (non consigliato), è possibile usare il nuovo `-legacy` argomento.

- È ora necessario specificare i nuovi `-o` `-rc` argomenti e che specificano rispettivamente il nome e il percorso del file di intestazione e di risorse.
- È possibile usare il nuovo `-prefix` argomento facoltativo per specificare una stringa da aggiungere all'inizio delle variabili globali e delle funzioni definite nel file di intestazione generato.
- Se è necessario aggiornare il manifesto dei contatori, l'utilizzo della nuova generazione del codice elimina la necessità di eseguire il merge dell'implementazione di callback precedente con il nuovo codice generato poiché i callback non sono più inclusi nel codice generato.

`symbol`È disponibile un nuovo attributo per gli elementi manifesto seguenti:

- [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

L' `symbol` attributo è obbligatorio per il [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) e il contatore e è facoltativo per il [contatore](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). [](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element) L'attributo consente di fornire un nome simbolico che è possibile utilizzare per fare riferimento a ogni elemento quando si chiamano le funzioni del provider (ad esempio, è possibile utilizzare il nome simbolico dell'insieme di contatori quando si chiama [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

L'architettura dei contatori delle prestazioni per fornire i dati del contatore è stata modificata completamente per questa versione.

In precedenza è stato usato un file INI per definire i dati del contatore ed è stata implementata una DLL di prestazioni che è stata eseguita nel processo del consumer per fornire i dati quando un consumer lo ha richiesto. Questa architettura è deprecata e non è consigliata per il nuovo codice a causa di problemi significativi relativi a prestazioni e affidabilità.

La nuova architettura usa un manifesto per definire i dati del contatore ed esegue il codice nel processo del provider per fornire i dati quando un consumer lo richiede. Per ulteriori informazioni, vedere la pagina relativa alla [fornitura di dati del contatore con la versione 2,0](providing-counter-data-using-version-2-0.md).

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

- [\_identità contatore \_ prestazioni](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [\_informazioni contatore \_ prestazioni](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [informazioni sul contatore delle prestazioni \_ \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [istanza del contatore delle prestazioni \_ \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Per un elenco degli elementi XML usati nel manifesto per definire i contatori, vedere [schema dei contatori delle prestazioni](performance-counters-schema.md).

Per informazioni sullo strumento di pre-elaborazione CTRPP che analizza il manifesto e genera il codice usato come punto di partenza per il provider, vedere [CTRPP](ctrpp.md).
