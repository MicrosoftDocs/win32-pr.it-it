---
title: Provider di sistema
description: Abilitare gli eventi del provider di traccia di sistema con EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387814"
---
# <a name="system-providers"></a><span data-ttu-id="62848-103">Provider di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-103">System Providers</span></span>
 
<span data-ttu-id="62848-104">A partire da Windows 10 SDK build 20348, gli eventi del provider di traccia di sistema possono essere abilitati allo stesso modo di altri provider ETW, con [EnableTraceEx2.](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)</span><span class="sxs-lookup"><span data-stu-id="62848-104">Beginning in Windows 10 SDK build 20348, the System Trace Provider's events can be enabled in the same way that other ETW providers are, with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).</span></span>  <span data-ttu-id="62848-105">I diversi flag e [maschere di gruppo](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associati al provider di traccia di sistema sono stati mappati a nuovi provider di traccia, denominati provider di sistema, e parole chiave corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="62848-105">The different flags and [group masks](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associated with the System Trace Provider have been mapped to new trace providers, called System Providers, and matching keywords.</span></span>  
 
<span data-ttu-id="62848-106">Analogamente all'abilitazione diretta del provider di traccia di sistema, i provider di sistema possono essere abilitati solo da una sessione con il [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) impostato.</span><span class="sxs-lookup"><span data-stu-id="62848-106">Like enabling the System Trace Provider directly, the System Providers can only be enabled by a session with the [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) set.</span></span>

## <a name="system-provider-reference"></a><span data-ttu-id="62848-107">Informazioni di riferimento sul provider di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-107">System Provider reference</span></span>

