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
# <a name="process-and-thread-structures"></a><span data-ttu-id="d6813-103">Strutture di processi e thread</span><span class="sxs-lookup"><span data-stu-id="d6813-103">Process and Thread Structures</span></span>

<span data-ttu-id="d6813-104">Questo argomento elenca le strutture usate con processi, thread, processori, oggetti processo e pianificazione in modalità utente (UMS).</span><span class="sxs-lookup"><span data-stu-id="d6813-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="d6813-105">Strutture di processi e thread</span><span class="sxs-lookup"><span data-stu-id="d6813-105">Process and Thread Structures</span></span>

<span data-ttu-id="d6813-106">Con i processi e i thread vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6813-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="d6813-107">**\_informazioni memoria \_ app**</span><span class="sxs-lookup"><span data-stu-id="d6813-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="d6813-108">**\_stato AR**</span><span class="sxs-lookup"><span data-stu-id="d6813-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="d6813-109">**\_descrittore cache**</span><span class="sxs-lookup"><span data-stu-id="d6813-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="d6813-110">**\_contatori io**</span><span class="sxs-lookup"><span data-stu-id="d6813-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="d6813-111">**\_preferenza orientamento**</span><span class="sxs-lookup"><span data-stu-id="d6813-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="d6813-112">**PEB**</span><span class="sxs-lookup"><span data-stu-id="d6813-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="d6813-113">**\_dati LDR \_ PEB**</span><span class="sxs-lookup"><span data-stu-id="d6813-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="d6813-114">**\_informazioni sul processo**</span><span class="sxs-lookup"><span data-stu-id="d6813-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="d6813-115">**\_informazioni sull' \_ esaurimento della memoria del processo \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="d6813-116">**criteri ASLR per la \_ mitigazione dei processi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="d6813-117">**\_ \_ criteri di firma binaria di mitigazione dei processi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="d6813-118">**\_criteri di protezione del flusso di controllo di mitigazione dei processi \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="d6813-119">**criteri DEP per la \_ mitigazione dei processi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="d6813-120">**\_ \_ criteri del codice dinamico per la mitigazione dei processi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="d6813-121">**\_ \_ criteri di \_ \_ disabilitazione del punto di estensione \_ mitigazione processo**</span><span class="sxs-lookup"><span data-stu-id="d6813-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="d6813-122">**\_ \_ \_ criterio disabilitazione del tipo di carattere di mitigazione processo \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="d6813-123">**\_criteri di caricamento dell'immagine di mitigazione dei processi \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="d6813-124">**\_criteri di controllo dell' \_ handle rigorosi \_ \_ per la prevenzione \_ dei processi**</span><span class="sxs-lookup"><span data-stu-id="d6813-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="d6813-125">**\_richiesta di sistema di mitigazione dei processi disabilitare i \_ \_ \_ \_ criteri**</span><span class="sxs-lookup"><span data-stu-id="d6813-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="d6813-126">**\_parametri del \_ processo \_ utente RTL**</span><span class="sxs-lookup"><span data-stu-id="d6813-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="d6813-127">**STARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="d6813-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="d6813-128">**STARTUPINFOEX**</span><span class="sxs-lookup"><span data-stu-id="d6813-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="d6813-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="d6813-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="d6813-130">Strutture del processore</span><span class="sxs-lookup"><span data-stu-id="d6813-130">Processor Structures</span></span>

<span data-ttu-id="d6813-131">Con i processori e i gruppi di processori vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6813-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="d6813-132">**\_relazione cache**</span><span class="sxs-lookup"><span data-stu-id="d6813-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="d6813-133">**\_affinità gruppo**</span><span class="sxs-lookup"><span data-stu-id="d6813-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="d6813-134">**\_relazione tra gruppi**</span><span class="sxs-lookup"><span data-stu-id="d6813-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="d6813-135">**\_relazione nodo \_ NUMA**</span><span class="sxs-lookup"><span data-stu-id="d6813-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="d6813-136">**\_informazioni gruppo \_ processore**</span><span class="sxs-lookup"><span data-stu-id="d6813-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="d6813-137">**\_numero processore**</span><span class="sxs-lookup"><span data-stu-id="d6813-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="d6813-138">**\_relazione processore**</span><span class="sxs-lookup"><span data-stu-id="d6813-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="d6813-139">**\_ \_ informazioni sui set di CPU di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="d6813-140">**\_ \_ informazioni sul processore logico di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="d6813-141">**\_ \_ informazioni sul processore logico di sistema, ad \_ \_ esempio**</span><span class="sxs-lookup"><span data-stu-id="d6813-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="d6813-142">Struttura coda Dispatcher</span><span class="sxs-lookup"><span data-stu-id="d6813-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="d6813-143">La struttura seguente viene usata per creare un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span><span class="sxs-lookup"><span data-stu-id="d6813-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="d6813-144">**DispatcherQueueOptions**</span><span class="sxs-lookup"><span data-stu-id="d6813-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="d6813-145">Strutture di oggetti processo</span><span class="sxs-lookup"><span data-stu-id="d6813-145">Job Object Structures</span></span>

<span data-ttu-id="d6813-146">Con gli oggetti processo vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6813-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="d6813-147">**JOBOBJECT \_ associare \_ la \_ porta di completamento**</span><span class="sxs-lookup"><span data-stu-id="d6813-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="d6813-148">**\_informazioni di \_ contabilità di base di JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="d6813-149">**informazioni su JOBOBJECT \_ Basic \_ e \_ io \_ Accounting \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="d6813-150">**\_ \_ informazioni sul limite di JOBOBJECT Basic \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="d6813-151">**\_ \_ \_ elenco ID processo Basic \_ JOBOBJECT**</span><span class="sxs-lookup"><span data-stu-id="d6813-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="d6813-152">**\_ \_ restrizioni dell'interfaccia utente di base di JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="d6813-153">**JOBOBJECT \_ \_ \_ \_ \_ informazioni sull'ora di fine del processo**</span><span class="sxs-lookup"><span data-stu-id="d6813-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="d6813-154">**\_ \_ informazioni sul limite esteso JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="d6813-155">**\_ \_ informazioni sul limite di sicurezza JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="d6813-156">User-Mode strutture di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d6813-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="d6813-157">Con UMS vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6813-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="d6813-158">**\_attributi di \_ thread \_ creati da UMS**</span><span class="sxs-lookup"><span data-stu-id="d6813-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="d6813-159">**\_informazioni di avvio dell'utilità di pianificazione UMS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="d6813-160">**\_ \_ informazioni sul thread di sistema UMS \_**</span><span class="sxs-lookup"><span data-stu-id="d6813-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
