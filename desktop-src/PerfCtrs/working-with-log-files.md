---
description: Per aprire un file di log per la lettura, chiamare PdhOpenQuery e specificare un percorso per il file di log.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Utilizzo dei file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2032b90036f8f58c07d8c7e80e7e7ac2b2701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312073"
---
# <a name="working-with-log-files"></a>Utilizzo dei file di log

Per aprire un file di log per la lettura, chiamare [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) e specificare un percorso per il file di log. Per aprire un file di log per la scrittura, è necessario chiamare [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Per chiudere un file di log, chiamare [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) o [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) a seconda della funzione utilizzata per aprire il file di log.

## <a name="reading-from-a-log-file"></a>Lettura da un file di log

La lettura dei dati sulle prestazioni da un file di log equivale alla lettura dei dati da un'origine in tempo reale: si apre una query, si aggiungono contatori alla query e si chiama [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per raccogliere un campione dal file di log. **PdhCollectQueryData** restituisce PDH \_ non \_ più \_ dati quando si raggiunge la fine del file di log.

Ogni esempio nel file di log contiene un timestamp per il momento in cui è stato originariamente raccolto e scritto nel file di log. Per recuperare il timestamp del primo e dell'ultimo esempio nel file di log, chiamare la funzione [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) . Se si desidera limitare gli esempi letti dal log a un intervallo di tempo specifico, vedere [impostazione di un intervallo di tempo per una query](setting-a-time-range-for-a-query.md).

Se non si sa quali oggetti e contatori delle prestazioni sono presenti nel file di log, è possibile chiamare [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) per determinare l'elenco di oggetti. Dato un oggetto, è possibile chiamare [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) o [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) per recuperare un elenco delle istanze e dei contatori dell'oggetto contenuti nel file di log.

Se si chiama [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa), utilizzare gli elenchi di istanze e contatori per creare un percorso per ogni possibile combinazione di istanza e contatore. Quando si chiama [**chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) per aggiungere il contatore alla query, la funzione avrà esito negativo se il file di log non contiene la combinazione specificata.

Se si utilizza [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha), è possibile creare un percorso che contenga un carattere jolly per il nome dell'istanza e il contatore, ad esempio \\ oggetto ( \* ) \\ \* . La funzione restituisce \_ un percorso non valido PDH \_ se l'oggetto non contiene un'istanza. In questo caso, chiamare **PdhExpandWildCardPath** usando un carattere jolly solo per il contatore, ad esempio \\ Object \\ \* .

I sistemi operativi più recenti possono leggere i file di log generati in sistemi operativi meno recenti; Tuttavia, i file di log creati in Windows Vista e nei sistemi operativi successivi non possono essere letti nei sistemi operativi precedenti.

Per un esempio in cui vengono letti i dati da un file di log, vedere [lettura dei dati sulle prestazioni da un file di log](reading-performance-data-from-a-log-file.md).

## <a name="reading-from-multiple-log-files"></a>Lettura da più file di log

Se è necessario creare una query che legga da diversi file di log, chiamare [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) per associare i file di log insieme. È quindi necessario usare funzioni PDH che terminano con "H", ad esempio [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh).

## <a name="writing-to-a-log-file"></a>Scrittura in un file di log

Prima di scrivere in un file di log, chiamare [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) per creare una query e specificare l'origine dei dati sulle prestazioni, ovvero i dati in tempo reale o un file di log. Aggiungere quindi i contatori su cui si desidera eseguire la query.

Per aprire il file di destinazione, chiamare [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Specificare la query quando si apre il file di log. Per raccogliere i dati sulle prestazioni e scriverli nel file di log, chiamare [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

Se i dati del contatore vengono scritti in un file di log delimitato da virgole (CSV) o delimitati da tabulazioni (TSV) e il percorso contiene un'istanza con caratteri jolly, il percorso viene espanso e solo le istanze esistenti nel momento in cui il percorso è espanso vengono incluse nel file di log. Tuttavia, per i file binari (. grandi) o i file di log SQL, il carattere jolly non viene espanso in modo che il file di log contenga le istanze create durante la registrazione.

Per un esempio in cui vengono scritti i dati in un file di log, vedere [scrittura di dati sulle prestazioni in un file di log](writing-performance-data-to-a-log-file.md).

## <a name="compressing-a-log-file"></a>Compressione di un file di log

È possibile utilizzare la funzione [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) per comprimere un file di log. Ad esempio, leggere dieci record da un file di log, chiamare **PdhComputeCounterStatistics** per calcolare il valore medio e quindi scrivere il valore medio in un file di log di output.

Nell'argomento seguente vengono fornite informazioni aggiuntive sull'utilizzo di un file di log.

-   [Recupero delle dimensioni di un file di log](getting-the-size-of-a-log-file.md)

 

 