* [<span data-ttu-id="62848-108">Provider ALPC di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-108">System ALPC Provider</span></span>](#system-alpc-provider)
* [<span data-ttu-id="62848-109">Provider di configurazione di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-109">System Config Provider</span></span>](#system-config-provider)
* [<span data-ttu-id="62848-110">Provider CPU di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-110">System CPU Provider</span></span>](#system-cpu-provider)
* [<span data-ttu-id="62848-111">Provider hypervisor di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-111">System Hypervisor Provider</span></span>](#system-hypervisor-provider)
* [<span data-ttu-id="62848-112">Provider di interrupt di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-112">System Interrupt Provider</span></span>](#system-interrupt-provider)
* [<span data-ttu-id="62848-113">Provider di I/O di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-113">System IO Provider</span></span>](#system-io-provider)
* [<span data-ttu-id="62848-114">Provider di filtri I/O di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-114">System IO Filter Provider</span></span>](#system-io-filter-provider)
* [<span data-ttu-id="62848-115">Provider di blocchi di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-115">System Lock Provider</span></span>](#system-lock-provider)
* [<span data-ttu-id="62848-116">Provider di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-116">System Memory Provider</span></span>](#system-memory-provider)
* [<span data-ttu-id="62848-117">Provider di oggetti di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-117">System Object Provider</span></span>](#system-object-provider)
* [<span data-ttu-id="62848-118">System Power Provider</span><span class="sxs-lookup"><span data-stu-id="62848-118">System Power Provider</span></span>](#system-power-provider)
* [<span data-ttu-id="62848-119">Provider di processi di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-119">System Process Provider</span></span>](#system-process-provider)
* [<span data-ttu-id="62848-120">Provider di profili di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-120">System Profile Provider</span></span>](#system-profile-provider)
* [<span data-ttu-id="62848-121">Provider del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-121">System Registry Provider</span></span>](#system-registry-provider)
* [<span data-ttu-id="62848-122">Provider dell'Utilità di pianificazione di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-122">System Scheduler Provider</span></span>](#system-scheduler-provider)
* [<span data-ttu-id="62848-123">Provider Syscall di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-123">System Syscall Provider</span></span>](#system-syscall-provider)
* [<span data-ttu-id="62848-124">Provider timer di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-124">System Timer Provider</span></span>](#system-timer-provider)
 
### <a name="system-alpc-provider"></a><span data-ttu-id="62848-125">Provider ALPC di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-125">System ALPC Provider</span></span>

<span data-ttu-id="62848-126">Fornisce eventi correlati al sistema ALPC.</span><span class="sxs-lookup"><span data-stu-id="62848-126">Provides events related to the ALPC system.</span></span>

<span data-ttu-id="62848-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span><span class="sxs-lookup"><span data-stu-id="62848-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span></span>

| <span data-ttu-id="62848-128">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-128">Keyword</span></span> | <span data-ttu-id="62848-129">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-129">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-130">SYSTEM_ALPC_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-130">SYSTEM_ALPC_KW_GENERAL</span></span> | <span data-ttu-id="62848-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span><span class="sxs-lookup"><span data-stu-id="62848-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span></span> |
 
### <a name="system-config-provider"></a><span data-ttu-id="62848-132">Provider di configurazione di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-132">System Config Provider</span></span> 

<span data-ttu-id="62848-133">Fornisce eventi di configurazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-133">Provides system configuration events.</span></span>

<span data-ttu-id="62848-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span><span class="sxs-lookup"><span data-stu-id="62848-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span></span>

| <span data-ttu-id="62848-135">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-135">Keyword</span></span> | <span data-ttu-id="62848-136">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-136">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-137">SYSTEM_CONFIG_KW_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="62848-137">SYSTEM_CONFIG_KW_SYSTEM</span></span> | <span data-ttu-id="62848-138">PERF_SYSCFG_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="62848-138">PERF_SYSCFG_SYSTEM</span></span> |
| <span data-ttu-id="62848-139">SYSTEM_CONFIG_KW_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="62848-139">SYSTEM_CONFIG_KW_GRAPHICS</span></span> | <span data-ttu-id="62848-140">PERF_SYSCFG_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="62848-140">PERF_SYSCFG_GRAPHICS</span></span> |
| <span data-ttu-id="62848-141">SYSTEM_CONFIG_KW_STORAGE</span><span class="sxs-lookup"><span data-stu-id="62848-141">SYSTEM_CONFIG_KW_STORAGE</span></span> | <span data-ttu-id="62848-142">PERF_SYSCFG_STORAGE</span><span class="sxs-lookup"><span data-stu-id="62848-142">PERF_SYSCFG_STORAGE</span></span> |
| <span data-ttu-id="62848-143">SYSTEM_CONFIG_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="62848-143">SYSTEM_CONFIG_KW_NETWORK</span></span> | <span data-ttu-id="62848-144">PERF_SYSCFG_NETWORK</span><span class="sxs-lookup"><span data-stu-id="62848-144">PERF_SYSCFG_NETWORK</span></span> |
| <span data-ttu-id="62848-145">SYSTEM_CONFIG_KW_SERVICES</span><span class="sxs-lookup"><span data-stu-id="62848-145">SYSTEM_CONFIG_KW_SERVICES</span></span> | <span data-ttu-id="62848-146">PERF_SYSCFG_SERVICES</span><span class="sxs-lookup"><span data-stu-id="62848-146">PERF_SYSCFG_SERVICES</span></span> |
| <span data-ttu-id="62848-147">SYSTEM_CONFIG_KW_PNP</span><span class="sxs-lookup"><span data-stu-id="62848-147">SYSTEM_CONFIG_KW_PNP</span></span> | <span data-ttu-id="62848-148">PERF_SYSCFG_PNP</span><span class="sxs-lookup"><span data-stu-id="62848-148">PERF_SYSCFG_PNP</span></span> |
| <span data-ttu-id="62848-149">SYSTEM_CONFIG_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="62848-149">SYSTEM_CONFIG_KW_OPTICAL</span></span> | <span data-ttu-id="62848-150">PERF_SYSCFG_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="62848-150">PERF_SYSCFG_OPTICAL</span></span> |
 
### <a name="system-cpu-provider"></a><span data-ttu-id="62848-151">Provider CPU di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-151">System CPU Provider</span></span> 

<span data-ttu-id="62848-152">Fornisce eventi correlati alla CPU.</span><span class="sxs-lookup"><span data-stu-id="62848-152">Provides events related to the CPU.</span></span>

<span data-ttu-id="62848-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span><span class="sxs-lookup"><span data-stu-id="62848-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span></span>

| <span data-ttu-id="62848-154">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-154">Keyword</span></span> | <span data-ttu-id="62848-155">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-155">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-156">SYSTEM_CPU_KW_CONFIG</span><span class="sxs-lookup"><span data-stu-id="62848-156">SYSTEM_CPU_KW_CONFIG</span></span> | <span data-ttu-id="62848-157">PERF_CPU_CONFIG</span><span class="sxs-lookup"><span data-stu-id="62848-157">PERF_CPU_CONFIG</span></span> |
| <span data-ttu-id="62848-158">SYSTEM_CPU_KW_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="62848-158">SYSTEM_CPU_KW_CACHE_FLUSH</span></span> | <span data-ttu-id="62848-159">PERF_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="62848-159">PERF_CACHE_FLUSH</span></span> |
| <span data-ttu-id="62848-160">SYSTEM_CPU_KW_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="62848-160">SYSTEM_CPU_KW_SPEC_CONTROL</span></span> | <span data-ttu-id="62848-161">PERF_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="62848-161">PERF_SPEC_CONTROL</span></span> |
 
### <a name="system-hypervisor-provider"></a><span data-ttu-id="62848-162">Provider hypervisor di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-162">System Hypervisor Provider</span></span> 

<span data-ttu-id="62848-163">Fornisce eventi relativi all'hypervisor.</span><span class="sxs-lookup"><span data-stu-id="62848-163">Provides events relating to the hypervisor.</span></span>

<span data-ttu-id="62848-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span><span class="sxs-lookup"><span data-stu-id="62848-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span></span>

| <span data-ttu-id="62848-165">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-165">Keyword</span></span> | <span data-ttu-id="62848-166">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-166">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-167">SYSTEM_HYPERVISOR_KW_PROFILE</span><span class="sxs-lookup"><span data-stu-id="62848-167">SYSTEM_HYPERVISOR_KW_PROFILE</span></span> | <span data-ttu-id="62848-168">PERF_HV_PROFILE</span><span class="sxs-lookup"><span data-stu-id="62848-168">PERF_HV_PROFILE</span></span> |
| <span data-ttu-id="62848-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="62848-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span></span> | <span data-ttu-id="62848-170">PERF_HV_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="62848-170">PERF_HV_CALLOUTS</span></span> |
| <span data-ttu-id="62848-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="62848-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span></span> | <span data-ttu-id="62848-172">PERF_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="62848-172">PERF_VTL_CHANGE</span></span> |
 
### <a name="system-interrupt-provider"></a><span data-ttu-id="62848-173">Provider di interrupt di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-173">System Interrupt Provider</span></span> 

<span data-ttu-id="62848-174">Fornisce eventi relativi a DPC e interrupt.</span><span class="sxs-lookup"><span data-stu-id="62848-174">Provides events relating to DPCs and interrupts.</span></span>

<span data-ttu-id="62848-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span><span class="sxs-lookup"><span data-stu-id="62848-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span></span>

| <span data-ttu-id="62848-176">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-176">Keyword</span></span> | <span data-ttu-id="62848-177">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-177">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-178">SYSTEM_INTERRUPT_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-178">SYSTEM_INTERRUPT_KW_GENERAL</span></span> | <span data-ttu-id="62848-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="62848-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span></span> |
| <span data-ttu-id="62848-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="62848-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span></span> | <span data-ttu-id="62848-181">PERF_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="62848-181">PERF_CLOCK_INTERRUPT</span></span> |
| <span data-ttu-id="62848-182">SYSTEM_INTERRUPT_KW_DPC</span><span class="sxs-lookup"><span data-stu-id="62848-182">SYSTEM_INTERRUPT_KW_DPC</span></span> | <span data-ttu-id="62848-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span><span class="sxs-lookup"><span data-stu-id="62848-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span></span> |
| <span data-ttu-id="62848-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="62848-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span></span> | <span data-ttu-id="62848-185">PERF_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="62848-185">PERF_DPC_QUEUE</span></span> |
| <span data-ttu-id="62848-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="62848-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span></span> | <span data-ttu-id="62848-187">PERF_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="62848-187">PERF_WDF_DPC</span></span> |
| <span data-ttu-id="62848-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="62848-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span></span> | <span data-ttu-id="62848-189">PERF_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="62848-189">PERF_WDF_INTERRUPT</span></span> |
| <span data-ttu-id="62848-190">SYSTEM_INTERRUPT_KW_IPI</span><span class="sxs-lookup"><span data-stu-id="62848-190">SYSTEM_INTERRUPT_KW_IPI</span></span> | <span data-ttu-id="62848-191">PERF_IPI</span><span class="sxs-lookup"><span data-stu-id="62848-191">PERF_IPI</span></span> |
 
 
### <a name="system-io-provider"></a><span data-ttu-id="62848-192">Provider di I/O di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-192">System IO Provider</span></span> 

<span data-ttu-id="62848-193">Fornisce eventi relativi a più tipi di I/O, tra cui disco, cache e rete.</span><span class="sxs-lookup"><span data-stu-id="62848-193">Provides events relating to multiple kinds of IO including disk, cache, and network.</span></span>

<span data-ttu-id="62848-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span><span class="sxs-lookup"><span data-stu-id="62848-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span></span>

| <span data-ttu-id="62848-195">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-195">Keyword</span></span> | <span data-ttu-id="62848-196">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-196">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-197">SYSTEM_IO_KW_DISK</span><span class="sxs-lookup"><span data-stu-id="62848-197">SYSTEM_IO_KW_DISK</span></span> | <span data-ttu-id="62848-198">EVENT_TRACE_FLAG_DISK_IO</span><span class="sxs-lookup"><span data-stu-id="62848-198">EVENT_TRACE_FLAG_DISK_IO</span></span> |
| <span data-ttu-id="62848-199">SYSTEM_IO_KW_DISK_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-199">SYSTEM_IO_KW_DISK_INIT</span></span> | <span data-ttu-id="62848-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span></span> |
| <span data-ttu-id="62848-201">SYSTEM_IO_KW_FILENAME</span><span class="sxs-lookup"><span data-stu-id="62848-201">SYSTEM_IO_KW_FILENAME</span></span> | <span data-ttu-id="62848-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="62848-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span></span> |
| <span data-ttu-id="62848-203">SYSTEM_IO_KW_SPLIT</span><span class="sxs-lookup"><span data-stu-id="62848-203">SYSTEM_IO_KW_SPLIT</span></span> | <span data-ttu-id="62848-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span><span class="sxs-lookup"><span data-stu-id="62848-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span></span> |
| <span data-ttu-id="62848-205">SYSTEM_IO_KW_FILE</span><span class="sxs-lookup"><span data-stu-id="62848-205">SYSTEM_IO_KW_FILE</span></span> | <span data-ttu-id="62848-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="62848-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span></span> |
| <span data-ttu-id="62848-207">SYSTEM_IO_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="62848-207">SYSTEM_IO_KW_OPTICAL</span></span> | <span data-ttu-id="62848-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span></span> |
| <span data-ttu-id="62848-209">SYSTEM_IO_KW_OPTICAL_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-209">SYSTEM_IO_KW_OPTICAL_INIT</span></span> | <span data-ttu-id="62848-210">PERF_OPTICAL_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-210">PERF_OPTICAL_IO_INIT</span></span> |
| <span data-ttu-id="62848-211">SYSTEM_IO_KW_DRIVERS</span><span class="sxs-lookup"><span data-stu-id="62848-211">SYSTEM_IO_KW_DRIVERS</span></span> | <span data-ttu-id="62848-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span><span class="sxs-lookup"><span data-stu-id="62848-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span></span> |
| <span data-ttu-id="62848-213">SYSTEM_IO_KW_CC</span><span class="sxs-lookup"><span data-stu-id="62848-213">SYSTEM_IO_KW_CC</span></span> | <span data-ttu-id="62848-214">PERF_CC</span><span class="sxs-lookup"><span data-stu-id="62848-214">PERF_CC</span></span> |
| <span data-ttu-id="62848-215">SYSTEM_IO_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="62848-215">SYSTEM_IO_KW_NETWORK</span></span> | <span data-ttu-id="62848-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span><span class="sxs-lookup"><span data-stu-id="62848-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span></span> |

<span data-ttu-id="62848-217">Nota: l'abilitazione SYSTEM_IO_KW_DRIVERS la parola chiave SYSTEM_IO_KW_FILENAME automaticamente.</span><span class="sxs-lookup"><span data-stu-id="62848-217">Note: Enabling the SYSTEM_IO_KW_DRIVERS keyword will automatically enable SYSTEM_IO_KW_FILENAME as well.</span></span>  <span data-ttu-id="62848-218">Il SYSTEM_IO_KW_FILENAME viene attivato automaticamente anche quando il provider di memoria di sistema è abilitato con la parola chiave SYSTEM_MEMORY_KW_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="62848-218">The SYSTEM_IO_KW_FILENAME is also automatically turned on when the System Memory Provider is enabled with the SYSTEM_MEMORY_KW_MEMORY keyword.</span></span>
 
### <a name="system-io-filter-provider"></a><span data-ttu-id="62848-219">Provider di filtri I/O di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-219">System IO Filter Provider</span></span> 

<span data-ttu-id="62848-220">Fornisce eventi correlati al filtro di I/O, inclusi tempi ed errori.</span><span class="sxs-lookup"><span data-stu-id="62848-220">Provides events related to IO filtering including timing and failures.</span></span>

<span data-ttu-id="62848-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span><span class="sxs-lookup"><span data-stu-id="62848-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span></span>

| <span data-ttu-id="62848-222">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-222">Keyword</span></span> | <span data-ttu-id="62848-223">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-223">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-224">SYSTEM_IOFILTER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-224">SYSTEM_IOFILTER_KW_GENERAL</span></span> | <span data-ttu-id="62848-225">PERF_FLT_IO</span><span class="sxs-lookup"><span data-stu-id="62848-225">PERF_FLT_IO</span></span> |
| <span data-ttu-id="62848-226">SYSTEM_IOFILTER_KW_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-226">SYSTEM_IOFILTER_KW_INIT</span></span> | <span data-ttu-id="62848-227">PERF_FLT_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="62848-227">PERF_FLT_IO_INIT</span></span> |
| <span data-ttu-id="62848-228">SYSTEM_IOFILTER_KW_FASTIO</span><span class="sxs-lookup"><span data-stu-id="62848-228">SYSTEM_IOFILTER_KW_FASTIO</span></span> | <span data-ttu-id="62848-229">PERF_FLT_FASTIO</span><span class="sxs-lookup"><span data-stu-id="62848-229">PERF_FLT_FASTIO</span></span> |
| <span data-ttu-id="62848-230">SYSTEM_IOFILTER_KW_FAILURE</span><span class="sxs-lookup"><span data-stu-id="62848-230">SYSTEM_IOFILTER_KW_FAILURE</span></span> | <span data-ttu-id="62848-231">PERF_FLT_IO_FAILURE</span><span class="sxs-lookup"><span data-stu-id="62848-231">PERF_FLT_IO_FAILURE</span></span> |
 
### <a name="system-lock-provider"></a><span data-ttu-id="62848-232">Provider di blocchi di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-232">System Lock Provider</span></span> 

<span data-ttu-id="62848-233">Fornisce eventi relativi ai meccanismi di blocco del kernel.</span><span class="sxs-lookup"><span data-stu-id="62848-233">Provides events relating to kernel locking mechanisms.</span></span>

<span data-ttu-id="62848-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span><span class="sxs-lookup"><span data-stu-id="62848-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span></span>

| <span data-ttu-id="62848-235">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-235">Keyword</span></span> | <span data-ttu-id="62848-236">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-236">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-237">SYSTEM_LOCK_KW_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="62848-237">SYSTEM_LOCK_KW_SPINLOCK</span></span> | <span data-ttu-id="62848-238">PERF_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="62848-238">PERF_SPINLOCK</span></span> |
| <span data-ttu-id="62848-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="62848-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span></span> | <span data-ttu-id="62848-240">PERF_SPINLOCK_CNTRS</span><span class="sxs-lookup"><span data-stu-id="62848-240">PERF_SPINLOCK_CNTRS</span></span> |
| <span data-ttu-id="62848-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="62848-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span></span> | <span data-ttu-id="62848-242">PERF_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="62848-242">PERF_SYNC_OBJECTS</span></span> |
 
### <a name="system-memory-provider"></a><span data-ttu-id="62848-243">Provider di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-243">System Memory Provider</span></span> 

<span data-ttu-id="62848-244">Fornisce eventi relativi al gestore della memoria.</span><span class="sxs-lookup"><span data-stu-id="62848-244">Provides events relating to the memory manager.</span></span>

<span data-ttu-id="62848-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span><span class="sxs-lookup"><span data-stu-id="62848-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span></span>

| <span data-ttu-id="62848-246">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-246">Keyword</span></span> | <span data-ttu-id="62848-247">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-247">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-248">SYSTEM_MEMORY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-248">SYSTEM_MEMORY_KW_GENERAL</span></span> | <span data-ttu-id="62848-249">PERF_MEMORY</span><span class="sxs-lookup"><span data-stu-id="62848-249">PERF_MEMORY</span></span> |
| <span data-ttu-id="62848-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="62848-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span></span> | <span data-ttu-id="62848-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="62848-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span></span> |
| <span data-ttu-id="62848-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span><span class="sxs-lookup"><span data-stu-id="62848-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span></span> | <span data-ttu-id="62848-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span><span class="sxs-lookup"><span data-stu-id="62848-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span></span> |
| <span data-ttu-id="62848-254">SYSTEM_MEMORY_KW_POOL</span><span class="sxs-lookup"><span data-stu-id="62848-254">SYSTEM_MEMORY_KW_POOL</span></span> | <span data-ttu-id="62848-255">PERF_POOL</span><span class="sxs-lookup"><span data-stu-id="62848-255">PERF_POOL</span></span> |
| <span data-ttu-id="62848-256">SYSTEM_MEMORY_KW_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="62848-256">SYSTEM_MEMORY_KW_MEMINFO</span></span> | <span data-ttu-id="62848-257">PERF_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="62848-257">PERF_MEMINFO</span></span> |
| <span data-ttu-id="62848-258">SYSTEM_MEMORY_KW_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="62848-258">SYSTEM_MEMORY_KW_PFSECTION</span></span> | <span data-ttu-id="62848-259">PERF_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="62848-259">PERF_PFSECTION</span></span> |
| <span data-ttu-id="62848-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="62848-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span></span> | <span data-ttu-id="62848-261">PERF_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="62848-261">PERF_MEMINFO_WS</span></span> |
| <span data-ttu-id="62848-262">SYSTEM_MEMORY_KW_HEAP</span><span class="sxs-lookup"><span data-stu-id="62848-262">SYSTEM_MEMORY_KW_HEAP</span></span> | <span data-ttu-id="62848-263">PERF_HEAP</span><span class="sxs-lookup"><span data-stu-id="62848-263">PERF_HEAP</span></span> |
| <span data-ttu-id="62848-264">SYSTEM_MEMORY_KW_WS</span><span class="sxs-lookup"><span data-stu-id="62848-264">SYSTEM_MEMORY_KW_WS</span></span> | <span data-ttu-id="62848-265">PERF_WS</span><span class="sxs-lookup"><span data-stu-id="62848-265">PERF_WS</span></span> |
| <span data-ttu-id="62848-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="62848-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span></span> | <span data-ttu-id="62848-267">PERF_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="62848-267">PERF_CONTMEM_GEN</span></span> |
| <span data-ttu-id="62848-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="62848-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span></span> | <span data-ttu-id="62848-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="62848-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span></span> |
| <span data-ttu-id="62848-270">SYSTEM_MEMORY_KW_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="62848-270">SYSTEM_MEMORY_KW_FOOTPRINT</span></span> | <span data-ttu-id="62848-271">PERF_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="62848-271">PERF_FOOTPRINT</span></span> |
| <span data-ttu-id="62848-272">SYSTEM_MEMORY_KW_SESSION</span><span class="sxs-lookup"><span data-stu-id="62848-272">SYSTEM_MEMORY_KW_SESSION</span></span> | <span data-ttu-id="62848-273">PERF_SESSION</span><span class="sxs-lookup"><span data-stu-id="62848-273">PERF_SESSION</span></span> |
| <span data-ttu-id="62848-274">SYSTEM_MEMORY_KW_REFSET</span><span class="sxs-lookup"><span data-stu-id="62848-274">SYSTEM_MEMORY_KW_REFSET</span></span> | <span data-ttu-id="62848-275">PERF_REFSET</span><span class="sxs-lookup"><span data-stu-id="62848-275">PERF_REFSET</span></span> |
| <span data-ttu-id="62848-276">SYSTEM_MEMORY_KW_VAMAP</span><span class="sxs-lookup"><span data-stu-id="62848-276">SYSTEM_MEMORY_KW_VAMAP</span></span> | <span data-ttu-id="62848-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span><span class="sxs-lookup"><span data-stu-id="62848-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span></span> |

<span data-ttu-id="62848-278">Note:</span><span class="sxs-lookup"><span data-stu-id="62848-278">Notes:</span></span> 
* <span data-ttu-id="62848-279">L'abilitazione SYSTEM_MEMORY_KW_MEMORY parola chiave abiliterà automaticamente SYSTEM_IO_KW_FILENAME nel provider di I/O di sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-279">Enabling the SYSTEM_MEMORY_KW_MEMORY keyword will automatically enable SYSTEM_IO_KW_FILENAME on the System IO Provider as well.</span></span>
* <span data-ttu-id="62848-280">Gli eventi abilitati dal SYSTEM_MEMORY_KW_POOL supportano un filtro tag pool, per scrivere in modo selettivo gli eventi solo per determinati tag del pool.</span><span class="sxs-lookup"><span data-stu-id="62848-280">The events enabled by the SYSTEM_MEMORY_KW_POOL support a Pool Tag Filter, to selectively write events only for certain pool tags.</span></span>  <span data-ttu-id="62848-281">Viene configurato come filtro [schematizzato nel](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) provider di memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-281">This is configured as a [Schematized Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) on the System Memory Provider.</span></span>  <span data-ttu-id="62848-282">Il filtro PoolTag viene costruito come segue:</span><span class="sxs-lookup"><span data-stu-id="62848-282">The PoolTag filter is constructed as follows:</span></span>

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* <span data-ttu-id="62848-283">Il [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) deve essere inizializzato con Id impostato su SYSTEM_MEMORY_POOL_FILTER_ID e il campo size impostato sulla dimensione di Header più la parte usata della matrice PoolTags.</span><span class="sxs-lookup"><span data-stu-id="62848-283">The [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) should be initialized with Id set to SYSTEM_MEMORY_POOL_FILTER_ID and the size field set to the size of Header plus the used portion of the PoolTags array.</span></span>  

* <span data-ttu-id="62848-284">Ogni tag del pool è una stringa di 4 caratteri archiviata come ULONG nel filtro.</span><span class="sxs-lookup"><span data-stu-id="62848-284">Each Pool Tag is a 4 character string that is stored as a ULONG in the filter.</span></span>  
 
 
### <a name="system-object-provider"></a><span data-ttu-id="62848-285">Provider di oggetti di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-285">System Object Provider</span></span> 

<span data-ttu-id="62848-286">Fornisce eventi relativi a Object Manager.</span><span class="sxs-lookup"><span data-stu-id="62848-286">Provides events relating to the Object Manager.</span></span>

<span data-ttu-id="62848-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span><span class="sxs-lookup"><span data-stu-id="62848-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span></span>

| <span data-ttu-id="62848-288">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-288">Keyword</span></span> | <span data-ttu-id="62848-289">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-289">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-290">SYSTEM_OBJECT_KW_HANDLE</span><span class="sxs-lookup"><span data-stu-id="62848-290">SYSTEM_OBJECT_KW_HANDLE</span></span> | <span data-ttu-id="62848-291">PERF_OB_HANDLE</span><span class="sxs-lookup"><span data-stu-id="62848-291">PERF_OB_HANDLE</span></span> |
| <span data-ttu-id="62848-292">SYSTEM_OBJECT_KW_OBJECT</span><span class="sxs-lookup"><span data-stu-id="62848-292">SYSTEM_OBJECT_KW_OBJECT</span></span> | <span data-ttu-id="62848-293">PERF_OB_OBJECT</span><span class="sxs-lookup"><span data-stu-id="62848-293">PERF_OB_OBJECT</span></span> |
 
### <a name="system-power-provider"></a><span data-ttu-id="62848-294">System Power Provider</span><span class="sxs-lookup"><span data-stu-id="62848-294">System Power Provider</span></span> 

<span data-ttu-id="62848-295">Fornisce eventi relativi allo stato di alimentazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-295">Provides events relating to the system's power state.</span></span>

<span data-ttu-id="62848-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span><span class="sxs-lookup"><span data-stu-id="62848-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span></span>

| <span data-ttu-id="62848-297">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-297">Keyword</span></span> | <span data-ttu-id="62848-298">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-298">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-299">SYSTEM_POWER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-299">SYSTEM_POWER_KW_GENERAL</span></span> | <span data-ttu-id="62848-300">PERF_POWER</span><span class="sxs-lookup"><span data-stu-id="62848-300">PERF_POWER</span></span> |
| <span data-ttu-id="62848-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="62848-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span></span> | <span data-ttu-id="62848-302">PERF_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="62848-302">PERF_HIBER_RUNDOWN</span></span> |
| <span data-ttu-id="62848-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="62848-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span></span> | <span data-ttu-id="62848-304">PERF_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="62848-304">PERF_PROCESSOR_IDLE</span></span> |
| <span data-ttu-id="62848-305">SYSTEM_POWER_KW_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="62848-305">SYSTEM_POWER_KW_IDLE_SELECTION</span></span> | <span data-ttu-id="62848-306">PERF_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="62848-306">PERF_IDLE_SELECTION</span></span> |
| <span data-ttu-id="62848-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="62848-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span></span> | <span data-ttu-id="62848-308">PERF_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="62848-308">PERF_PPM_EXIT_LATENCY</span></span> |
 
### <a name="system-process-provider"></a><span data-ttu-id="62848-309">Provider di processi di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-309">System Process Provider</span></span> 

<span data-ttu-id="62848-310">Fornisce eventi relativi al processo, incluse le informazioni sulla durata, gli eventi di caricamento delle immagini e gli eventi correlati ai thread.</span><span class="sxs-lookup"><span data-stu-id="62848-310">Provides events relating to the process, including lifetime information, image load events, and thread related events.</span></span>

<span data-ttu-id="62848-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span><span class="sxs-lookup"><span data-stu-id="62848-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span></span>

| <span data-ttu-id="62848-312">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-312">Keyword</span></span> | <span data-ttu-id="62848-313">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-313">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-314">SYSTEM_PROCESS_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-314">SYSTEM_PROCESS_KW_GENERAL</span></span> | <span data-ttu-id="62848-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span><span class="sxs-lookup"><span data-stu-id="62848-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span></span> |
| <span data-ttu-id="62848-316">SYSTEM_PROCESS_KW_INSWAP</span><span class="sxs-lookup"><span data-stu-id="62848-316">SYSTEM_PROCESS_KW_INSWAP</span></span> | <span data-ttu-id="62848-317">PERF_PROCESS_INSWAP</span><span class="sxs-lookup"><span data-stu-id="62848-317">PERF_PROCESS_INSWAP</span></span> |
| <span data-ttu-id="62848-318">SYSTEM_PROCESS_KW_FREEZE</span><span class="sxs-lookup"><span data-stu-id="62848-318">SYSTEM_PROCESS_KW_FREEZE</span></span> | <span data-ttu-id="62848-319">PERF_PROCESS_FREEZE</span><span class="sxs-lookup"><span data-stu-id="62848-319">PERF_PROCESS_FREEZE</span></span> |
| <span data-ttu-id="62848-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span><span class="sxs-lookup"><span data-stu-id="62848-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span></span> | <span data-ttu-id="62848-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="62848-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span></span> |
| <span data-ttu-id="62848-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="62848-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span></span> | <span data-ttu-id="62848-323">PERF_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="62848-323">PERF_WAKE_COUNTER</span></span> |
| <span data-ttu-id="62848-324">SYSTEM_PROCESS_KW_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="62848-324">SYSTEM_PROCESS_KW_WAKE_DROP</span></span> | <span data-ttu-id="62848-325">PERF_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="62848-325">PERF_WAKE_DROP</span></span> |
| <span data-ttu-id="62848-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="62848-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span></span> | <span data-ttu-id="62848-327">PERF_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="62848-327">PERF_WAKE_EVENT</span></span> |
| <span data-ttu-id="62848-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="62848-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span></span> | <span data-ttu-id="62848-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="62848-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span></span> |
| <span data-ttu-id="62848-330">SYSTEM_PROCESS_KW_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="62848-330">SYSTEM_PROCESS_KW_DBGPRINT</span></span> | <span data-ttu-id="62848-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="62848-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span></span> |
| <span data-ttu-id="62848-332">SYSTEM_PROCESS_KW_JOB</span><span class="sxs-lookup"><span data-stu-id="62848-332">SYSTEM_PROCESS_KW_JOB</span></span> | <span data-ttu-id="62848-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span><span class="sxs-lookup"><span data-stu-id="62848-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span></span> |
| <span data-ttu-id="62848-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="62848-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span></span> | <span data-ttu-id="62848-335">PERF_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="62848-335">PERF_WORKER_THREAD</span></span> |
| <span data-ttu-id="62848-336">SYSTEM_PROCESS_KW_THREAD</span><span class="sxs-lookup"><span data-stu-id="62848-336">SYSTEM_PROCESS_KW_THREAD</span></span> | <span data-ttu-id="62848-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span><span class="sxs-lookup"><span data-stu-id="62848-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span></span> |
| <span data-ttu-id="62848-338">SYSTEM_PROCESS_KW_LOADER</span><span class="sxs-lookup"><span data-stu-id="62848-338">SYSTEM_PROCESS_KW_LOADER</span></span> | <span data-ttu-id="62848-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span><span class="sxs-lookup"><span data-stu-id="62848-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span></span> |
 
### <a name="system-profile-provider"></a><span data-ttu-id="62848-340">Provider di profili di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-340">System Profile Provider</span></span> 

<span data-ttu-id="62848-341">Fornisce eventi di profilatura.</span><span class="sxs-lookup"><span data-stu-id="62848-341">Provides profiling events.</span></span>

<span data-ttu-id="62848-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span><span class="sxs-lookup"><span data-stu-id="62848-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span></span>

| <span data-ttu-id="62848-343">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-343">Keyword</span></span> | <span data-ttu-id="62848-344">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-344">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-345">SYSTEM_PROFILE_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-345">SYSTEM_PROFILE_KW_GENERAL</span></span> | <span data-ttu-id="62848-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span><span class="sxs-lookup"><span data-stu-id="62848-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span></span> |
| <span data-ttu-id="62848-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="62848-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span></span> | <span data-ttu-id="62848-348">PERF_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="62848-348">PERF_PMC_PROFILE</span></span> |
 
### <a name="system-registry-provider"></a><span data-ttu-id="62848-349">Provider del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-349">System Registry Provider</span></span> 

<span data-ttu-id="62848-350">Fornisce eventi relativi al Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-350">Provides events relating to the registry.</span></span>

<span data-ttu-id="62848-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span><span class="sxs-lookup"><span data-stu-id="62848-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span></span>

| <span data-ttu-id="62848-352">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-352">Keyword</span></span> | <span data-ttu-id="62848-353">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-353">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-354">SYSTEM_REGISTRY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-354">SYSTEM_REGISTRY_KW_GENERAL</span></span> | <span data-ttu-id="62848-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="62848-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span></span> |
| <span data-ttu-id="62848-356">SYSTEM_REGISTRY_KW_HIVE</span><span class="sxs-lookup"><span data-stu-id="62848-356">SYSTEM_REGISTRY_KW_HIVE</span></span> | <span data-ttu-id="62848-357">PERF_REG_HIVE</span><span class="sxs-lookup"><span data-stu-id="62848-357">PERF_REG_HIVE</span></span> |
| <span data-ttu-id="62848-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="62848-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span></span> | <span data-ttu-id="62848-359">PERF_REG_NOTIF</span><span class="sxs-lookup"><span data-stu-id="62848-359">PERF_REG_NOTIF</span></span> |
 
### <a name="system-scheduler-provider"></a><span data-ttu-id="62848-360">Provider dell'Utilità di pianificazione di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-360">System Scheduler Provider</span></span> 

<span data-ttu-id="62848-361">Fornisce eventi relativi all'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="62848-361">Provides events relating to the scheduler.</span></span>

<span data-ttu-id="62848-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span><span class="sxs-lookup"><span data-stu-id="62848-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span></span>

| <span data-ttu-id="62848-363">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-363">Keyword</span></span> | <span data-ttu-id="62848-364">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-364">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="62848-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span></span> | <span data-ttu-id="62848-366">PERF_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="62848-366">PERF_XSCHEDULER</span></span> |
| <span data-ttu-id="62848-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="62848-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span></span> | <span data-ttu-id="62848-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="62848-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span></span> |
| <span data-ttu-id="62848-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="62848-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span></span> | <span data-ttu-id="62848-370">PERF_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="62848-370">PERF_KERNEL_QUEUE</span></span> |
| <span data-ttu-id="62848-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="62848-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span></span> | <span data-ttu-id="62848-372">PERF_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="62848-372">PERF_SHOULD_YIELD</span></span> |
| <span data-ttu-id="62848-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="62848-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span></span> | <span data-ttu-id="62848-374">PERF_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="62848-374">PERF_ANTI_STARVATION</span></span> |
| <span data-ttu-id="62848-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="62848-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span></span> | <span data-ttu-id="62848-376">PERF_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="62848-376">PERF_LOAD_BALANCER</span></span> |
| <span data-ttu-id="62848-377">SYSTEM_SCHEDULER_KW_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="62848-377">SYSTEM_SCHEDULER_KW_AFFINITY</span></span> | <span data-ttu-id="62848-378">PERF_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="62848-378">PERF_AFFINITY</span></span> |
| <span data-ttu-id="62848-379">SYSTEM_SCHEDULER_KW_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="62848-379">SYSTEM_SCHEDULER_KW_PRIORITY</span></span> | <span data-ttu-id="62848-380">PERF_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="62848-380">PERF_PRIORITY</span></span> |
| <span data-ttu-id="62848-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="62848-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span></span> | <span data-ttu-id="62848-382">PERF_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="62848-382">PERF_IDEAL_PROCESSOR</span></span> |
| <span data-ttu-id="62848-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span><span class="sxs-lookup"><span data-stu-id="62848-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span></span> | <span data-ttu-id="62848-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span><span class="sxs-lookup"><span data-stu-id="62848-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span></span> |
 
### <a name="system-syscall-provider"></a><span data-ttu-id="62848-385">Provider Syscall di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-385">System Syscall Provider</span></span> 

<span data-ttu-id="62848-386">Fornisce eventi con informazioni sulle chiamate di sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-386">Provides events with information about system calls.</span></span>

<span data-ttu-id="62848-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span><span class="sxs-lookup"><span data-stu-id="62848-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span></span>

| <span data-ttu-id="62848-388">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-388">Keyword</span></span> | <span data-ttu-id="62848-389">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-389">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-390">SYSTEM_SYSCALL_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-390">SYSTEM_SYSCALL_KW_GENERAL</span></span> | <span data-ttu-id="62848-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span><span class="sxs-lookup"><span data-stu-id="62848-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span></span> |
 
### <a name="system-timer-provider"></a><span data-ttu-id="62848-392">Provider timer di sistema</span><span class="sxs-lookup"><span data-stu-id="62848-392">System Timer Provider</span></span> 

<span data-ttu-id="62848-393">Fornisce eventi relativi ai timer nel kernel.</span><span class="sxs-lookup"><span data-stu-id="62848-393">Provides events relating to timers in the kernel.</span></span>

<span data-ttu-id="62848-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span><span class="sxs-lookup"><span data-stu-id="62848-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span></span>

| <span data-ttu-id="62848-395">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="62848-395">Keyword</span></span> | <span data-ttu-id="62848-396">Flag e gruppi legacy corrispondenti</span><span class="sxs-lookup"><span data-stu-id="62848-396">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="62848-397">SYSTEM_TIMER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="62848-397">SYSTEM_TIMER_KW_GENERAL</span></span> | <span data-ttu-id="62848-398">PERF_TIMER</span><span class="sxs-lookup"><span data-stu-id="62848-398">PERF_TIMER</span></span> |
| <span data-ttu-id="62848-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="62848-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span></span> | <span data-ttu-id="62848-400">PERF_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="62848-400">PERF_CLOCK_TIMER</span></span> |
 
## <a name="remarks"></a><span data-ttu-id="62848-401">Commenti</span><span class="sxs-lookup"><span data-stu-id="62848-401">Remarks</span></span>

<span data-ttu-id="62848-402">Questo nuovo meccanismo di abilitazione si aggiunge ai metodi preesistnti per abilitare questi eventi.</span><span class="sxs-lookup"><span data-stu-id="62848-402">This new enablement mechanism is in addition to the pre-existing methods for enabling these events.</span></span>  <span data-ttu-id="62848-403">Qualsiasi codice usato in genere continuerà a eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="62848-403">Any code that used to work, will continue to do so.</span></span>
 
<span data-ttu-id="62848-404">Gli eventi generati dal provider di traccia di sistema non cambiano a causa di questa nuova funzionalità.</span><span class="sxs-lookup"><span data-stu-id="62848-404">The events generated by the System Trace Provider are not changing due to this new feature.</span></span>  <span data-ttu-id="62848-405">Ciò significa che gli eventi restituiti non vengono contrassegnati come generati dai singoli provider di sistema.</span><span class="sxs-lookup"><span data-stu-id="62848-405">This means that the outputted events are not marked as being emitted from the individual system providers.</span></span>
 
<span data-ttu-id="62848-406">Per altre informazioni sul GUID del provider e sulle definizioni delle parole chiave, [vedere evntrace.h.](/windows/win32/api/evntrace/)</span><span class="sxs-lookup"><span data-stu-id="62848-406">For more information on provider GUID and keyword definitions see [evntrace.h](/windows/win32/api/evntrace/).</span></span>

## <a name="see-also"></a><span data-ttu-id="62848-407">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="62848-407">See Also</span></span>

[<span data-ttu-id="62848-408">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="62848-408">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)

[<span data-ttu-id="62848-409">Intestazione evntrace.h</span><span class="sxs-lookup"><span data-stu-id="62848-409">evntrace.h header</span></span>](/windows/win32/api/evntrace/)