---
description: Windows fornisce le API che è possibile usare per acquisire indicatori temporali ad alta risoluzione o misurare gli intervalli di tempo.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Acquisizione di timestamp ad alta risoluzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968749"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Acquisizione di timestamp ad alta risoluzione

Windows fornisce le API che è possibile usare per acquisire indicatori temporali ad alta risoluzione o misurare gli intervalli di tempo. L'API primaria per il codice nativo è [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Per i driver di dispositivo, l'API in modalità kernel è [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Per il codice gestito, la classe [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) USA **QPC** come base di tempo precisa.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è indipendente da e non è sincronizzato con un riferimento all'ora esterno. Per recuperare i timestamp che possono essere sincronizzati con un riferimento ora esterno, ad esempio l'ora UTC (Coordinated Universal Time) per l'uso in misurazioni temporali ad alta risoluzione, usare [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

I timestamp e le misurazioni di intervallo di tempo sono parte integrante delle misurazioni delle prestazioni di rete e del computer. Queste operazioni di misurazione delle prestazioni includono il calcolo del tempo di risposta, della velocità effettiva e della latenza, nonché dell'esecuzione del codice di profilatura. Ognuna di queste operazioni comporta una misurazione delle attività che si verificano durante un intervallo di tempo definito da un evento di inizio e di fine che può essere indipendente da qualsiasi riferimento all'ora del giorno esterno.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è in genere il metodo migliore da usare per gli eventi timestamp e misurare intervalli di tempo ridotti che si verificano nello stesso sistema o nella stessa macchina virtuale. Si consiglia di usare [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) quando si desidera eseguire il timestamp degli eventi tra più computer, purché ogni computer partecipi a uno schema di sincronizzazione dell'ora, ad esempio Network Time Protocol (NTP). **QPC** consente di evitare le difficoltà che possono verificarsi con altri approcci di misurazione del tempo, ad esempio la lettura diretta del contatore del timestamp del processore (TSC).

-   [Supporto di QPC nelle versioni di Windows](#qpc-support-in-windows-versions)
-   [Linee guida per l'acquisizione di timestamp](#guidance-for-acquiring-time-stamps)
    -   [Virtualizzazione](#virtualization)
    -   [Utilizzo diretto di TSC](#direct-tsc-usage)
    -   [Esempi per l'acquisizione di timestamp](#examples-for-acquiring-time-stamps)
-   [Domande frequenti generali su QPC e TSC](#general-faq-about-qpc-and-tsc)
-   [Domande frequenti sulla programmazione con QPC e TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Caratteristiche del clock hardware di basso livello](#low-level-hardware-clock-characteristics)
    -   [Orologi assoluti e orologi di differenza](#absolute-clocks-and-difference-clocks)
    -   [Risoluzione, precisione, accuratezza e stabilità](#resolution-precision-accuracy-and-stability)
-   [Informazioni sul timer hardware](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Supporto di QPC nelle versioni di Windows

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è stato introdotto in Windows 2000 e Windows XP ed è stato sviluppato per sfruttare i miglioramenti apportati alla piattaforma hardware e ai processori. Di seguito vengono descritte le caratteristiche di **QPC** su diverse versioni di Windows per semplificare la manutenzione del software in esecuzione in tali versioni di Windows.

### <a name="windows-xp-and-windows-2000"></a>Windows XP e Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è disponibile in Windows XP e Windows 2000 e funziona bene nella maggior parte dei sistemi. Tuttavia, alcuni sistemi hardware ' BIOS non indicano correttamente le caratteristiche della CPU hardware (un TSC non invariante) e alcuni sistemi multicore o multiprocessore hanno usato processori con TSCs che non potevano essere sincronizzati tra i core. I sistemi con firmware difettoso che eseguono queste versioni di Windows potrebbero non fornire lo stesso **QPC** di lettura su core diversi se hanno usato il TSC come base per **QPC**.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista e Windows Server 2008

Tutti i computer forniti con Windows Vista e Windows Server 2008 usavano un contatore della piattaforma (High Precision Event Timer (HPET)) o il timer di risparmio energia ACPI (timer PM) come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Questi timer di piattaforma hanno una latenza di accesso superiore rispetto al TSC e sono condivisi tra più processori. Questo limita la scalabilità di **QPC** se viene chiamata simultaneamente da più processori.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

La maggior parte dei computer Windows 7 e Windows Server 2008 R2 dispone di processori con TSCs a frequenza costante e usa questi contatori come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). TSCs sono contatori hardware ad alta risoluzione a cui è possibile accedere con latenza molto bassa e overhead (nell'ordine di decine o centinaia di cicli del computer, a seconda del tipo di processore). Windows 7 e Windows Server 2008 R2 usano TSCs come base di **QPC** nei sistemi di dominio a Clock singolo in cui il sistema operativo (o l'hypervisor) è in grado di sincronizzare strettamente i singoli TSCS tra tutti i processori durante l'inizializzazione del sistema. In tali sistemi, il costo della lettura del contatore delle prestazioni è significativamente inferiore rispetto ai sistemi che utilizzano un contatore della piattaforma. Inoltre, non vi è alcun sovraccarico aggiuntivo per le chiamate simultanee e le query in modalità utente ignorano spesso le chiamate di sistema, riducendo ulteriormente il sovraccarico. Nei sistemi in cui il TSC non è adatto per il cronometraggio, Windows seleziona automaticamente un contatore della piattaforma (il timer HPET o il timer di PM ACPI) come base per **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 usano TSCs come base per il contatore delle prestazioni. L'algoritmo di sincronizzazione TSC è stato significativamente migliorato per supportare al meglio i sistemi di grandi dimensioni con molti processori. È stato inoltre aggiunto il supporto per la nuova API di Time-of-Day precisa, che consente di acquisire timestamp precisi dal sistema operativo. Per altre informazioni, vedere [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Nelle piattaforme PC Windows RT, il contatore delle prestazioni si basa su un contatore della piattaforma proprietario o sul contatore di sistema fornito dal timer generico Windows RT PC se la piattaforma è così attrezzata.

## <a name="guidance-for-acquiring-time-stamps"></a>Linee guida per l'acquisizione di timestamp

Windows ha e continuerà a investire nella fornitura di un contatore delle prestazioni affidabile ed efficiente. Quando sono necessari timestamp con una risoluzione di 1 microsecondo o superiore e non sono necessari i timestamp da sincronizzare con un riferimento ora esterno, scegliere [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise). Quando sono necessari timestamp con sincronizzazione UTC con una risoluzione di 1 microsecondo o superiore, scegliere [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) o [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

In un numero relativamente ridotto di piattaforme che non possono usare il registro TSC come base [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , ad esempio, per i motivi illustrati nelle [informazioni sul timer hardware](#hardware-timer-info), l'acquisizione di timestamp ad alta risoluzione può essere notevolmente più costosa rispetto all'acquisizione di timestamp con risoluzione inferiore. Se è sufficiente la risoluzione da 10 a 16 millisecondi, è possibile usare [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)o [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) per ottenere i timestamp non sincronizzati con un riferimento ora esterno. Per gli indicatori di ora UTC sincronizzati, utilizzare [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) o [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Se è necessaria una risoluzione più elevata, è possibile usare [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) per ottenere i timestamp.

In generale, i risultati dei contatori delle prestazioni sono coerenti in tutti i processori nei sistemi multicore e multiprocessore, anche se misurati in thread o processi diversi. Di seguito sono riportate alcune eccezioni a questa regola:

-   I sistemi operativi precedenti a Windows Vista eseguiti su determinati processori potrebbero violare questa coerenza a causa di uno dei motivi seguenti:

    -   I processori hardware hanno un TSC non invariante e il BIOS non indica correttamente questa condizione.
    -   L'algoritmo di sincronizzazione TSC utilizzato non era adatto per i sistemi con un numero elevato di processori.

-   Quando si confrontano i risultati dei contatori delle prestazioni acquisiti da thread diversi, prendere in considerazione i valori che differiscono per ± 1, per avere un ordinamento ambiguo. Se gli indicatori di data e ora vengono ricavati dallo stesso thread, l'incertezza di ± 1 non viene applicata. In questo contesto, il termine segno si riferisce a un periodo di tempo uguale a 1 ÷ (la frequenza del contatore delle prestazioni ottenuto da [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).

Quando si usa il contatore delle prestazioni in sistemi server di grandi dimensioni con domini a più clock che non sono sincronizzati nell'hardware, Windows determina che il TSC non può essere usato a scopo di temporizzazione e seleziona un contatore della piattaforma come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Sebbene questo scenario produca comunque indicatori di tempo affidabili, la latenza e la scalabilità dell'accesso sono compromesse. Pertanto, come indicato in precedenza nelle linee guida per l'utilizzo precedenti, usare solo le API che forniscono una soluzione microsecondo o migliore quando è necessaria una risoluzione di questo tipo. Il TSC viene usato come base per **QPC** nei sistemi di dominio a più clock che includono la sincronizzazione hardware di tutti i domini di clock del processore, in quanto ciò li rende effettivamente funzioni come un unico sistema di dominio di clock.

La frequenza del contatore delle prestazioni è fissa all'avvio del sistema ed è coerente in tutti i processori, quindi è sufficiente eseguire una query sulla frequenza da [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) durante l'inizializzazione dell'applicazione e quindi memorizzare nella cache il risultato.

### <a name="virtualization"></a>Virtualizzazione

Il contatore delle prestazioni dovrebbe funzionare in modo affidabile in tutte le macchine virtuali guest eseguite in hypervisor correttamente implementati. Tuttavia, gli hypervisor che sono conformi all'interfaccia dell'hypervisor versione 1,0 e la superficie dell'Illuminismo del tempo di riferimento possono offrire un sovraccarico notevolmente inferiore. Per ulteriori informazioni sulle interfacce hypervisor e sugli illuminamenti, vedere [specifiche hypervisor](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Utilizzo diretto di TSC

È fortemente sconsigliato l'uso dell'istruzione del processore **RDTSC** o **rdtscp (** per eseguire direttamente una query sul TSC perché non si ottengono risultati affidabili in alcune versioni di Windows, tra migrazioni in tempo reale di macchine virtuali e su sistemi hardware senza invariante o con TSCS strettamente sincronizzati. Si consiglia invece di usare [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) per sfruttare l'astrazione, la coerenza e la portabilità che offre.

### <a name="examples-for-acquiring-time-stamps"></a>Esempi per l'acquisizione di timestamp

I vari esempi di codice in queste sezioni illustrano come acquisire timestamp.

### <a name="using-qpc-in-native-code"></a>Uso di QPC nel codice nativo

Questo esempio Mostra come usare [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) in codice nativo C e C++.


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

Questo esempio illustra come usare la classe [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) di codice gestito.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



La classe [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) fornisce anche diversi metodi pratici per eseguire misure di intervallo di tempo.

### <a name="using-qpc-from-kernel-mode"></a>Uso di QPC dalla modalità kernel

Il kernel di Windows fornisce l'accesso in modalità kernel al contatore delle prestazioni tramite [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) da cui è possibile ottenere sia il contatore delle prestazioni che la frequenza delle prestazioni. **KeQueryPerformanceCounter** è disponibile solo in modalità kernel e viene fornito per writer di driver di dispositivo e altri componenti in modalità kernel.

Questo esempio Mostra come usare [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) in modalità kernel C e C++.


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

Di seguito sono riportate le risposte alle domande frequenti su [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e TSCS in generale.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**QueryPerformanceCounter () è uguale alla funzione Win32 GetTickCount () o GetTickCount64 ()?**
</dt> <dd>

No. [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) e [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) non sono correlati a [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). **GetTickCount** e **GetTickCount64** restituiscono il numero di millisecondi trascorsi dall'avvio del sistema.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**È consigliabile usare QPC o chiamare direttamente le istruzioni/RDTSCP RDTSC?**
</dt> <dd>

Per evitare problemi di correttezza e portabilità, è consigliabile usare [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) invece di usare il registro TSC o le istruzioni del processore **RDTSC** o **rdtscp (** .

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Qual è la relazione di QPC con un periodo di tempo esterno? Può essere sincronizzato con un'Epoch esterna, ad esempio UTC?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) si basa su un contatore hardware che non può essere sincronizzato con un riferimento all'ora esterno, ad esempio UTC. Per gli indicatori di data e ora specifici che possono essere sincronizzati con un riferimento UTC esterno, usare [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**QPC è influenzato dall'ora legale, dai secondi intercalari, dai fusi orari o dalle modifiche dell'ora di sistema apportate dall'amministratore?**
</dt> <dd>

No. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è completamente indipendente dall'ora di sistema e dall'ora UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**QPC è influenzato dall'accuratezza delle modifiche della frequenza del processore dovute alla tecnologia di risparmio energia o Turbo Boost?**
</dt> <dd>

No. Se il processore ha un TSC invariante, il [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) non è interessato da queste modifiche. Se il processore non ha un TSC invariante, **QPC** verrà ripristinato un timer hardware della piattaforma che non sarà influenzato dalle modifiche della frequenza del processore o dalla tecnologia Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**QPC funziona in modo affidabile su sistemi multiprocessore, sistema multicore e sistemi con Hyper-Threading?**
</dt> <dd>

Sì

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Ricerca per categorie determinare e verificare che QPC funzioni nel computer?**
</dt> <dd>

Non è necessario eseguire tali controlli.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Quali processori hanno TSCs non invarianti? Come è possibile verificare se il sistema dispone di un TSC non invariante?**
</dt> <dd>

Non è necessario eseguire questa verifica. I sistemi operativi Windows eseguono diversi controlli nell'inizializzazione del sistema per determinare se il TSC è adatto come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Tuttavia, a scopo di riferimento, è possibile determinare se il processore ha un TSC invariante utilizzando uno dei seguenti:

-   utilità Coreinfo.exe da Windows Sysinternals
-   Verifica dei valori restituiti dall'istruzione CPUID relativa alle caratteristiche TSC
-   documentazione del produttore del processore

Di seguito sono illustrate le informazioni relative a TSC-Invariant fornite dall'utilità Coreinfo.exe di Windows Sysinternals ([www.sysInternals.com](https://www.sysinternals.com)). Un asterisco indica "true".

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

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**QPC funziona in modo affidabile sulle piattaforme hardware del PC Windows RT?**
</dt> <dd>

Sì

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Con quale frequenza viene eseguito il rollover di QPC?**
</dt> <dd>

Non meno di 100 anni dall'avvio del sistema più recente e potenzialmente più lungo a seconda del timer hardware sottostante utilizzato. Per la maggior parte delle applicazioni, il rollover non è un problema.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Qual è il costo computazionale della chiamata a QPC?**
</dt> <dd>

Il costo di chiamata computazionale di [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è determinato principalmente dalla piattaforma hardware sottostante. Se il registro TSC viene usato come base per QPC, il costo di calcolo è determinato principalmente dal tempo impiegato dal processore per elaborare un'istruzione **RDTSC** . Questo intervallo di tempo va da 10 a 10 cicli CPU a centinaia di cicli di CPU a seconda del processore usato. Se non è possibile utilizzare il TSC, il sistema selezionerà un tempo hardware diverso. Poiché queste basi temporali si trovano sulla scheda madre (ad esempio, sul Bridge PCI meridionale o PCH), il costo di calcolo per chiamata è superiore a quello del TSC e spesso è in prossimità di 0,8-1,0 microsecondi a seconda della velocità del processore e di altri fattori hardware. Questo costo è dominato dal tempo necessario per accedere al dispositivo hardware sulla scheda madre.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**QPC richiede una transizione del kernel (chiamata di sistema)?**
</dt> <dd>

Non è necessaria una transizione del kernel se il sistema è in grado di usare il registro TSC come base per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Se il sistema deve usare una base temporale diversa, ad esempio il timer HPET o PM, è necessaria una chiamata di sistema.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Il contatore delle prestazioni è monotonico (non decrescente)?**
</dt> <dd>

Sì

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**Il contatore delle prestazioni può essere utilizzato per ordinare gli eventi in tempo?**
</dt> <dd>

Sì. Tuttavia, quando si confrontano i risultati dei contatori delle prestazioni acquisiti da thread diversi, i valori che differiscono per ± 1 segno di selezione hanno un ordinamento ambiguo come se avessero un timestamp identico.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Quanto è preciso il contatore delle prestazioni?**
</dt> <dd>

La risposta dipende da diversi fattori. Per altre informazioni, vedere [caratteristiche del clock hardware di basso livello](#low-level-hardware-clock-characteristics).

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Domande frequenti sulla programmazione con QPC e TSC

Di seguito sono riportate le risposte alle domande frequenti sulla programmazione con [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e tscs.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**È necessario convertire l'output QPC in millisecondi. Come è possibile evitare la perdita di precisione con la conversione a Double o float?**
</dt> <dd>

Esistono diversi aspetti da tenere presenti quando si eseguono calcoli su contatori di prestazioni Integer:

-   La divisione di interi perderà il resto. In alcuni casi può causare la perdita di precisione.
-   La conversione tra interi a 64 bit e virgola mobile (Double) può causare la perdita di precisione perché il mantissa a virgola mobile non può rappresentare tutti i valori integrali possibili.
-   La moltiplicazione degli Integer a 64 bit può causare un overflow di Integer.

Come principio generale, ritardare questi calcoli e conversioni il più a lungo possibile per evitare la composizione degli errori introdotti.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Come è possibile convertire QPC in cicli di 100 nanosecondi in modo che sia possibile aggiungerli a un FILETIME?**
</dt> <dd>

Un'ora di file è un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi trascorsi da 12:00 A.M. 1 gennaio 1601 Coordinated Universal Time (UTC). Gli orari dei file vengono usati dalle chiamate API Win32 che restituiscono l'ora del giorno, ad esempio [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) e [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Al contrario, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) restituisce i valori che rappresentano il tempo in unità di 1/(la frequenza del contatore delle prestazioni ottenuto da [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)). Per la conversione tra i due è necessario calcolare il rapporto tra l'intervallo di **QPC** e gli intervalli di 100 nanosecondi. Prestare attenzione per evitare di perdere la precisione perché i valori possono essere di dimensioni ridotte (0,0000001/0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Perché il timestamp restituito da QPC è un intero con segno?**
</dt> <dd>

I calcoli che coinvolgono [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) timestamp possono comportare la sottrazione. Utilizzando un valore con segno, è possibile gestire calcoli che potrebbero produrre valori negativi.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Come è possibile ottenere indicatori temporali ad alta risoluzione dal codice gestito?**
</dt> <dd>

Chiamare il metodo [**Stopwatch. GetTimestamp**](/previous-versions/windows/) dalla classe [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) . Per un esempio su come usare **Stopwatch. GetTimestamp**, vedere [acquisizione di timestamp ad alta risoluzione dal codice gestito](#acquiring-high-resolution-time-stamps-from-managed-code).

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**In quali circostanze QueryPerformanceFrequency restituisce FALSE oppure QueryPerformanceCounter restituisce zero?**
</dt> <dd>

Questa operazione non si verifica in alcun sistema che esegue Windows XP o versione successiva.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**È necessario impostare l'affinità di thread su un singolo core per usare QPC?**
</dt> <dd>

No. Per altre informazioni, vedere [linee guida per l'acquisizione dei timestamp](#guidance-for-acquiring-time-stamps). Questo scenario non è necessario né auspicabile. L'esecuzione di questo scenario può influire negativamente sulle prestazioni dell'applicazione limitando l'elaborazione a un core o creando un collo di bottiglia in un singolo core se più thread impostano la loro affinità allo stesso nucleo quando chiamano [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Caratteristiche del clock hardware di basso livello

In queste sezioni vengono illustrate le caratteristiche del clock hardware di basso livello.

### <a name="absolute-clocks-and-difference-clocks"></a>Orologi assoluti e orologi di differenza

Gli orologi assoluti forniscono letture accurate per l'ora del giorno. Si basano in genere sull'ora UTC (Coordinated Universal Time) e, di conseguenza, la loro accuratezza dipende in parte dal modo in cui vengono sincronizzate con un riferimento all'ora esterna. Gli orologi di differenza misurano gli intervalli di tempo e non sono in genere basati su un periodo di tempo esterno. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è un clock di differenza e non viene sincronizzato con un periodo di tempo o un riferimento esterno. Quando si usa **QPC** per le misurazioni di intervallo di tempo, in genere si ottiene una maggiore precisione di quanto si otterrebbe usando i timestamp derivati da un clock assoluto. Questo è dovuto al fatto che il processo di sincronizzazione dell'ora di un clock assoluto può introdurre turni di fase e frequenza che aumentano l'incertezza delle misurazioni a breve termine di intervallo di tempo.

### <a name="resolution-precision-accuracy-and-stability"></a>Risoluzione, precisione, accuratezza e stabilità

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contatore hardware come base. I timer hardware sono costituiti da tre parti: un generatore di cicli, un contatore che conta i cicli e un mezzo per recuperare il valore del contatore. Le caratteristiche di questi tre componenti determinano la risoluzione, la precisione, l'accuratezza e la stabilità dei **QPC**.

Se un generatore di hardware fornisce i cicli a una velocità costante, è possibile misurare gli intervalli di tempo semplicemente contando questi cicli. La frequenza con cui vengono generati i cicli è detta frequenza e espressa in Hertz (Hz). Il reciproco della frequenza è denominato intervallo del periodo o del segno ed è espresso in un'unità di tempo del sistema internazionale (SI) appropriata (ad esempio, secondo, millisecondo, microsecondo o nanosecondo).

![intervallo di tempo](images/tick-interval.png)

La risoluzione del timer è uguale al punto. La risoluzione determina la possibilità di distinguere tra due timestamp e inserisce un limite inferiore per gli intervalli di tempo più piccoli che possono essere misurati. Questa operazione viene a volte definita risoluzione del ciclo.

La misurazione digitale del tempo introduce un'incertezza delle misurazioni di ± 1 segno di avanzamento perché il contatore digitale avanza in passaggi discreti, mentre il tempo continua a avanzare. Questa incertezza è detta errore di quantizzazione. Per le misurazioni tipiche dell'intervallo di tempo, questo effetto può spesso essere ignorato perché l'errore di quantizzazione è molto più piccolo dell'intervallo di tempo misurato.

![misurazione del tempo digitale](images/digital-time-measure.png)

Tuttavia, se il periodo misurato è ridotto e si avvicina alla risoluzione del timer, sarà necessario prendere in considerazione questo errore di quantizzazione. La dimensione dell'errore introdotta è quella di un periodo di clock.

I due diagrammi seguenti illustrano l'effetto dell'incertezza di ± 1 segno di incertezza usando un timer con una risoluzione di 1 unità di tempo.

![incertezze del segno di incertezza](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) restituisce la frequenza di [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)e il periodo e la risoluzione sono uguali al reciproco di questo valore. La frequenza del contatore delle prestazioni restituita da **QueryPerformanceFrequency** viene determinata durante l'inizializzazione del sistema e non cambia mentre il sistema è in esecuzione.

> [!Note]  
> Potrebbero esistere casi in cui [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) non restituisce la frequenza effettiva del generatore di cicli hardware. In molti casi, ad esempio, **QueryPerformanceFrequency** restituisce la frequenza TSC divisa per 1024; in Hyper-V, la frequenza del contatore delle prestazioni è sempre 10 MHz quando la macchina virtuale guest viene eseguita con un [hypervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) che implementa l' [interfaccia hypervisor versione 1,0](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx). Di conseguenza, non presupporre che **QueryPerformanceFrequency** restituirà la frequenza TSC precisa.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) legge il contatore delle prestazioni e restituisce il numero totale di cicli verificatisi dopo l'avvio del sistema operativo Windows, inclusa la data e l'ora in cui il computer si trova in uno stato di sospensione, ad esempio standby, ibernazione o standby connesso.

In questi esempi viene illustrato come calcolare l'intervallo e la risoluzione del segno di cadenza e come convertire il conteggio dei cicli in un valore di ora.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Esempio 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) restituisce il valore 3.125.000 in un computer specifico. Qual è l'intervallo di cicli e la risoluzione delle misurazioni [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) nel computer? L'intervallo di cicli, o punto, è il reciproco di 3.125.000, ovvero 0,000000320 (320 nanosecondi). Ogni segno di selezione rappresenta pertanto il superamento di 320 nanosecondi. Non è possibile misurare intervalli di tempo inferiori a 320 nanosecondi in questo computer.

Intervallo di cicli = 1/(frequenza delle prestazioni)

Intervallo di cicli = 1/3125000 = 320 NS

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Esempio 2**
</dt> <dd>

Nello stesso computer dell'esempio precedente, la differenza tra i valori restituiti da due chiamate successive a [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è 5. Quanto tempo è trascorso tra le due chiamate? 5 cicli moltiplicati per 320 nanosecondi generano 1,6 microsecondi.

ElapsedTime = intervallo di \* cicli

ElapsedTime = 5 \* 320 NS = 1,6 μs

</dd> </dl>

È necessario tempo per accedere (leggere) al contatore dei segni di indicizzazione dal software e questo tempo di accesso può ridurre la precisione della misurazione del tempo. Questo è dovuto al fatto che il tempo minimo di intervallo, ovvero l'intervallo di tempo più piccolo che è possibile misurare, è maggiore della risoluzione e del tempo di accesso.

Precisione = \[ risoluzione massima, AccessTime\]

Si consideri, ad esempio, un ipotetico timer hardware con una risoluzione di 100 nanosecondi e un tempo di accesso di 800 nanosecondi. Questo potrebbe essere il caso in cui il timer della piattaforma è stato usato al posto del registro TSC come base di [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Quindi, la precisione sarà di 800 nanosecondi non 100 nanosecondi, come illustrato in questo calcolo.

Precisione = MAX \[ 800 ns, 100 NS \] = 800 ns

Queste due figure rappresentano questo effetto.

![QPC tempo di accesso](images/qpc-access-time.png)

Se il tempo di accesso è maggiore della risoluzione, non provare a migliorare la precisione indovinando. In altre parole, è un errore supporre che il timestamp venga assunto con precisione al centro o all'inizio o alla fine della chiamata.

Al contrario, si consideri l'esempio seguente in cui il tempo di accesso di [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) è solo 20 nanosecondi e la risoluzione dell'orologio hardware è di 100 nanosecondi. Questo potrebbe essere il caso in cui il registro TSC è stato usato come base per **QPC**. Qui la precisione è limitata dalla risoluzione dell'orologio.

![precisione QPC](images/qpc-precision.png)

In pratica, è possibile trovare origini temporali per le quali il tempo necessario per la lettura del contatore è maggiore o minore della risoluzione. In entrambi i casi, la precisione sarà il più grande dei due.

Questa tabella fornisce informazioni sulla risoluzione approssimativa, il tempo di accesso e la precisione di diversi orologi. Si noti che alcuni valori variano a seconda della velocità del processore, delle piattaforme hardware e dei processori.



| Origine Clock                                                      | Frequenza di clock nominale | Risoluzione del clock    | Tempo di accesso (tipico) | Precision       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| RTC DEL PC                                                            | 64 Hz                   | 15,625 millisecondi | N/D                   | N/D             |
| Contatore delle prestazioni delle query con TSC con clock del processore a 3 GHz  | 3 MHz                   | 333 nanosecondi     | 30 nanosecondi        | 333 nanosecondi |
| **RDTSC** le istruzioni del computer in un sistema con una durata del ciclo di 3 GHz | 3 GHz                   | 333 picosecondi     | 30 nanosecondi        | 30 nanosecondi  |



 

Poiché [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) utilizza un contatore hardware, quando si conoscono alcune caratteristiche di base dei contatori hardware, è possibile ottenere informazioni sulle funzionalità e le limitazioni di **QPC**.

Il generatore di cicli hardware più comunemente usato è un oscillatore di cristallo. Il cristallo è una piccola parte di quarzo o altro materiale ceramico che presenta le caratteristiche piezoelettrici che forniscono un riferimento di frequenza economico con una stabilità e un'accuratezza ottimali. Questa frequenza viene utilizzata per generare i tick conteggiati dal clock.

L'accuratezza di un timer si riferisce al grado di conformità a un valore true o standard. Questo dipende principalmente dalla capacità di Crystal Oscillator di fornire segni di scanditura alla frequenza specificata. Se la frequenza delle oscillazioni è troppo elevata, il clock verrà eseguito in modo rapido e gli intervalli misurati verranno visualizzati più a lungo di quanto siano effettivamente. Se la frequenza è troppo bassa, il clock verrà eseguito lentamente e gli intervalli misurati verranno visualizzati più a breve di quanto siano effettivamente.

Per le misure tipiche di intervallo di tempo per la durata breve (ad esempio, misure del tempo di risposta, misure di latenza di rete e così via), l'accuratezza dell'oscillatore hardware è in genere sufficiente. Per alcune misure, tuttavia, l'accuratezza della frequenza Oscillator diventa importante, in particolare per intervalli di tempo lunghi o quando si desidera confrontare le misurazioni eseguite su computer diversi. Nella parte restante di questa sezione vengono esaminati gli effetti dell'accuratezza dell'oscillatore.

La frequenza delle oscillazioni dei cristalli viene impostata durante il processo di produzione e viene specificata dal produttore in termini di una frequenza specificata più o meno una tolleranza di produzione espressa in ' parti per milione ' (ppm), denominata offset frequenza massima. Un cristallo con una frequenza specificata di 1 milione Hz e un offset di frequenza massima pari a ± 10 ppm è entro i limiti della specifica se la frequenza effettiva è compresa tra 999.990 Hz e 1.000.010 Hz.

Sostituendo le parti di frase per milione con microsecondi al secondo, è possibile applicare questo errore di offset della frequenza alle misure di intervallo di tempo. Un oscillatore con un offset di + 10 ppm avrà un errore di 10 microsecondi al secondo. Di conseguenza, quando si misura un intervallo di 1 secondo, l'esecuzione viene eseguita velocemente e viene misurato un intervallo di 1 secondo come 0,999990 secondi.

Un riferimento utile è che un errore di frequenza di 100 ppm causa un errore di 8,64 secondi dopo 24 ore. Questa tabella presenta l'incertezza di misurazione a causa dell'errore accumulato per intervalli di tempo più lunghi.



| Durata intervallo di tempo | Incertezza di misurazione dovuta a un errore accumulato con tolleranza di frequenza di +/-10 PPM |
|------------------------|--------------------------------------------------------------------------------------|
| 1 microsecondo          | ± 10 picosecondi (10-12)                                                             |
| 1 millisecondo          | ± 10 nanosecondi (10-9)                                                              |
| 1 secondo               | ± 10 microsecondi                                                                    |
| 1 ora                 | microsecondi da ± 60                                                                    |
| 1 giorno                  | ± 0,86 secondi                                                                       |
| 1 settimana                 | ± 6,08 secondi                                                                       |



 

La tabella precedente mostra che per intervalli di tempo ridotti è spesso possibile ignorare l'errore di offset della frequenza. Tuttavia, per intervalli di tempo prolungati, anche un offset di frequenza ridotto può comportare un'incertezza sostanziale della misura.

Gli oscillatori cristallini usati in Personal computer e server vengono in genere prodotti con una tolleranza di frequenza di ± 30 a 50 parti per milione e raramente i cristalli possono essere spenti fino a 500 ppm. Sebbene i cristalli con una maggiore tolleranza di offset di frequenza siano disponibili, sono più costosi e pertanto non vengono usati nella maggior parte dei computer.

Per ridurre gli effetti negativi di questo errore di offset della frequenza, le versioni recenti di Windows, in particolare Windows 8, usano più timer hardware per rilevare l'offset della frequenza e compensarlo nella misura massima possibile. Questo processo di calibrazione viene eseguito all'avvio di Windows.

Come illustrato negli esempi seguenti, l'errore di offset della frequenza di un orologio hardware influisce sull'accuratezza ottenibile e la risoluzione dell'orologio può essere meno importante.

![l'errore di offset della frequenza influenza la precisione ottenibile](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Esempio 1**
</dt> <dd>

Si supponga di eseguire misure di intervallo di tempo usando un oscillatore di 1 MHz, che ha una risoluzione di 1 microsecondo e un errore di offset della frequenza massima pari a ± 50 ppm. A questo punto, supponiamo che l'offset sia esattamente + 50 ppm. Ciò significa che la frequenza effettiva sarebbe 1.000.050 Hz. Se è stato misurato un intervallo di tempo di 24 ore, la misura sarà di 4,3 secondi troppo breve (23:59:55.700000 misurato rispetto a 24:00:00.000000 effettivo).

Secondi in un giorno = 86400

Errore di offset frequenza = 50 ppm = 0,00005

86.400 secondi \* 0,00005 = 4,3 secondi

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Esempio 2**
</dt> <dd>

Si supponga che il clock TSC del processore sia controllato da un oscillatore di cristallo e che abbia una frequenza di 3 GHz specificata. Ciò significa che la risoluzione sarà 1/3000000000 o circa 333 picosecondi. Si supponga che il cristallo usato per controllare il clock del processore abbia una tolleranza di frequenza pari a ± 50 ppm ed è effettivamente + 50 ppm. Nonostante la risoluzione impressionante, una misurazione del periodo di tempo di 24 ore sarà ancora di 4,3 secondi troppo breve. (23:59:55.7000000000 misurato rispetto a 24:00:00.0000000000 effettivo).

Secondi in un giorno = 86400

Errore di offset frequenza = 50 ppm = 0,00005

86.400 secondi \* 0,00005 = 4,3 secondi

Questo mostra che un orologio TSC a risoluzione elevata non fornisce necessariamente misurazioni più accurate rispetto a un clock di risoluzione inferiore.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Esempio 3**
</dt> <dd>

Prendere in considerazione l'utilizzo di due computer diversi per misurare lo stesso intervallo di tempo di 24 ore. Entrambi i computer hanno un oscillatore con un offset di frequenza massima pari a ± 50 ppm. Quanto è possibile che la misurazione dello stesso intervallo di tempo in questi due sistemi sia diversa? Come negli esempi precedenti, ± 50 ppm restituisce un errore massimo di ± 4,3 secondi dopo 24 ore. Se un sistema esegue rapidamente 4,3 secondi e l'altro è lento di 4,3 secondi, l'errore massimo dopo 24 ore potrebbe essere 8,6 secondi.

Secondi in un giorno = 86400

Errore di offset frequenza = ± 50 ppm = ± 0,00005

± (86.400 secondi \* 0,00005) = ± 4,3 secondi

Offset massimo tra i due sistemi = 8,6 secondi

In breve, l'errore di offset della frequenza diventa sempre più importante quando si misurano intervalli di tempo lunghi e quando si confrontano le misurazioni tra sistemi diversi.

La stabilità di un timer indica se la frequenza del segno di variazione viene modificata nel tempo, ad esempio in seguito a variazioni di temperatura. I cristalli di quarzo usati come generatori di cicli sui computer mostreranno piccole variazioni di frequenza come funzione di temperatura. L'errore causato dalla deriva termica è in genere di piccole dimensioni rispetto all'errore di offset della frequenza per intervalli di temperature comuni. Tuttavia, i progettisti di software per apparecchiature portatili o apparecchiature soggette a fluttuazioni di temperatura elevate potrebbero dover considerare questo effetto.

</dd> </dl>

## <a name="hardware-timer-info"></a>Informazioni sul timer hardware

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Registro TSC**
</dt> <dd>

Alcuni processori Intel e AMD contengono un registro TSC che è un registro a 64 bit che aumenta a una frequenza elevata, in genere uguale al clock del processore. Il valore di questo contatore può essere letto tramite le istruzioni del computer **RDTSC** o **rdtscp (** , fornendo tempi di accesso molto bassi e costi di calcolo nell'ordine di decine o centinaia di cicli del computer, a seconda del processore.

Sebbene il registro TSC sembri un meccanismo di timestamp ideale, di seguito sono riportati alcuni casi in cui non può funzionare in modo affidabile ai fini del cronometraggio:

-   Non tutti i processori hanno registri TSC, quindi l'uso del registro TSC nel software crea direttamente un problema di portabilità. In questo caso, in Windows verrà selezionata un'origine dell'ora alternativa per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , che evita il problema di portabilità.
-   Alcuni processori possono variare la frequenza dell'orologio TSC o arrestare l'avanzamento del registro TSC, rendendo il TSC non adatto ai fini della temporizzazione di questi processori. Questi processori hanno un registro TSC non invariante. (Windows rileva automaticamente questo e selezionare un'origine ora alternativa per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Nei sistemi multiprocessore o multicore, alcuni processori e sistemi non sono in grado di sincronizzare gli orologi di ogni core con lo stesso valore. (Windows rileva automaticamente questo e selezionare un'origine ora alternativa per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   In alcuni sistemi multiprocessori di grandi dimensioni, potrebbe non essere possibile sincronizzare gli orologi del processore con lo stesso valore anche se il processore ha un TSC invariante. (Windows rileva automaticamente questo e selezionare un'origine ora alternativa per [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Alcuni processori eseguiranno istruzioni non ordinate. Questo può comportare un numero di cicli errato quando **RDTSC** viene usato per le sequenze di istruzioni temporali perché l'istruzione **RDTSC** potrebbe essere eseguita in un momento diverso rispetto a quanto specificato nel programma. L'istruzione **rdtscp (** è stata introdotta in alcuni processori in risposta a questo problema.

Analogamente ad altri timer, il TSC si basa su un oscillatore di cristallo la cui frequenza esatta non è nota in anticipo e che presenta un errore di offset della frequenza. Quindi, prima di poterlo usare, è necessario che venga calibrato usando un altro riferimento temporizzato.

Durante l'inizializzazione del sistema, Windows controlla se il TSC è adatto ai fini della temporizzazione ed esegue la taratura di frequenza e la sincronizzazione di base necessarie.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Clock PM**
</dt> <dd>

Il timer ACPI, noto anche come clock PM, è stato aggiunto all'architettura di sistema per fornire indicatori di tempo affidabili indipendentemente dalla velocità dei processori. Poiché questo è l'obiettivo singolo di questo timer, fornisce un timestamp in un singolo ciclo di clock, ma non fornisce altre funzionalità.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**Timer HPET**
</dt> <dd>

Il High Precision Event Timer (HPET) è stato sviluppato congiuntamente da Intel e Microsoft per soddisfare i requisiti di temporizzazione di applicazioni multimediali e di altre applicazioni sensibili al tempo. Il supporto di HPET è stato in Windows da Windows Vista e la certificazione del logo hardware di Windows 7 e Windows 8 richiede il supporto di HPET nella piattaforma hardware.

</dd> </dl>

 

 
