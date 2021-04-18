---
description: Questo argomento elenca le strutture usate con processi, thread, processori, oggetti processo e pianificazione in modalità utente (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Strutture di processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311971"
---
# <a name="process-and-thread-structures"></a>Strutture di processi e thread

Questo argomento elenca le strutture usate con processi, thread, processori, oggetti processo e pianificazione in modalità utente (UMS).

## <a name="process-and-thread-structures"></a>Strutture di processi e thread

Con i processi e i thread vengono utilizzate le strutture seguenti:

-   [**\_informazioni memoria \_ app**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**\_stato AR**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**\_descrittore cache**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**\_contatori io**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**\_preferenza orientamento**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**\_dati LDR \_ PEB**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**\_informazioni sul processo**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**\_informazioni sull' \_ esaurimento della memoria del processo \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**criteri ASLR per la \_ mitigazione dei processi \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**\_ \_ criteri di firma binaria di mitigazione dei processi \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**\_criteri di protezione del flusso di controllo di mitigazione dei processi \_ \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**criteri DEP per la \_ mitigazione dei processi \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**\_ \_ criteri del codice dinamico per la mitigazione dei processi \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**\_ \_ criteri di \_ \_ disabilitazione del punto di estensione \_ mitigazione processo**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**\_ \_ \_ criterio disabilitazione del tipo di carattere di mitigazione processo \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**\_criteri di caricamento dell'immagine di mitigazione dei processi \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**\_criteri di controllo dell' \_ handle rigorosi \_ \_ per la prevenzione \_ dei processi**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**\_richiesta di sistema di mitigazione dei processi disabilitare i \_ \_ \_ \_ criteri**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_parametri del \_ processo \_ utente RTL**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Strutture del processore

Con i processori e i gruppi di processori vengono utilizzate le strutture seguenti:

-   [**\_relazione cache**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**\_affinità gruppo**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**\_relazione tra gruppi**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**\_relazione nodo \_ NUMA**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**\_informazioni gruppo \_ processore**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**\_numero processore**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**\_relazione processore**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**\_ \_ informazioni sui set di CPU di sistema \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**\_ \_ informazioni sul processore logico di sistema \_**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**\_ \_ informazioni sul processore logico di sistema, ad \_ \_ esempio**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Struttura coda Dispatcher

La struttura seguente viene usata per creare un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Strutture di oggetti processo

Con gli oggetti processo vengono utilizzate le strutture seguenti:

-   [**JOBOBJECT \_ associare \_ la \_ porta di completamento**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**\_informazioni di \_ contabilità di base di JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**informazioni su JOBOBJECT \_ Basic \_ e \_ io \_ Accounting \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**\_ \_ informazioni sul limite di JOBOBJECT Basic \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_ \_ \_ elenco ID processo Basic \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**\_ \_ restrizioni dell'interfaccia utente di base di JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JOBOBJECT \_ \_ \_ \_ \_ informazioni sull'ora di fine del processo**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**\_ \_ informazioni sul limite esteso JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_ \_ informazioni sul limite di sicurezza JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>User-Mode strutture di pianificazione

Con UMS vengono utilizzate le strutture seguenti:

-   [**\_attributi di \_ thread \_ creati da UMS**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**\_informazioni di avvio dell'utilità di pianificazione UMS \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**\_ \_ informazioni sul thread di sistema UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
