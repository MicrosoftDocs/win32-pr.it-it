---
description: Il tempo di interrupt è la quantità di tempo trascorso dall'ultimo avvio del sistema, in intervalli di 100 nanosecondi.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Tempo di interrupt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308100"
---
# <a name="interrupt-time"></a>Tempo di interrupt

Il *tempo di interrupt* è la quantità di tempo trascorso dall'ultimo avvio del sistema, in intervalli di 100 nanosecondi. Il conteggio del tempo di interrupt inizia da zero all'avvio del sistema e viene incrementato a ogni interrupt del clock per la lunghezza di un tick dell'orologio. La lunghezza esatta di un tick dell'orologio dipende dall'hardware sottostante e può variare tra i sistemi.

A differenza dell' [ora di sistema](system-time.md), il conteggio dei tempi di interrupt non è soggetto a modifiche da parte degli utenti o del servizio ora di Windows, rendendolo la scelta migliore per la misurazione di durate brevi. Le applicazioni che richiedono una maggiore precisione rispetto al numero di interrupt devono usare un [timer ad alta risoluzione](../winmsg/about-timers.md). Utilizzare la funzione [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) per recuperare la frequenza del timer ad alta risoluzione e la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) per recuperare il valore del contatore.

È possibile utilizzare le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) per recuperare il conteggio del tempo di interrupt. Il tempo di interrupt non distorta indica che viene conteggiato solo il tempo in cui il sistema si trova nello stato di lavoro; pertanto, il numero di interruzioni del sistema non viene "distorta" entro il tempo di sospensione o di ibernazione del sistema.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP/2000:** La funzione [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) è disponibile a partire da Windows 7 e windows Server 2008 R2.

La risoluzione del timer impostata dalle funzioni [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) influiscono sulla risoluzione delle funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) e [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Tuttavia, non è consigliabile aumentare la risoluzione del timer perché può ridurre le prestazioni complessive del sistema e aumentare il consumo di energia impedendo al processore di accedere agli Stati di risparmio energia. Al contrario, le applicazioni devono utilizzare un timer ad alta risoluzione.

> [!Note]  
> Le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) producono risultati diversi per le compilazioni di debug ("verificate") di Windows, perché il conteggio dei tempi di interrupt e il numero di cicli sono avanzati di circa 49 giorni. Ciò consente di identificare i bug che potrebbero non verificarsi fino a quando il sistema non è in esecuzione per molto tempo. La compilazione selezionata è disponibile per gli abbonati MSDN tramite il sito Web [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .

 

Nell'esempio seguente viene illustrato come recuperare il conteggio del tempo di interrupt chiamando le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . Collegarsi alla libreria OneCore. lib quando si compila un'applicazione console che chiama queste funzioni.


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



Per recuperare il tempo trascorso per la sospensione o l'ibernazione, utilizzare la funzione [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) oppure utilizzare il contatore delle prestazioni del tempo di sistema. Questo contatore delle prestazioni può essere recuperato dai dati sulle prestazioni nella chiave del registro di sistema **HKEY \_ \_ dati sulle prestazioni**. Il valore restituito è un valore a 8 byte. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
