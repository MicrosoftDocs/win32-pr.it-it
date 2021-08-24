---
title: Provider di sistema
description: Abilitare gli eventi del provider di traccia di sistema con EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 46c141c6449594b8030ce24bb901b0afede33f3f6e2cefcaa36f4df4bf0dde0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812151"
---
# <a name="system-providers"></a>Provider di sistema
 
A partire da Windows 10 SDK build 20348, gli eventi del provider di traccia di sistema possono essere abilitati allo stesso modo di altri provider ETW, con [EnableTraceEx2.](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)  I diversi flag e [maschere di gruppo](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associati al provider di traccia di sistema sono stati mappati a nuovi provider di traccia, denominati provider di sistema, e parole chiave corrispondenti.  
 
Analogamente all'abilitazione diretta del provider di traccia di sistema, i provider di sistema possono essere abilitati solo da una sessione con [il EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) impostato.

## <a name="system-provider-reference"></a>Informazioni di riferimento sul provider di sistema

* [Provider ALPC di sistema](#system-alpc-provider)
* [Provider di configurazione di sistema](#system-config-provider)
* [Provider CPU di sistema](#system-cpu-provider)
* [Provider hypervisor di sistema](#system-hypervisor-provider)
* [Provider di interrupt di sistema](#system-interrupt-provider)
* [Provider di I/O di sistema](#system-io-provider)
* [Provider di filtri I/O di sistema](#system-io-filter-provider)
* [Provider di blocchi di sistema](#system-lock-provider)
* [Provider di memoria di sistema](#system-memory-provider)
* [Provider di oggetti di sistema](#system-object-provider)
* [System Power Provider](#system-power-provider)
* [Provider di processi di sistema](#system-process-provider)
* [Provider di profili di sistema](#system-profile-provider)
* [Provider del Registro di sistema](#system-registry-provider)
* [Provider dell'Utilità di pianificazione di sistema](#system-scheduler-provider)
* [Provider Syscall di sistema](#system-syscall-provider)
* [Provider timer di sistema](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>Provider ALPC di sistema

Fornisce eventi correlati al sistema ALPC.

GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC, EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>Provider di configurazione di sistema 

Fornisce eventi di configurazione del sistema.

GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>Provider CPU di sistema 

Fornisce eventi correlati alla CPU.

GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>Provider hypervisor di sistema 

Fornisce eventi relativi all'hypervisor.

GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>Provider di interrupt di sistema 

Fornisce eventi relativi a DPC e interrupt.

GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC, EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>Provider di I/O di sistema 

Fornisce eventi relativi a più tipi di I/O, tra cui disco, cache e rete.

GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP |

Nota: l'abilitazione SYSTEM_IO_KW_DRIVERS la parola chiave SYSTEM_IO_KW_FILENAME automaticamente.  Il SYSTEM_IO_KW_FILENAME viene attivato automaticamente anche quando il provider di memoria di sistema è abilitato con la parola chiave SYSTEM_MEMORY_KW_MEMORY.
 
### <a name="system-io-filter-provider"></a>Provider di filtri I/O di sistema 

Fornisce eventi correlati al filtro di I/O, inclusi tempi ed errori.

GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>Provider di blocchi di sistema 

Fornisce eventi relativi ai meccanismi di blocco del kernel.

GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>Provider di memoria di sistema 

Fornisce eventi relativi al gestore della memoria.

GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP |

Note: 
* L'abilitazione SYSTEM_MEMORY_KW_MEMORY parola chiave abilita automaticamente SYSTEM_IO_KW_FILENAME nel provider di I/O di sistema.
* Gli eventi abilitati dal SYSTEM_MEMORY_KW_POOL supportano un filtro tag pool, per scrivere in modo selettivo gli eventi solo per determinati tag del pool.  Viene configurato come filtro [schematizzato nel](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) provider di memoria di sistema.  Il filtro PoolTag viene costruito come segue:

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* Il [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) deve essere inizializzato con Id impostato su SYSTEM_MEMORY_POOL_FILTER_ID e il campo size impostato sulla dimensione di Header più la parte usata della matrice PoolTags.  

* Ogni tag del pool è una stringa di 4 caratteri archiviata come ULONG nel filtro.  
 
 
### <a name="system-object-provider"></a>Provider di oggetti di sistema 

Fornisce eventi relativi a Object Manager.

GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>System Power Provider 

Fornisce eventi relativi allo stato di alimentazione del sistema.

GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>Provider di processi di sistema 

Fornisce eventi relativi al processo, incluse le informazioni sulla durata, gli eventi di caricamento delle immagini e gli eventi correlati ai thread.

GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB, EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD, EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>Provider di profili di sistema 

Fornisce eventi di profilatura.

GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>Provider del Registro di sistema 

Fornisce eventi relativi al Registro di sistema.

GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>Provider dell'Utilità di pianificazione di sistema 

Fornisce eventi relativi all'utilità di pianificazione.

GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STARVATION | PERF_ANTI_STARVATION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>Provider Syscall di sistema 

Fornisce eventi con informazioni sulle chiamate di sistema.

GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>Provider timer di sistema 

Fornisce eventi relativi ai timer nel kernel.

GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}

| Parola chiave | Flag e gruppi legacy corrispondenti |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>Commenti

Questo nuovo meccanismo di abilitazione si aggiunge ai metodi preesistnti per abilitare questi eventi.  Qualsiasi codice usato in genere continuerà a eseguire questa operazione.
 
Gli eventi generati dal provider di traccia di sistema non cambiano a causa di questa nuova funzionalità.  Ciò significa che gli eventi restituiti non vengono contrassegnati come generati dai singoli provider di sistema.
 
Per altre informazioni sul GUID del provider e sulle definizioni delle parole chiave, [vedere evntrace.h.](/windows/win32/api/evntrace/)

## <a name="see-also"></a>Vedere anche

[Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)

[Intestazione evntrace.h](/windows/win32/api/evntrace/)