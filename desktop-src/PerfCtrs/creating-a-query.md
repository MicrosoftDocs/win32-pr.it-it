---
description: Per creare una nuova query che raccoglie i dati sulle prestazioni da un file di log o di origine in tempo reale, chiamare la funzione PdhOpenQuery. La funzione restituisce un handle per la query utilizzata nelle chiamate di funzione PDH successive.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Creazione di una query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1175c491ac1336458ed73d375d963f8a68b874bf3fecbb32000730a475d52714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775661"
---
# <a name="creating-a-query"></a>Creazione di una query

Per creare una nuova query che raccoglie i dati sulle prestazioni da un file di log o di origine in tempo reale, chiamare la [**funzione PdhOpenQuery.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) La funzione restituisce un handle per la query utilizzata nelle chiamate di funzione PDH successive.

Dopo aver creato la query, chiamare la [**funzione PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) per ogni contatore da aggiungere alla query. È possibile usare uno dei metodi seguenti per fornire il percorso completo del contatore.

-   Definire il percorso del contatore come stringa statica. Usare questo metodo se si monitora sempre lo stesso contatore e se si ha familiarità con la sintassi corretta di un percorso del contatore. Per informazioni sulla sintassi corretta usata per specificare un contatore, vedere [Specifica di un percorso contatore](specifying-a-counter-path.md).
-   Inizializzare [**una struttura PDH \_ COUNTER PATH \_ \_ ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) con i nomi del computer, dell'oggetto, del contatore e dell'istanza. Passare questa struttura a [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) che restituirà un percorso del contatore per gli elementi specificati.
-   Specificare un percorso contatore contenente caratteri jolly e chiamare [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) per ottenere un elenco di nomi di contatori che corrispondono ai caratteri jolly nel percorso. Analizzare l'elenco dei nomi dei contatori e aggiungere alla query i contatori desiderati da questo elenco.
-   Chiamare la [**funzione PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) per visualizzare una finestra di dialogo che consente all'utente di esplorare e selezionare i contatori delle prestazioni. Per altre informazioni, vedere [Esplorazione dei contatori](browsing-counters.md).

Si noti che se viene specificata un'istanza del contatore che non esiste, [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) non segnala una condizione di errore. Restituisce invece ERROR \_ SUCCESS. Il motivo di questo comportamento è che non è noto se è stata specificata un'istanza del contatore inesistente o se esisterà ma non è ancora stata creata.

L'istanza del contatore mancante verrà segnalata da [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)o [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Quando si chiama **PdhCollectQueryData** solo per un'istanza del contatore e l'istanza del contatore non esiste ancora, si presuppone che l'istanza del contatore non esista e che la funzione restituisca PDH \_ NO \_ DATA. Tuttavia, se viene eseguita una query su più contatori, **PdhCollectQueryData** può comunque restituire ERROR SUCCESS anche se una delle istanze del contatore \_ non esiste ancora. In questo caso, chiamare **PdhGetRawCounterValue** o **PdhGetFormattedCounterValue** per ognuna delle istanze del contatore di interesse. Se l'istanza non esiste quando si chiama **PdhGetRawCounterValue,** la funzione restituisce ERROR SUCCESS e imposta il membro \_ **CStatus** di [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) su PDH \_ STATUS NO \_ \_ INSTANCE. Se l'istanza non esiste quando si chiama **PdhGetFormattedCounterValue,** la funzione restituisce PDH INVALID DATA e imposta il membro CStatus di \_ \_ [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) su PDH  \_ CSTATUS NO \_ \_ INSTANCE.

Si noti che il percorso del contatore specificato nella [**funzione PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) deve essere localizzato. La [**funzione PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) offre un modo indipendente dalle impostazioni locali per aggiungere contatori delle prestazioni alla query. Questa funzione è il modo consigliato per aggiungere contatori indipendenti dalle impostazioni locali a una query.

Per rimuovere un contatore da una query, chiamare la [**funzione PdhRemoveCounter.**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)

Al termine della raccolta dei dati per una query, chiamare la [**funzione PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) per chiudere la query e rilasciare tutte le risorse di sistema allocate. **PdhCloseQuery** chiude tutti gli handle del contatore associati alla query.

 

 



