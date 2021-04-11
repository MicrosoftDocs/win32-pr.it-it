---
description: Per creare una nuova query che raccoglie i dati sulle prestazioni da un file di origine o di log in tempo reale, chiamare la funzione PdhOpenQuery. La funzione restituisce un handle per la query usata nelle chiamate di funzione PDH successive.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Creazione di una query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9d50ec52966529a3476a6d375606ba3d0b538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131682"
---
# <a name="creating-a-query"></a>Creazione di una query

Per creare una nuova query che raccoglie i dati sulle prestazioni da un file di origine o di log in tempo reale, chiamare la funzione [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) . La funzione restituisce un handle per la query usata nelle chiamate di funzione PDH successive.

Dopo aver creato la query, chiamare la funzione [**chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) per ogni contatore che si desidera aggiungere alla query. Per specificare il percorso completo del contatore, è possibile utilizzare uno dei metodi seguenti.

-   Definire il percorso del contatore come stringa statica. Utilizzare questo metodo se si monitora sempre lo stesso contatore e se si ha familiarità con la sintassi corretta di un percorso del contatore. Per informazioni sulla sintassi corretta utilizzata per specificare un contatore, vedere [specifica di un percorso del contatore](specifying-a-counter-path.md).
-   Inizializzare una struttura [**\_ \_ \_ degli elementi del percorso del contatore PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) con i nomi di computer, oggetto, contatore e istanza. Passare questa struttura a [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) che restituirà un percorso del contatore per gli elementi specificati.
-   Specificare un percorso del contatore che contenga caratteri jolly e chiamare [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) per ottenere un elenco dei nomi dei contatori che corrispondono ai caratteri jolly nel percorso. Analizzare l'elenco dei nomi dei contatori e aggiungere alla query i contatori desiderati da questo elenco.
-   Chiamare la funzione [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) per visualizzare una finestra di dialogo che consente all'utente di esplorare e selezionare i contatori delle prestazioni. Per ulteriori informazioni, vedere l' [esplorazione dei contatori](browsing-counters.md).

Si noti che se si specifica un'istanza del contatore che non esiste, [**chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) non segnala una condizione di errore. Viene invece restituito ERROR \_ Success. Il motivo di questo comportamento è che non è noto se è stata specificata un'istanza del contatore inesistente o se ne esiste una che non è ancora stata creata.

L'istanza del contatore mancante verrà segnalata da [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)o [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Quando si chiama **PdhCollectQueryData** solo per un'istanza del contatore e l'istanza del contatore non esiste ancora, si presuppone che l'istanza del contatore non esista e che la funzione restituisca PDH \_ senza \_ dati. Tuttavia, se viene eseguita una query su più di un contatore, **PdhCollectQueryData** può comunque restituire l'errore con \_ esito positivo anche se una delle istanze del contatore non esiste ancora. In questo caso, chiamare **PdhGetRawCounterValue** o **PdhGetFormattedCounterValue** per ognuna delle istanze del contatore di interesse. Se l'istanza non esiste quando si chiama **PdhGetRawCounterValue**, la funzione restituisce Error \_ Success e imposta il membro **CStatus** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) \_ sullo stato PDH \_ Nessuna \_ istanza. Se l'istanza non esiste quando si chiama **PdhGetFormattedCounterValue**, la funzione restituisce \_ dati non validi PDH \_ e imposta il membro **CStatus** di [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) su PDH \_ CStatus \_ Nessuna \_ istanza.

Si noti che è necessario localizzare il percorso del contatore specificato nella funzione [**chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) . La funzione [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) fornisce una modalità indipendente dalle impostazioni locali per aggiungere i contatori delle prestazioni alla query. Questa funzione è la modalità consigliata per aggiungere contatori indipendenti dalle impostazioni locali a una query.

Per rimuovere un contatore da una query, chiamare la funzione [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) .

Al termine della raccolta dei dati per una query, chiamare la funzione [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) per chiudere la query e rilasciare tutte le risorse di sistema allocate. **PdhCloseQuery** chiude tutti gli handle di contatore associati alla query.

 

 



