---
description: Il formato dei dati recuperati dalla funzione RegQueryValueEx inizia con una struttura di intestazione a lunghezza fissa, un \_ blocco di dati Perf \_ .
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Formato dati prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551462"
---
# <a name="performance-data-format"></a>Formato dati prestazioni

Il formato dei dati recuperati dalla funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) inizia con una struttura di intestazione a lunghezza fissa, [**un \_ \_ blocco di dati Perf**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block). La struttura del **\_ \_ blocco di dati Perf** descrive il sistema e i dati sulle prestazioni. La struttura del **\_ \_ blocco di dati Perf** è seguita da un numero variabile di elementi di dati oggetto a lunghezza variabile. L'intestazione di ogni elemento oggetto contiene l'offset dell'elemento oggetto successivo nell'elenco. Nel diagramma seguente viene illustrata la struttura dei dati sulle prestazioni di base.

![struttura dei dati sulle prestazioni](images/perfdata.png)

Esistono due formati per gli elementi di dati oggetto: uno che supporta più istanze e l'altro che non supporta più istanze.

Ogni blocco di elementi di dati oggetto contiene una struttura del [**\_ \_ tipo di oggetto Perf**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) , che descrive i dati sulle prestazioni per l'oggetto. La struttura del **\_ \_ tipo di oggetto Perf** è seguita da un elenco di strutture di [**definizione dei \_ contatori \_ delle prestazioni**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) , una per ogni contatore definito per l'oggetto. Per un oggetto con una sola istanza, l'elenco delle strutture delle **\_ \_ definizioni dei contatori delle prestazioni** è seguito da una singola struttura del [**\_ \_ blocco del contatore delle prestazioni**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) , seguita dai dati del contatore. Ogni struttura di **\_ \_ definizione dei contatori delle prestazioni** contiene l'offset dall'inizio della struttura del **\_ \_ blocco del contatore delle prestazioni** ai dati del contatore corrispondenti. Nel diagramma seguente viene illustrata la struttura di un oggetto prestazione che non supporta più istanze.

![struttura dell'oggetto prestazione che non supporta più istanze](images/perfnoinst.png)

Per un tipo di oggetto che supporta più istanze, l'elenco di strutture di [**\_ \_ definizione dei contatori delle prestazioni**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) è seguito da un elenco di blocchi di informazioni sull'istanza (uno per ogni istanza). Ogni blocco di informazioni sull'istanza contiene una struttura di [**\_ \_ definizione dell'istanza Perf**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) , il nome dell'istanza e una struttura del [**blocco del \_ contatore \_ delle prestazioni**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) . Nel diagramma seguente viene illustrata la struttura di un oggetto prestazioni che supporta due istanze.

![struttura di un oggetto prestazioni che supporta due istanze](images/perfinst.png)

Per un esempio in cui vengono usati gli offset, vedere [visualizzazione di nomi di oggetti, istanze e contatori](displaying-object-instance-and-counter-names.md).

 

 
