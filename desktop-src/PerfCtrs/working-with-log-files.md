---
description: Per aprire un file di log per la lettura, chiamare PdhOpenQuery e specificare un percorso al file di log.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Uso dei file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82281694b72a2c28bb0e65ee4db16bd9ba33b8ed9c6e5e74dbf6c6cbf559507a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143744"
---
# <a name="working-with-log-files"></a>Uso dei file di log

Per aprire un file di log per la lettura, chiamare [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) e specificare un percorso al file di log. Per aprire un file di log per la scrittura, è necessario chiamare [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Per chiudere un file di log, chiamare [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) o [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) a seconda della funzione usata per aprire il file di log.

## <a name="reading-from-a-log-file"></a>Lettura da un file di log

La lettura dei dati sulle prestazioni da un file di log è la stessa della lettura dei dati da un'origine in tempo reale: si apre una query, si aggiungono contatori alla query e si chiama [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per raccogliere un esempio dal file di log. **PdhCollectQueryData** restituisce PDH NO MORE DATA quando \_ si raggiunge la fine del file di \_ \_ log.

Ogni esempio nel file di log contiene un timestamp per il momento in cui è stato raccolto e scritto in origine nel file di log. Per recuperare il timestamp per il primo e l'ultimo esempio nel file di log, chiamare la [**funzione PdhGetDataSourceTimeRange.**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) Per limitare gli esempi letti dal log a un intervallo di tempo specifico, vedere Impostazione di un intervallo di tempo [per una query](setting-a-time-range-for-a-query.md).

Se non si conoscono gli oggetti prestazioni e i contatori presenti nel file di log, è possibile chiamare [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) per determinare l'elenco di oggetti. Dato un oggetto, è possibile chiamare [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) o [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) per recuperare un elenco delle istanze e dei contatori dell'oggetto contenuti nel file di log.

Se si chiama [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa), usare gli elenchi di istanze e contatori per creare un percorso per ogni possibile combinazione di istanza e contatore. Quando si chiama [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) per aggiungere il contatore alla query, la funzione avrà esito negativo se il file di log non contiene la combinazione specificata.

Se si usa [**PdhExpandWildCardPath,**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)è possibile creare un percorso contenente un carattere jolly per il nome dell'istanza e il contatore, ad esempio \\ object( \* ) \\ \* . La funzione restituisce PDH \_ INVALID \_ PATH se l'oggetto non contiene un'istanza. In questo caso, chiamare **PdhExpandWildCardPath** usando un carattere jolly solo per il contatore, ad esempio \\ l'oggetto \\ \* .

I sistemi operativi più recenti possono leggere i file di log generati nei sistemi operativi meno recenti. Tuttavia, i file di log creati in Windows Vista e nei sistemi operativi successivi non possono essere letti nei sistemi operativi precedenti.

Per un esempio che legge i dati da un file di log, vedere Lettura dei dati [sulle prestazioni da un file di log](reading-performance-data-from-a-log-file.md).

## <a name="reading-from-multiple-log-files"></a>Lettura da più file di log

Se è necessario creare una query che legge da diversi file di log, chiamare [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) per associare i file di log. È quindi necessario usare funzioni PDH che terminano con 'H', ad esempio [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh).

## <a name="writing-to-a-log-file"></a>Scrittura in un file di log

Prima di scrivere in un file di log, chiamare [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) per creare una query e specificare l'origine dei dati sulle prestazioni, dati in tempo reale o file di log. Aggiungere quindi i contatori su cui eseguire una query.

Per aprire il file di destinazione, chiamare [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Specificare la query quando si apre il file di log. Per raccogliere i dati sulle prestazioni e scriverlo nel file di log, chiamare [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

Se i dati del contatore vengono scritti in un file di log delimitato da virgole (.csv) o delimitato da tabulazioni (con estensione tsv) e il percorso contiene un'istanza con caratteri jolly, il percorso viene espanso e nel file di log vengono incluse solo le istanze esistenti al momento dell'espansione del percorso. Tuttavia, per i file di log binari (con estensione blg) o SQL, il carattere jolly non viene espanso in modo che il file di log contenga istanze create durante la registrazione.

Per un esempio che scrive dati in un file di log, vedere [Scrittura di dati sulle prestazioni in un file di log](writing-performance-data-to-a-log-file.md).

## <a name="compressing-a-log-file"></a>Compressione di un file di log

È possibile usare la [**funzione PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) per comprimere un file di log. Ad esempio, leggere dieci record da un file di log, chiamare **PdhComputeCounterStatistics** per calcolare il valore medio e quindi scrivere il valore medio in un file di log di output.

Nell'argomento seguente vengono fornite informazioni aggiuntive sull'uso di un file di log.

-   [Recupero delle dimensioni di un file di log](getting-the-size-of-a-log-file.md)

 

 



