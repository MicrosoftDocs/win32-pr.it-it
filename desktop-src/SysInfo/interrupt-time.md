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
# <a name="interrupt-time"></a><span data-ttu-id="c2af3-103">Tempo di interrupt</span><span class="sxs-lookup"><span data-stu-id="c2af3-103">Interrupt Time</span></span>

<span data-ttu-id="c2af3-104">Il *tempo di interrupt* è la quantità di tempo trascorso dall'ultimo avvio del sistema, in intervalli di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c2af3-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="c2af3-105">Il conteggio del tempo di interrupt inizia da zero all'avvio del sistema e viene incrementato a ogni interrupt del clock per la lunghezza di un tick dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="c2af3-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="c2af3-106">La lunghezza esatta di un tick dell'orologio dipende dall'hardware sottostante e può variare tra i sistemi.</span><span class="sxs-lookup"><span data-stu-id="c2af3-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="c2af3-107">A differenza dell' [ora di sistema](system-time.md), il conteggio dei tempi di interrupt non è soggetto a modifiche da parte degli utenti o del servizio ora di Windows, rendendolo la scelta migliore per la misurazione di durate brevi.</span><span class="sxs-lookup"><span data-stu-id="c2af3-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="c2af3-108">Le applicazioni che richiedono una maggiore precisione rispetto al numero di interrupt devono usare un [timer ad alta risoluzione](../winmsg/about-timers.md).</span><span class="sxs-lookup"><span data-stu-id="c2af3-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="c2af3-109">Utilizzare la funzione [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) per recuperare la frequenza del timer ad alta risoluzione e la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) per recuperare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="c2af3-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="c2af3-110">È possibile utilizzare le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) per recuperare il conteggio del tempo di interrupt.</span><span class="sxs-lookup"><span data-stu-id="c2af3-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="c2af3-111">Il tempo di interrupt non distorta indica che viene conteggiato solo il tempo in cui il sistema si trova nello stato di lavoro; pertanto, il numero di interruzioni del sistema non viene "distorta" entro il tempo di sospensione o di ibernazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="c2af3-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="c2af3-112">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP/2000:** La funzione [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) è disponibile a partire da Windows 7 e windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2af3-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="c2af3-113">La risoluzione del timer impostata dalle funzioni [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) influiscono sulla risoluzione delle funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) e [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) .</span><span class="sxs-lookup"><span data-stu-id="c2af3-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="c2af3-114">Tuttavia, non è consigliabile aumentare la risoluzione del timer perché può ridurre le prestazioni complessive del sistema e aumentare il consumo di energia impedendo al processore di accedere agli Stati di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="c2af3-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="c2af3-115">Al contrario, le applicazioni devono utilizzare un timer ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="c2af3-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="c2af3-116">Le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) producono risultati diversi per le compilazioni di debug ("verificate") di Windows, perché il conteggio dei tempi di interrupt e il numero di cicli sono avanzati di circa 49 giorni.</span><span class="sxs-lookup"><span data-stu-id="c2af3-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="c2af3-117">Ciò consente di identificare i bug che potrebbero non verificarsi fino a quando il sistema non è in esecuzione per molto tempo.</span><span class="sxs-lookup"><span data-stu-id="c2af3-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="c2af3-118">La compilazione selezionata è disponibile per gli abbonati MSDN tramite il sito Web [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c2af3-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="c2af3-119">Nell'esempio seguente viene illustrato come recuperare il conteggio del tempo di interrupt chiamando le funzioni [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) .</span><span class="sxs-lookup"><span data-stu-id="c2af3-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="c2af3-120">Collegarsi alla libreria OneCore. lib quando si compila un'applicazione console che chiama queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="c2af3-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


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



<span data-ttu-id="c2af3-121">Per recuperare il tempo trascorso per la sospensione o l'ibernazione, utilizzare la funzione [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) oppure utilizzare il contatore delle prestazioni del tempo di sistema.</span><span class="sxs-lookup"><span data-stu-id="c2af3-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="c2af3-122">Questo contatore delle prestazioni può essere recuperato dai dati sulle prestazioni nella chiave del registro di sistema **HKEY \_ \_ dati sulle prestazioni**.</span><span class="sxs-lookup"><span data-stu-id="c2af3-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="c2af3-123">Il valore restituito è un valore a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="c2af3-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="c2af3-124">Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="c2af3-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2af3-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2af3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2af3-126">**QueryInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="c2af3-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="c2af3-127">**QueryInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="c2af3-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="c2af3-128">**QueryUnbiasedInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="c2af3-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="c2af3-129">**QueryUnbiasedInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="c2af3-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="c2af3-130">**timeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="c2af3-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="c2af3-131">**timeEndPeriod**</span><span class="sxs-lookup"><span data-stu-id="c2af3-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
