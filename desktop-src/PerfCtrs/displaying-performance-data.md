---
description: La maggior parte dei contatori richiede due valori di esempio per calcolare un valore visualizzabile.
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: Visualizzazione dei dati sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56a2882485c0bf21db6f1f00788fb927442219f020b1241ab4cd64619c7ec56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794012"
---
# <a name="displaying-performance-data"></a>Visualizzazione dei dati sulle prestazioni

La maggior parte dei contatori richiede due valori di esempio per calcolare un valore visualizzabile. La formula per ogni contatore determina se il contatore richiede due campioni. Per un elenco dei contatori e delle relative formule, vedere la sezione Tipi di contatori di [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).

[Raccolta dei dati sulle prestazioni](collecting-performance-data.md) illustra come recuperare dati di esempio. Dopo aver creato gli esempi, in genere si chiama [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) per calcolare un valore visualizzabile.

Se è necessario aumentare o disattivare il valore del contatore per visualizzare il valore, chiamare la funzione [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor) prima di [**chiamare PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). I valori dei contatori possono essere ridimensionati di una potenza di dieci da un fattore da -7 a 7.

Se il percorso del contatore contiene un carattere jolly per il nome dell'istanza, chiamare [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) per recuperare una matrice di valori del contatore formattati per ogni istanza raccolta.

È anche possibile usare [**le funzioni PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) e [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) per calcolare un valore visualizzabile. Per usare queste funzioni, è necessario recuperare l'esempio raccolto dopo ogni [**chiamata PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) e archiviare l'esempio manualmente. Per recuperare l'esempio, chiamare [**la funzione PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) o [**PdhGetRawCounterArray.**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) Per i valori del contatore basati sul tempo, chiamare [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) prima **di PdhFormatFromRawValue** per recuperare la base temporale del contatore.

Se si eseguono calcoli usando i dati non elaborati, controllare sempre il membro **CStatus** della struttura [**\_ PDH RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) prima di usare l'esempio. L'esempio non è valido se il valore di **CStatus** non è PDH \_ CSTATUS \_ NEW DATA o \_ PDH \_ CSTATUS VALID \_ \_ DATA.

## <a name="displaying-statistics-for-a-counter"></a>Visualizzazione delle statistiche per un contatore

Per calcolare i valori minimo, massimo e medio di un contatore, chiamare la [**funzione PdhComputeCounterStatistics.**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) Quando si raccolgono esempi, archiviare le strutture [**\_ PDH RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) in una matrice passata a **PdhComputeCounterStatistics**. La funzione restituisce i valori statistici in una [**struttura PDH \_ STATISTICS.**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)

È anche possibile usare questa funzione per comprimere un file di log. Ad esempio, leggere dieci record da un file di log, chiamare [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) per calcolare il valore medio e quindi scrivere il valore medio in un file di log di output.

 

 
