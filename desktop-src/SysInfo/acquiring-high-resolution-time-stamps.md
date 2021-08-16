---
description: Windows api che è possibile usare per acquisire timestamp ad alta risoluzione o misurare intervalli di tempo.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Acquisizione di timestamp ad alta risoluzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e25c50cb602dd7e5c53c967c12321ec02a6ea68613767f4019b2def7f5793b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764625"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Acquisizione di timestamp ad alta risoluzione

Windows api che è possibile usare per acquisire timestamp ad alta risoluzione o misurare intervalli di tempo. L'API primaria per il codice nativo è [**QueryPerformanceCounter (QPC).**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Per i driver di dispositivo, l'API in modalità kernel è [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Per il codice gestito, la [**classe System.Diagnostics.Stopwatch**](/previous-versions/windows/) usa **QPC** come base temporale precisa.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è indipendente da e non è sincronizzato con alcun riferimento all'ora esterno. Per recuperare timestamp che possono essere sincronizzati con un riferimento ora esterno, ad esempio Coordinated Universal Time (UTC) per l'uso in misurazioni time-of-day ad alta risoluzione, usare [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

I timestamp e le misurazioni dell'intervallo di tempo sono parte integrante delle misurazioni delle prestazioni di computer e rete. Queste operazioni di misurazione delle prestazioni includono il calcolo del tempo di risposta, della velocità effettiva e della latenza, nonché la profilatura dell'esecuzione del codice. Ognuna di queste operazioni comporta una misurazione delle attività che si verificano durante un intervallo di tempo definito da un evento di inizio e di fine che può essere indipendente da qualsiasi riferimento esterno all'ora del giorno.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è in genere il metodo migliore da usare per gli eventi di timestamp e misurare piccoli intervalli di tempo che si verificano nello stesso sistema o macchina virtuale. Prendere in considerazione l'uso di [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) quando si vogliono impostare il timestamp degli eventi in più computer, a condizione che ogni computer partecipi a uno schema di sincronizzazione dell'ora, ad esempio NTP (Network Time Protocol). **QPC** consente di evitare difficoltà che possono verificarsi con altri approcci di misurazione del tempo, ad esempio la lettura diretta del contatore di timestamp del processore.

-   [Supporto QPC in Windows versioni](#qpc-support-in-windows-versions)
-   [Linee guida per l'acquisizione di timestamp](#guidance-for-acquiring-time-stamps)
    -   [Virtualizzazione](#virtualization)
    -   [Utilizzo diretto di TSC](#direct-tsc-usage)
    -   [Esempi per l'acquisizione di timestamp](#examples-for-acquiring-time-stamps)
-   [Domande frequenti generali su QPC e TSC](#general-faq-about-qpc-and-tsc)
-   [Domande frequenti sulla programmazione con QPC e TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Caratteristiche dell'orologio hardware di basso livello](#low-level-hardware-clock-characteristics)
    -   [Orologi assoluti e orologi di differenza](#absolute-clocks-and-difference-clocks)
    -   [Risoluzione, precisione, accuratezza e stabilità](#resolution-precision-accuracy-and-stability)
-   [Informazioni sul timer hardware](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Supporto QPC in Windows versioni

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è stato introdotto Windows 2000 e Windows XP e si è evoluto per sfruttare i miglioramenti della piattaforma hardware e dei processori. In questo articolo vengono descritte le caratteristiche di **QPC** in Windows diverse per gestire il software in esecuzione in tali Windows versioni.

### <a name="windows-xp-and-windows-2000"></a>Windows XP e Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è disponibile in Windows XP e Windows 2000 e funziona correttamente nella maggior parte dei sistemi. Tuttavia, il BIOS di alcuni sistemi hardware non indicava correttamente le caratteristiche della CPU hardware (un TSC non invariante) e alcuni sistemi multi-core o multiprocessore usava processori con TSC che non potevano essere sincronizzati tra core. I sistemi con firmware difettoso che eseguono queste versioni di Windows potrebbero non fornire la stessa lettura **QPC** su core diversi se usavano TSC come base per **QPC**.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista e Windows Server 2008

Tutti i computer forniti con Windows Vista e Windows Server 2008 hanno usato un contatore della piattaforma (High Precision Event Timer (HPET)) o il timer DI PM (ACPI Power Management Timer) come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Questi timer della piattaforma hanno una latenza di accesso più elevata rispetto a TSC e sono condivisi tra più processori. Ciò limita la scalabilità **di QPC** se viene chiamato contemporaneamente da più processori.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

La maggior parte dei computer Windows 7 e Windows Server 2008 R2 dispone di processori con TSC a velocità costante e usano questi contatori come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). I TSC sono contatori hardware per processore ad alta risoluzione a cui è possibile accedere con una latenza e un sovraccarico molto bassi (nell'ordine di 10 o 100 di cicli macchina, a seconda del tipo di processore). Windows 7 e Windows Server 2008 R2 usano ICC come base di **QPC** nei sistemi di dominio a clock singolo in cui il sistema operativo (o l'hypervisor) è in grado di sincronizzare strettamente i singoli TSC tra tutti i processori durante l'inizializzazione del sistema. In questi sistemi, il costo della lettura del contatore delle prestazioni è significativamente inferiore rispetto ai sistemi che usano un contatore della piattaforma. Inoltre, non si aggiunge alcun sovraccarico per le chiamate simultanee e le query in modalità utente spesso ignorano le chiamate di sistema, riducendo ulteriormente il sovraccarico. Nei sistemi in cui il TSC non è adatto per l'orario, Windows seleziona automaticamente un contatore della piattaforma (il timer HPET o il timer ACPI PM) come base per **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 usano i TSC come base per il contatore delle prestazioni. L'algoritmo di sincronizzazione TSC è stato notevolmente migliorato per supportare meglio sistemi di grandi dimensioni con molti processori. Inoltre, è stato aggiunto il supporto per la nuova API precisa dell'ora del giorno, che consente l'acquisizione di timestamp precisi dell'orologio a parete dal sistema operativo. Per altre informazioni, vedere [**GetSystemTimePreciseAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) Nelle Windows RT per PC, il contatore delle prestazioni è basato su un contatore della piattaforma proprietario o sul contatore di sistema fornito dal timer generico per PC Windows RT se la piattaforma è così dotata.

## <a name="guidance-for-acquiring-time-stamps"></a>Linee guida per l'acquisizione di timestamp

Windows ha e continuerà a investire per fornire un contatore delle prestazioni affidabile ed efficiente. Quando sono necessari timestamp con una risoluzione di 1 microsecondo o superiore e non è necessario sincronizzarli con un riferimento ora esterno, scegliere [**QueryPerformanceCounter,**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise). Quando sono necessari timestamp sincronizzati con UTC con una risoluzione di 1 microsecondo o superiore, scegliere [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) o [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

In un numero relativamente ridotto di piattaforme che non possono usare il registro TSC come base [**QPC,**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ad esempio, per motivi illustrati in Informazioni sul [timer](#hardware-timer-info)hardware, l'acquisizione di timestamp ad alta risoluzione può essere significativamente più costosa rispetto all'acquisizione di timestamp con risoluzione inferiore. Se la risoluzione da 10 a 16 millisecondi è sufficiente, è possibile usare [**GetTickCount64,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) [**QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryUnbiasedInterruptTime,**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)o [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) per ottenere timestamp non sincronizzati con un riferimento ora esterno. Per i timestamp sincronizzati con UTC, usare [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) o [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Se è necessaria una risoluzione più elevata, è possibile usare [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) per ottenere timestamp.

In generale, i risultati del contatore delle prestazioni sono coerenti tra tutti i processori nei sistemi multi-core e multiprocessore, anche se misurati su thread o processi diversi. Ecco alcune eccezioni a questa regola:

-   I sistemi operativi Windows Vista in esecuzione in determinati processori potrebbero violare questa coerenza per uno dei motivi seguenti:

    -   I processori hardware hanno un TSC non invariante e il BIOS non indica correttamente questa condizione.
    -   L'algoritmo di sincronizzazione TSC usato non era adatto per i sistemi con un numero elevato di processori.

-   Quando si confrontano i risultati del contatore delle prestazioni acquisiti da thread diversi, considerare i valori che differiscono ± 1 tick per avere un ordinamento ambiguo. Se i timestamp vengono prelevati dallo stesso thread, questa ±'incertezza di 1 tick non si applica. In questo contesto, il termine tick si riferisce a un periodo di tempo uguale a 1 ÷ (frequenza del contatore delle prestazioni ottenuto da [**QueryPerformanceFrequency).**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)

Quando si usa il contatore delle prestazioni in sistemi server di grandi dimensioni con domini a più orologi non sincronizzati nell'hardware, Windows determina che il TSC non può essere usato per scopi di temporizzazione e seleziona un contatore della piattaforma come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Anche se questo scenario produce ancora timestamp affidabili, la latenza di accesso e la scalabilità sono influenzate negativamente. Pertanto, come indicato in precedenza nelle indicazioni sull'utilizzo precedenti, usare solo le API che forniscono una risoluzione di 1 microsecondo o superiore quando tale risoluzione è necessaria. Il TSC viene usato come base per **QPC** nei sistemi di dominio multi clock che includono la sincronizzazione hardware di tutti i domini di clock del processore, perché in questo modo funzionano in modo efficace come un sistema di dominio a clock singolo.

La frequenza del contatore delle prestazioni è fissa all'avvio del sistema ed è coerente in tutti i processori, quindi è necessario eseguire una query solo sulla frequenza da [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) durante l'inizializzazione dell'applicazione e quindi memorizzare nella cache il risultato.

### <a name="virtualization"></a>Virtualizzazione

Il contatore delle prestazioni dovrebbe funzionare in modo affidabile in tutte le macchine virtuali guest in esecuzione su hypervisor implementati correttamente. Tuttavia, gli hypervisor conformi all'interfaccia hypervisor versione 1.0 e che espandono l'illuminazione dell'ora di riferimento possono offrire un overhead sostanzialmente inferiore. Per altre informazioni sulle interfacce e sulle funzionalità di hypervisor, vedere [Specifiche dell'hypervisor.](/virtualization/hyper-v-on-windows/reference/tlfs)

### <a name="direct-tsc-usage"></a>Utilizzo diretto di TSC

È fortemente sconsigliato usare l'istruzione del processore **RDTSC** o **RDTSCP** per eseguire direttamente query su TSC perché non si otterrà risultati affidabili in alcune versioni di Windows, nelle migrazioni in tempo reale delle macchine virtuali e nei sistemi hardware senza TSC invarianti o strettamente sincronizzati. È invece necessario usare [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) per sfruttare l'astrazione, la coerenza e la portabilità offerte.

### <a name="examples-for-acquiring-time-stamps"></a>Esempi per l'acquisizione di timestamp

I vari esempi di codice in queste sezioni illustrano come acquisire timestamp.

### <a name="using-qpc-in-native-code"></a>Uso di QPC nel codice nativo

Questo esempio illustra come usare [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) nel codice nativo C e C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Acquisizione di timestamp ad alta risoluzione dal codice gestito

Questo esempio illustra come usare la classe [**System.Diagnostics.Stopwatch del codice**](/previous-versions/windows/) gestito.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



La [**classe System.Diagnostics.Stopwatch**](/previous-versions/windows/) fornisce anche diversi metodi pratici per eseguire misurazioni dell'intervallo di tempo.

### <a name="using-qpc-from-kernel-mode"></a>Uso di QPC dalla modalità kernel

Il kernel Windows fornisce l'accesso in modalità kernel al contatore delle prestazioni [**tramite KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) da cui è possibile ottenere sia il contatore delle prestazioni che la frequenza delle prestazioni. **KeQueryPerformanceCounter** è disponibile solo in modalità kernel ed è disponibile per gli autori di driver di dispositivo e altri componenti in modalità kernel.

Questo esempio illustra come usare [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) in modalità kernel C e C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>Domande frequenti generali su QPC e TSC

Ecco le risposte alle domande frequenti su [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e TSC in generale.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**QueryPerformanceCounter() è uguale alla funzione Win32 GetTickCount() o GetTickCount64()?**
</dt> <dd>

No. [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) e [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) non sono correlati a [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) **GetTickCount** e **GetTickCount64** restituiscono il numero di millisecondi dall'avvio del sistema.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**È consigliabile usare QPC o chiamare direttamente le istruzioni RDTSC /RDTSCP?**
</dt> <dd>

Per evitare problemi di errato e portabilità, è consigliabile usare [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) invece di usare il registro TSC o le istruzioni del processore **RDTSC** o **RDTSCP.**

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Qual è la relazione di QPC con un'era temporale esterna? Può essere sincronizzato con un'era esterna, ad esempio UTC?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) si basa su un contatore hardware che non può essere sincronizzato con un riferimento ora esterno, ad esempio UTC. Per timestamp di ora precisi che possono essere sincronizzati con un riferimento UTC esterno, usare [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**QPC è interessato dall'ora legale, dai secondi intercalare, dai fusi orari o dalle modifiche all'ora di sistema apportate dall'amministratore?**
</dt> <dd>

No. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è completamente indipendente dall'ora di sistema e dall'ora UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**L'accuratezza QPC è influenzata dalle modifiche della frequenza del processore causate dalla tecnologia turbo boost o dal risparmio energia?**
</dt> <dd>

No. Se il processore ha un TSC invariante, [**il QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) non è interessato da questo tipo di modifiche. Se il processore non ha un TSC invariante, **QPC** ripristina un timer hardware della piattaforma che non sarà influenzato dalle modifiche della frequenza del processore o dalla tecnologia Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**QPC funziona in modo affidabile in sistemi multiprocessore, sistemi multi-core e sistemi con hyperthreading?**
</dt> <dd>

Sì

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Ricerca per categorie determinare e convalidare il funzionamento di QPC nel computer?**
</dt> <dd>

Non è necessario eseguire tali controlli.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Quali processori hanno TSC non invarianti? Come è possibile verificare se il sistema ha un TSC non invariante?**
</dt> <dd>

Non è necessario eseguire questo controllo manualmente. Windows sistemi operativi eseguono diversi controlli durante l'inizializzazione del sistema per determinare se TSC è adatto come base per [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Tuttavia, a scopo di riferimento, è possibile determinare se il processore ha un TSC invariante usando uno dei metodi seguenti:

-   Utilità Coreinfo.exe da Windows Sysinternals
-   controllo dei valori restituiti dall'istruzione CPUID relativa alle caratteristiche TSC
-   documentazione del produttore del processore

Di seguito vengono illustrate le informazioni TSC-INVARIANT fornite dall'utilità Windows Sysinternals Coreinfo.exe[ (www.sysinternals.com](https://www.sysinternals.com)). Un asterisco indica "True".

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**QPC funziona in modo affidabile nelle piattaforme hardware Windows RT PC?**
</dt> <dd>

Sì

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Con quale frequenza viene eseguito il roll over di QPC?**
</dt> <dd>

Non meno di 100 anni dall'avvio del sistema più recente e potenzialmente più lunghi in base al timer hardware sottostante usato. Per la maggior parte delle applicazioni, il rollover non è un problema.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Qual è il costo di calcolo della chiamata a QPC?**
</dt> <dd>

Il costo delle chiamate di calcolo [**di QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è determinato principalmente dalla piattaforma hardware sottostante. Se il registro TSC viene usato come base per QPC, il costo di calcolo è determinato principalmente dal tempo necessario al processore per elaborare **un'istruzione RDTSC.** Questo intervallo di tempo varia da 10 cicli di CPU a diverse centinaia di cicli di CPU a seconda del processore usato. Se non è possibile usare TSC, il sistema selezionerà una base temporale hardware diversa. Poiché queste basi tempo reale si trovano sulla scheda madre (ad esempio, sul bridge sud pci o PCH), il costo di calcolo per chiamata è superiore rispetto a TSC e si trova spesso in prossimità di microsecondi da 0,8 a 1,0 a seconda della velocità del processore e di altri fattori hardware. Questo costo dipende dal tempo necessario per accedere al dispositivo hardware sulla scheda madre.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**QPC richiede una transizione del kernel (chiamata di sistema)?**
</dt> <dd>

Non è necessaria una transizione del kernel se il sistema può usare il registro TSC come base per [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Se il sistema deve usare una base temporale diversa, ad esempio il timer HPET o PM, è necessaria una chiamata di sistema.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Il contatore delle prestazioni è monotonico (non decrescente)?**
</dt> <dd>

Sì

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**È possibile usare il contatore delle prestazioni per ordinare gli eventi nel tempo?**
</dt> <dd>

Sì. Tuttavia, quando si confrontano i risultati del contatore delle prestazioni acquisiti da thread diversi, i valori che differiscono per ± 1 tick hanno un ordinamento ambiguo come se avesse un timestamp identico.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Quanto è accurato il contatore delle prestazioni?**
</dt> <dd>

La risposta dipende da diversi fattori. Per altre informazioni, vedere [Caratteristiche dell'orologio hardware di basso livello.](#low-level-hardware-clock-characteristics)

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Domande frequenti sulla programmazione con QPC e TSC

Di seguito sono fornite le risposte alle domande frequenti sulla programmazione [**con QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e TSC.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**È necessario convertire l'output QPC in millisecondi. Come è possibile evitare la perdita di precisione con la conversione in double o float?**
</dt> <dd>

Quando si eseguono calcoli sui contatori delle prestazioni integer, è necessario tenere presenti diversi aspetti:

-   La divisione di interi perderà il resto. Ciò può causare una perdita di precisione in alcuni casi.
-   La conversione tra interi a 64 bit e a virgola mobile (double) può causare la perdita di precisione perché la mantissa a virgola mobile non può rappresentare tutti i valori integrali possibili.
-   La moltiplicazione di interi a 64 bit può comportare un overflow di integer.

Come principio generale, ritardare questi calcoli e conversioni il più a lungo possibile per evitare di compostare gli errori introdotti.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Come è possibile convertire QPC in tick di 100 nanosecondi in modo da poterlo aggiungere a UN FILETIME?**
</dt> <dd>

Un'ora del file è un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi trascorsi dalle 12:00 1 gennaio 1601 Coordinated Universal Time (UTC). Gli orari dei file vengono usati dalle chiamate API Win32 che restituiscono ora del giorno, ad esempio [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) e [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Al contrario, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) restituisce valori che rappresentano il tempo in unità di 1/(frequenza del contatore delle prestazioni ottenuto [**da QueryPerformanceFrequency).**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) La conversione tra i due richiede il calcolo del rapporto tra l'intervallo **QPC** e gli intervalli di 100 nanosecondi. Prestare attenzione a evitare la perdita di precisione perché i valori potrebbero essere piccoli (0,00000001 / 0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Perché il timestamp restituito da QPC è un intero con segno?**
</dt> <dd>

I calcoli che coinvolgono [**timestamp QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) possono comportare la sottrazione. Usando un valore con segno, è possibile gestire i calcoli che potrebbero produrre valori negativi.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Come è possibile ottenere timestamp ad alta risoluzione dal codice gestito?**
</dt> <dd>

Chiamare il [**metodo Stopwatch.GetTimeStamp**](/previous-versions/windows/) dalla [**classe System.Diagnostics.Stopwatch.**](/previous-versions/windows/) Per un esempio su come usare **Stopwatch.GetTimeStamp**, vedere Acquisizione di timestamp ad alta [risoluzione dal codice gestito.](#acquiring-high-resolution-time-stamps-from-managed-code)

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**In quali circostanze QueryPerformanceFrequency restituisce FALSE o QueryPerformanceCounter restituisce zero?**
</dt> <dd>

Questa operazione non si verifica in alcun sistema che esegue Windows XP o versioni successive.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**È necessario impostare l'affinità dei thread su un singolo core per usare QPC?**
</dt> <dd>

No. Per altre informazioni, vedere [Linee guida per l'acquisizione di timestamp.](#guidance-for-acquiring-time-stamps) Questo scenario non è necessario né auspicabile. L'esecuzione di questo scenario può influire negativamente sulle prestazioni dell'applicazione limitando l'elaborazione a un core o creando un collo di bottiglia in un singolo core se più thread impostano la propria affinità sullo stesso core quando si chiama [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Caratteristiche dell'orologio hardware di basso livello

Queste sezioni illustrano le caratteristiche dell'orologio hardware di basso livello.

### <a name="absolute-clocks-and-difference-clocks"></a>Orologi assoluti e orologi di differenza

Gli orologi assoluti forniscono letture accurate dell'ora del giorno. Sono in genere basati su Coordinated Universal Time (UTC) e di conseguenza la loro accuratezza dipende in parte dal livello di sincronizzazione con un riferimento all'ora esterno. Gli orologi delle differenze misurano gli intervalli di tempo e non sono in genere basati su un periodo di tempo esterno. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è un orologio di differenza e non viene sincronizzato con un periodo di tempo esterno o un riferimento. Quando si usa **QPC** per le misurazioni dell'intervallo di tempo, in genere si ottiene una precisione migliore rispetto a quella che si ottiene usando timestamp derivati da un orologio assoluto. Ciò è dovuto al fatto che il processo di sincronizzazione dell'ora di un orologio assoluto può introdurre cambiamenti di fase e frequenza che aumentano l'incertezza delle misurazioni a breve termine dell'intervallo di tempo.

### <a name="resolution-precision-accuracy-and-stability"></a>Risoluzione, precisione, accuratezza e stabilità

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contatore hardware come base. I timer hardware sono costituiti da tre parti: un generatore di tick, un contatore che conta i tick e un mezzo per recuperare il valore del contatore. Le caratteristiche di questi tre componenti determinano la risoluzione, la precisione, l'accuratezza e la stabilità di **QPC.**

Se un generatore di hardware fornisce tick a una velocità costante, gli intervalli di tempo possono essere misurati semplicemente contando questi tick. La frequenza con cui vengono generati i tick è detta frequenza ed espressa in Hertz (Hz). Il reciproco della frequenza è detto periodo o intervallo di tick ed è espresso in un'unità di tempo del sistema internazionale di unità (SI, International System of Units) appropriata, ad esempio secondo, millisecondo, microsecondo o nanosecondo.

![intervallo di tempo](images/tick-interval.png)

La risoluzione del timer è uguale al periodo. La risoluzione determina la possibilità di distinguere tra due timestamp qualsiasi e posiziona un limite inferiore sugli intervalli di tempo più piccoli che possono essere misurati. Questa operazione viene talvolta definita risoluzione del tick.

La misurazione digitale del tempo introduce un'incertezza delle misurazioni ± 1 tick perché il contatore digitale avanza in passaggi discreti, mentre il tempo avanza continuamente. Questa incertezza è detta errore di quantizzazione. Per le misurazioni tipiche dell'intervallo di tempo, questo effetto può spesso essere ignorato perché l'errore di quantizzazione è molto più piccolo dell'intervallo di tempo misurato.

![misurazione del tempo digitale](images/digital-time-measure.png)

Tuttavia, se il periodo misurato è ridotto e si avvicina alla risoluzione del timer, è necessario considerare questo errore di quantizzazione. La dimensione dell'errore introdotto è quella di un periodo di clock.

I due diagrammi seguenti illustrano l'impatto dell'incertezza ± 1 tick usando un timer con una risoluzione di 1 unità di tempo.

![tick incertezze](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) restituisce la frequenza [**di QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)e il periodo e la risoluzione sono uguali al reciproco di questo valore. La frequenza del contatore delle prestazioni restituita da **QueryPerformanceFrequency** viene determinata durante l'inizializzazione del sistema e non cambia durante l'esecuzione del sistema.

> [!Note]  
> Potrebbero esistere casi in cui [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) non restituisce la frequenza effettiva del generatore di tick hardware. In molti casi, ad esempio, **QueryPerformanceFrequency** restituisce la frequenza TSC divisa per 1024. e in Hyper-V, la frequenza del contatore delle prestazioni è sempre di 10 MHz quando la macchina virtuale guest viene eseguita in un [hypervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) che implementa l'interfaccia [hypervisor versione 1.0.](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx) Di conseguenza, non presupporre che **QueryPerformanceFrequency** restituisca la frequenza TSC precisa.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) legge il contatore delle prestazioni e restituisce il numero totale di tick che si sono verificati dall'avvio del sistema operativo Windows, incluso l'ora in cui il computer era in stato di sospensione, ad esempio standby, ibernazione o standby connesso.

Questi esempi illustrano come calcolare l'intervallo di tick e la risoluzione e come convertire il conteggio dei tick in un valore temporale.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Esempio 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) restituisce il valore 3.125.000 in un computer specifico. Qual è l'intervallo di tick e la risoluzione [**delle misurazioni QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) in questo computer? L'intervallo di tick, o periodo, è il reciproco di 3.125.000, ovvero 0,000000320 (320 nanosecondi). Pertanto, ogni tick rappresenta il passaggio di 320 nanosecondi. Gli intervalli di tempo inferiori a 320 nanosecondi non possono essere misurati in questo computer.

Tick Interval = 1/(Frequenza prestazioni)

Tick Interval = 1/3.125.000 = 320 ns

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Esempio 2**
</dt> <dd>

Nello stesso computer dell'esempio precedente, la differenza dei valori restituiti da due chiamate successive a [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è 5. Quanto tempo è trascorso tra le due chiamate? 5 tick moltiplicati per 320 nanosecondi producono 1,6 microsecondi.

ElapsedTime = Ticks \* Tick Interval

ElapsedTime = 5 \* 320 ns = 1,6 μs

</dd> </dl>

È necessario tempo per accedere (leggere) il contatore tick dal software e questo tempo di accesso può ridurre la precisione della misurazione del tempo. Ciò è dovuto al fatto che l'intervallo minimo (l'intervallo di tempo più piccolo che può essere misurato) è maggiore della risoluzione e del tempo di accesso.

Precisione = RISOLUZIONE \[ MASSIMA, AccessTime\]

Si consideri ad esempio un ipotetico timer hardware con una risoluzione di 100 nanosecondi e un tempo di accesso di 800 nanosecondi. Questo potrebbe essere il caso in cui è stato usato il timer della piattaforma anziché il registro TSC come base di [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) La precisione sarebbe quindi di 800 nanosecondi e non di 100 nanosecondi, come illustrato in questo calcolo.

Precisione = MAX \[ 800 ns,100 ns \] = 800 ns

Queste due figure illustrano questo effetto.

![Tempo di accesso qpc](images/qpc-access-time.png)

Se il tempo di accesso è maggiore della risoluzione, non provare a migliorare la precisione con l'ipotesi. In altre parole, è un errore presupporre che il timestamp sia preso esattamente al centro o all'inizio o alla fine della chiamata.

Si consideri invece l'esempio seguente in cui il tempo di accesso [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è di soli 20 nanosecondi e la risoluzione dell'orologio hardware è di 100 nanosecondi. Questo potrebbe essere il caso in cui il registro TSC è stato usato come base per **QPC.** In questo caso la precisione è limitata dalla risoluzione dell'orologio.

![Precisione qpc](images/qpc-precision.png)

In pratica, è possibile trovare le origini tempo per cui il tempo necessario per leggere il contatore è maggiore o minore della risoluzione. In entrambi i casi, la precisione sarà maggiore delle due.

Questa tabella fornisce informazioni sulla risoluzione approssimativa, sull'ora di accesso e sulla precisione di un'ampia gamma di orologi. Si noti che alcuni valori variano a seconda dei processori, delle piattaforme hardware e delle velocità del processore.



| Origine dell'orologio                                                      | Frequenza di clock nominale | Risoluzione dell'orologio    | Ora di accesso (tipico) | Precisione       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| PC RTC                                                            | 64 Hz                   | 15,625 millisecondi | N/D                   | N/D             |
| Contatore delle prestazioni delle query con TSC con un clock del processore a 3 GHz  | 3 MHz                   | 333 nanosecondi     | 30 nanosecondi        | 333 nanosecondi |
| Istruzioni del computer **RDTSC** in un sistema con un tempo di ciclo di 3 GHz | 3 GHz                   | 333 picosecondi     | 30 nanosecondi        | 30 nanosecondi  |



 

Poiché [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contatore hardware, quando si comprendono alcune caratteristiche di base dei contatori hardware, si acquisisce una conoscenza delle funzionalità e delle limitazioni di **QPC.**

Il generatore di tick hardware più comunemente usato è un oscillatore di cristallo. Il cristallo è un piccolo frammento di quarzo o di altro materiale dipinta che presenta caratteristiche piezoelettriche che forniscono un riferimento di frequenza economico con eccellente stabilità e accuratezza. Questa frequenza viene usata per generare i tick conteggiati dall'orologio.

L'accuratezza di un timer si riferisce al grado di conformità a un valore true o standard. Ciò dipende principalmente dalla capacità dell'oscillatore di cristallo di fornire segni di graduazione alla frequenza specificata. Se la frequenza di oscillazione è troppo elevata, l'orologio verrà eseguito rapidamente e gli intervalli misurati verranno visualizzati più a lungo di quanto non siano realmente. e se la frequenza è troppo bassa, l'orologio verrà eseguito lentamente e gli intervalli misurati verranno visualizzati più brevi di quanto non siano realmente.

Per le misurazioni tipiche dell'intervallo di tempo per una breve durata (ad esempio, misurazioni del tempo di risposta, misurazioni della latenza di rete e così via), l'accuratezza dell'oscillatore hardware è in genere sufficiente. Tuttavia, per alcune misurazioni, l'accuratezza della frequenza dell'oscillatore diventa importante, in particolare per lunghi intervalli di tempo o quando si vogliono confrontare le misurazioni prese in computer diversi. Nella parte restante di questa sezione vengono esaminati gli effetti dell'accuratezza dell'oscillatore.

La frequenza di oscillazione dei cristallo viene impostata durante il processo di produzione ed è specificata dal produttore in termini di una frequenza specificata più o meno una tolleranza di produzione espressa in "parti per milione" (ppm), denominata offset di frequenza massima. Un cristallo con una frequenza specificata di 1.000.000 Hz e un offset di frequenza massimo di ± 10 ppm rientra nei limiti di specifica se la frequenza effettiva è compresa tra 999.990 Hz e 1.000.010 Hz.

Sostituendo le parti della frase per milione con microsecondi al secondo, è possibile applicare questo errore di offset di frequenza alle misurazioni dell'intervallo di tempo. Un oscillatore con un offset + 10 ppm avrebbe un errore di 10 microsecondi al secondo. Di conseguenza, quando si misura un intervallo di 1 secondo, viene eseguito rapidamente e misura un intervallo di 1 secondo come 0,9999990 secondi.

Un riferimento pratico è che un errore di frequenza di 100 ppm causa un errore di 8,64 secondi dopo 24 ore. Questa tabella presenta l'incertezza di misurazione dovuta all'errore accumulato per intervalli di tempo più lunghi.



| Durata intervallo di tempo | Incertezza delle misurazioni dovuta a errori accumulati con +/- 10 PPM tolleranza di frequenza |
|------------------------|--------------------------------------------------------------------------------------|
| 1 microsecondo          | ± 10 picosecondi (10-12)                                                             |
| 1 millisecondo          | ± 10 nanosecondi (10-9)                                                              |
| 1 secondo               | ± 10 microsecondi                                                                    |
| 1 ora                 | ± 60 microsecondi                                                                    |
| 1 giorno                  | ± 0,86 secondi                                                                       |
| 1 settimana                 | ± 6,08 secondi                                                                       |



 

La tabella precedente mostra che per intervalli di tempo di piccole dimensioni l'errore di offset della frequenza può spesso essere ignorato. Tuttavia, per lunghi intervalli di tempo, anche una piccola differenza di frequenza può causare una notevole incertezza di misurazione.

Gli oscillatori di cristallo usati nei personal computer e nei server vengono in genere prodotti con una tolleranza di frequenza di ± 30-50 parti per milione e raramente i cristallo possono essere spenti fino a 500 ppm. Anche se sono disponibili cristallo con tolleranze di offset di frequenza molto più rigide, sono più costosi e quindi non vengono usati nella maggior parte dei computer.

Per ridurre gli effetti negativi di questo errore di offset della frequenza, le versioni recenti di Windows, in particolare Windows 8, usano più timer hardware per rilevare l'offset di frequenza e compensare tale offset nella misura possibile. Questo processo di calibrazione viene eseguito all Windows viene avviato.

Come illustrato negli esempi seguenti, l'errore di offset della frequenza di un clock hardware influisce sull'accuratezza ottenibile e la risoluzione dell'orologio può essere meno importante.

![l'errore di offset della frequenza influisce sull'accuratezza ottenibile](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Esempio 1**
</dt> <dd>

Si supponga di eseguire misurazioni dell'intervallo di tempo usando un oscillatore da 1 MHz, che ha una risoluzione di 1 microsecondo e un errore di offset di frequenza massima di ±50 ppm. Si supponga ora che l'offset sia esattamente +50 ppm. Ciò significa che la frequenza effettiva sarà 1.000.050 Hz. Se si misurasse un intervallo di tempo di 24 ore, la misurazione sarebbe troppo breve di 4,3 secondi (23:59:55.7000000 misurata rispetto alle 24:00:00.0000000 effettive).

Secondi al giorno = 86400

Errore di offset della frequenza = 50 ppm = 0,00005

86.400 secondi \* 0,00005 = 4,3 secondi

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Esempio 2**
</dt> <dd>

Si supponga che l'orologio TSC del processore sia controllato da un oscillatore a sfera e abbia una frequenza specificata di 3 GHz. Ciò significa che la risoluzione sarà 1/3.000.000.000 o circa 333 millisecondi. Si supponga che il cristallo usato per controllare l'orologio del processore abbia una tolleranza di frequenza di ±50 ppm e sia effettivamente +50 ppm. Nonostante la risoluzione eccezionale, una misurazione dell'intervallo di tempo di 24 ore sarà ancora troppo breve di 4,3 secondi. (23:59:55.700000000000 misurate rispetto a 24:00:00.000000000000 effettive).

Secondi al giorno = 86400

Errore di offset della frequenza = 50 ppm = 0,00005

86.400 secondi \* 0,00005 = 4,3 secondi

Ciò indica che un orologio TSC ad alta risoluzione non fornisce necessariamente misurazioni più accurate rispetto a un orologio con risoluzione inferiore.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Esempio 3**
</dt> <dd>

Prendere in considerazione l'uso di due computer diversi per misurare lo stesso intervallo di tempo di 24 ore. Entrambi i computer hanno un oscillatore con un offset di frequenza massima ± 50 ppm. A quale distanza può essere la misurazione dello stesso intervallo di tempo in questi due sistemi? Come negli esempi precedenti, ± 50 ppm genera un errore massimo di ± 4,3 secondi dopo 24 ore. Se un sistema viene eseguito con una velocità di 4,3 secondi e l'altro lento di 4,3 secondi, l'errore massimo dopo 24 ore potrebbe essere di 8,6 secondi.

Secondi al giorno = 86400

Errore di offset della frequenza = ±50 ppm = ±0.00005

±(86.400 secondi \* 0,00005) = ±4,3 secondi

Offset massimo tra i due sistemi = 8,6 secondi

In sintesi, l'errore di offset della frequenza diventa sempre più importante quando si misurano intervalli di tempo lunghi e quando si confrontano le misurazioni tra sistemi diversi.

La stabilità di un timer descrive se la frequenza dei segni di graduazione cambia nel tempo, ad esempio in seguito a variazioni delle temperature. I quartz generatori usati come generatori di segni di graduazione nei computer presenteranno piccole variazioni nella frequenza in funzione della temperatura. L'errore causato dalla deriva termica è in genere ridotto rispetto all'errore di offset della frequenza per gli intervalli di temperatura comuni. Tuttavia, i progettisti di software per apparecchiature portatili o apparecchiature soggette a fluttuazioni di temperatura di grandi dimensioni potrebbero dover prendere in considerazione questo effetto.

</dd> </dl>

## <a name="hardware-timer-info"></a>Informazioni sul timer hardware

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Registro TSC**
</dt> <dd>

Alcuni processori Intel e AMD contengono un registro TSC che è un registro a 64 bit che aumenta a una velocità elevata, in genere uguale al clock del processore. Il valore di questo contatore può essere letto tramite le istruzioni del computer **RDTSC** o **RDTSCP,** fornendo tempi di accesso e costi di calcolo molto bassi nell'ordine di decine o centinaia di cicli di computer, a seconda del processore.

Anche se il registro TSC sembra un meccanismo di timestamp ideale, ecco alcune circostanze in cui non può funzionare in modo affidabile per scopi di timekeeping:

-   Non tutti i processori hanno registri TSC, quindi l'uso del registro TSC nel software crea direttamente un problema di portabilità. In Windows verrà selezionata un'origine ora alternativa per [**QPC,**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) evitando così il problema di portabilità.
-   Alcuni processori possono variare la frequenza del clock TSC o arrestare l'avanzamento del registro TSC, il che rende TSC non adatto per scopi di temporizzazione in questi processori. Si dice che questi processori hanno registri TSC non invarianti. (Windows rileva automaticamente questo problema e seleziona un'origine ora alternativa per [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
-   Nei sistemi multiprocessore o multi-core, alcuni processori e sistemi non sono in grado di sincronizzare gli orologi in ogni core con lo stesso valore. (Windows rileva automaticamente questo problema e seleziona un'origine ora alternativa per [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
-   In alcuni sistemi multiprocessore di grandi dimensioni, potrebbe non essere possibile sincronizzare i clock del processore con lo stesso valore anche se il processore ha un TSC invariante. (Windows rileva automaticamente questo problema e seleziona un'origine ora alternativa per [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
-   Alcuni processori eseguiranno istruzioni non in ordine. Ciò può comportare conteggi di cicli non corretti quando **RDTSC** viene usato per le sequenze di istruzioni tempormente perché l'istruzione **RDTSC** potrebbe essere eseguita in un momento diverso da quello specificato nel programma. **L'istruzione RDTSCP** è stata introdotta in alcuni processori in risposta a questo problema.

Analogamente ad altri timer, il TSC si basa su un oscillatore a sfera la cui frequenza esatta non è nota in anticipo e che presenta un errore di offset della frequenza. Pertanto, prima di poter essere usato, deve essere calibrato usando un altro riferimento di temporizzazione.

Durante l'inizializzazione del Windows verifica se TSC è adatto per scopi di temporizzazione ed esegue la calibrazione della frequenza e la sincronizzazione di base necessarie.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Orologio PM**
</dt> <dd>

Il timer ACPI, noto anche come orologio PM, è stato aggiunto all'architettura di sistema per fornire timestamp affidabili indipendentemente dalla velocità dei processori. Poiché questo era l'unico obiettivo di questo timer, fornisce un timestamp in un singolo ciclo di clock, ma non fornisce altre funzionalità.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**HPET Timer**
</dt> <dd>

Il High Precision Event Timer (HPET) è stato sviluppato congiuntamente da Intel e Microsoft per soddisfare i requisiti di temporizzazione dei contenuti multimediali e di altre applicazioni sensibili al tempo. Il supporto HPET è stato Windows da Windows Vista e la certificazione del logo hardware Windows 7 e Windows 8 richiede il supporto HPET nella piattaforma hardware.

</dd> </dl>

 

 
