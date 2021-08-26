---
description: In questo argomento vengono elencate le strutture utilizzate con processi, thread, processori, oggetti processo e pianificazione in modalità utente (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Strutture di processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5893340c72ee46eff43b16db936025fbb5463fbe0cc10e2eba1829962269d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081381"
---
# <a name="process-and-thread-structures"></a>Strutture di processi e thread

In questo argomento vengono elencate le strutture utilizzate con processi, thread, processori, oggetti processo e pianificazione in modalità utente (UMS).

## <a name="process-and-thread-structures"></a>Strutture di processi e thread

Le strutture seguenti vengono usate con processi e thread:

-   [**INFORMAZIONI SULLA \_ MEMORIA \_ DELL'APP**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**STATO \_ AR**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**DESCRITTORE \_ CACHE**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**CONTATORI DI \_ I/O**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**PREFERENZA DI \_ ORIENTAMENTO**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**Peb**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**PEB \_ LDR \_ DATA**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**INFORMAZIONI SUL \_ PROCESSO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**ELABORARE \_ LE INFORMAZIONI \_ SULL'ESAURIMENTO DELLA \_ MEMORIA**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**CRITERI \_ \_ ASLR DI MITIGAZIONE \_ DEI PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**CRITERI DI \_ FIRMA \_ BINARIA DI \_ MITIGAZIONE \_ DEI PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**CRITERI DI \_ PROTEZIONE DEL FLUSSO DI CONTROLLO DI \_ \_ \_ MITIGAZIONE \_ DEI PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**CRITERI DEP \_ DI \_ MITIGAZIONE DEI \_ PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**CRITERI DEL \_ CODICE DINAMICO PER LA \_ \_ MITIGAZIONE DEI \_ PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**CRITERIO DI \_ DISABILITAZIONE \_ DEL PUNTO DI ESTENSIONE \_ DI \_ MITIGAZIONE DEI \_ PROCESSI**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**CRITERIO DI \_ DISABILITAZIONE DEL \_ TIPO DI CARATTERE DI \_ ATTENUAZIONE DEL \_ PROCESSO**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**CRITERI DI \_ CARICAMENTO DELLE IMMAGINI DI \_ \_ MITIGAZIONE \_ DEI PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**CRITERI DI \_ CONTROLLO HANDLE STRICT DI \_ \_ MITIGAZIONE \_ DEI \_ PROCESSI**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**PROCESS \_ MITIGATION \_ SYSTEM \_ CALL \_ DISABLE \_ POLICY**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**PARAMETRI DEL PROCESSO UTENTE RTL \_ \_ \_**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Strutture del processore

Le strutture seguenti vengono usate con processori e gruppi di processori:

-   [**RELAZIONE \_ CACHE**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**AFFINITÀ \_ DI GRUPPO**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**RELAZIONE DI \_ GRUPPO**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**RELAZIONE TRA NODI NUMA \_ \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**INFORMAZIONI SUL \_ GRUPPO \_ DI PROCESSORI**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**NUMERO \_ PROCESSORE**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**RELAZIONE \_ PROCESSORE**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**INFORMAZIONI SUL \_ SET DI CPU DI \_ \_ SISTEMA**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**INFORMAZIONI SUL \_ PROCESSORE \_ LOGICO DI \_ SISTEMA**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**INFORMAZIONI SUL \_ \_ PROCESSORE LOGICO \_ DI SISTEMA \_ AD ESEMPIO**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Struttura della coda del dispatcher

La struttura seguente viene usata per creare un [oggetto DispatcherQueueController.](/uwp/api/windows.system.dispatcherqueuecontroller)

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Strutture degli oggetti processo

Con gli oggetti processo vengono utilizzate le strutture seguenti:

-   [**PORTA DI COMPLETAMENTO \_ \_ ASSOCIATA \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**INFORMAZIONI DI BASE \_ \_ SULL'ACCOUNTING JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**INFORMAZIONI DI BASE SU JOBOBJECT \_ \_ E \_ \_ I/O \_ ACCOUNTING**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**INFORMAZIONI SUI LIMITI \_ DI BASE \_ DI JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**ELENCO DI \_ ID PROCESSO \_ DI BASE \_ JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**RESTRIZIONI \_ DELL'INTERFACCIA UTENTE \_ DI BASE \_ DI JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**INFORMAZIONI \_ SULL'ORA \_ DI FINE \_ PROCESSO \_ \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**INFORMAZIONI SUI LIMITI ESTESI DI JOBOBJECT \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**INFORMAZIONI SUL LIMITE \_ DI SICUREZZA \_ DI JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>User-Mode di pianificazione

Con UMS vengono usate le strutture seguenti:

-   [**ATTRIBUTI DI CREAZIONE \_ THREAD UMS \_ \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**INFORMAZIONI DI AVVIO \_ DELL'UTILITÀ DI \_ PIANIFICAZIONE UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**INFORMAZIONI SUI \_ THREAD DI \_ SISTEMA UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
