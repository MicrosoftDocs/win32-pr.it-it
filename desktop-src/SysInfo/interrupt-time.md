---
description: Il tempo di interruzione è la quantità di tempo dall'ultimo avvio del sistema, a intervalli di 100 nanosecondi.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Tempo di interrupt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0da8fa92fc51cdceef6f0052dda7a2cd27d7b21b24d11bd8ec7b1ea4aff18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885511"
---
# <a name="interrupt-time"></a>Tempo di interrupt

*Il tempo di* interruzione è la quantità di tempo dall'ultimo avvio del sistema, a intervalli di 100 nanosecondi. Il conteggio del tempo di interrupt inizia da zero all'avvio del sistema e viene incrementato a ogni interrupt di clock della lunghezza di un tick di clock. La lunghezza esatta di un tick di clock dipende dall'hardware sottostante e può variare da un sistema all'altro.

A [differenza dell'ora](system-time.md)di sistema, il conteggio dei tempi di interrupt non è soggetto a modifiche da parte degli utenti o del servizio ora di Windows, quindi è una scelta migliore per misurare le durate brevi. Le applicazioni che richiedono una maggiore precisione rispetto al conteggio dei tempi di interrupt devono usare un [timer ad alta risoluzione.](../winmsg/about-timers.md) Usare la [**funzione QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) per recuperare la frequenza del timer ad alta risoluzione e la [**funzione QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) per recuperare il valore del contatore.

Le funzioni [**QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) possono essere usate per recuperare il conteggio del tempo di interrupt. Tempo di interrupt non distorto significa che viene conteggiato solo il tempo in cui il sistema si trova nello stato di lavoro, pertanto il conteggio dei tempi di interrupt non viene "distorto" dal tempo trascorso dal sistema in sospensione o ibernazione.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP/2000:** La [**funzione QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) è disponibile a partire da Windows 7 e Windows Server 2008 R2.

La risoluzione del timer impostata dalle funzioni [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) influisce sulla risoluzione delle funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) e [**QueryUnbiasedInterruptTime.**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) Tuttavia, non è consigliabile aumentare la risoluzione del timer perché può ridurre le prestazioni complessive del sistema e aumentare il consumo di energia impedendo al processore di entrare negli stati di risparmio energia. Le applicazioni devono invece usare un timer ad alta risoluzione.

> [!Note]  
> Le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) producono risultati diversi nelle build di debug ("checked") di Windows, perché il conteggio tempo di interrupt e il conteggio dei tick sono avanzati di circa 49 giorni. Ciò consente di identificare i bug che potrebbero non verificarsi fino a quando il sistema non è in esecuzione da molto tempo. La build selezionata è disponibile per i sottoscrittori MSDN [tramite il sito Web Sviluppatore Microsoft Network (MSDN).](https://msdn.microsoft.com/default.aspx)

 

L'esempio seguente illustra come recuperare il conteggio dei tempi di interrupt chiamando le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . Collegamento alla libreria OneCore.lib quando si compila un'applicazione console che chiama queste funzioni.


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



Per recuperare il tempo trascorso che rappresenta la sospensione o l'ibernazione, usare la funzione [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) oppure usare il contatore delle prestazioni Tempo di esecuzione del sistema. Questo contatore delle prestazioni può essere recuperato dai dati sulle prestazioni nella chiave del Registro di sistema **HKEY \_ PERFORMANCE \_ DATA**. Il valore restituito è un valore a 8 byte. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

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

 

 
