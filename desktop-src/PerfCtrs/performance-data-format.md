---
description: Il formato dei dati recuperati dalla funzione RegQueryValueEx inizia con una struttura di intestazione a lunghezza fissa, PERF \_ DATA \_ BLOCK.
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Formato dei dati sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea20d0cc0be6174fdd945c4bf956d7df60a067cd9f20b3d08d9762d75b8b97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143928"
---
# <a name="performance-data-format"></a>Formato dei dati sulle prestazioni

Il formato dei dati recuperati dalla funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) inizia con una struttura di intestazione a lunghezza fissa, [**PERF \_ DATA \_ BLOCK.**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block) La **struttura PERF \_ DATA \_ BLOCK** descrive il sistema e i dati sulle prestazioni. La **struttura PERF \_ DATA \_ BLOCK** è seguita da un numero variabile di elementi di dati oggetto a lunghezza variabile. L'intestazione di ogni elemento oggetto contiene l'offset dell'elemento oggetto successivo nell'elenco. Il diagramma seguente illustra la struttura dei dati sulle prestazioni di base.

![struttura dei dati sulle prestazioni](images/perfdata.png)

Esistono due formati per gli elementi dati oggetto: uno che supporta più istanze e l'altro che non supporta più istanze.

Ogni blocco di elementi dati oggetto contiene [**una struttura PERF \_ OBJECT \_ TYPE,**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) che descrive i dati sulle prestazioni per l'oggetto. La **struttura PERF \_ OBJECT \_ TYPE** è seguita da un elenco di [**strutture PERF COUNTER \_ \_ DEFINITION,**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) una per ogni contatore definito per l'oggetto. Per un oggetto con una sola istanza, l'elenco delle strutture **PERF \_ COUNTER \_ DEFINITION** è seguito da una singola struttura [**PERF \_ COUNTER \_ BLOCK,**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) seguita dai dati del contatore. Ogni **struttura PERF \_ COUNTER \_ DEFINITION** contiene l'offset dall'inizio della **struttura PERF COUNTER \_ \_ BLOCK** ai dati del contatore corrispondenti. Nel diagramma seguente viene illustrata la struttura di un oggetto prestazioni che non supporta più istanze.

![Struttura dell'oggetto prestazioni che non supporta più istanze](images/perfnoinst.png)

Per un tipo di oggetto che supporta più istanze, l'elenco di strutture [**COUNTER \_ \_ DEFINITION di PERF**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) è seguito da un elenco di blocchi di informazioni sull'istanza (uno per ogni istanza). Ogni blocco di informazioni sull'istanza [**contiene una struttura PERF INSTANCE \_ \_ DEFINITION,**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) il nome dell'istanza e una [**struttura PERF COUNTER \_ \_ BLOCK.**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) Nel diagramma seguente viene illustrata la struttura di un oggetto prestazioni che supporta due istanze di .

![Struttura di un oggetto prestazioni che supporta due istanze di](images/perfinst.png)

Per un esempio in cui vengono utilizzati gli offset, vedere Visualizzazione dei nomi di [oggetti, istanze e contatori.](displaying-object-instance-and-counter-names.md)

 

 
