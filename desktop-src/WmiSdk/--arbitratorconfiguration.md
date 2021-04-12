---
description: Limita le risorse interne utilizzate dalle operazioni avviate dai client WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: Classe __ArbitratorConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232212"
---
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="1c2b2-103">\_\_Classe ArbitratorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c2b2-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="1c2b2-104">La classe **\_ \_ ArbitratorConfiguration** è una classe di configurazione che limita le risorse interne utilizzate dalle operazioni avviate dai client WMI.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="1c2b2-105">Si tratta di una classe singleton che risiede nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="1c2b2-106">La classe viene generata internamente, pertanto non è presente alcun file MOF.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="1c2b2-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1c2b2-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c2b2-109">Syntax</span></span>

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a><span data-ttu-id="1c2b2-110">Members</span><span class="sxs-lookup"><span data-stu-id="1c2b2-110">Members</span></span>

<span data-ttu-id="1c2b2-111">La classe **\_ \_ ArbitratorConfiguration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c2b2-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="1c2b2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c2b2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c2b2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c2b2-113">Properties</span></span>

<span data-ttu-id="1c2b2-114">La classe **\_ \_ ArbitratorConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c2b2-115">**OutstandingTasksPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-118">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-118">Unused.</span></span> <span data-ttu-id="1c2b2-119">Numero di attività avviate dall'utente in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-120">**OutstandingTasksTotal**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-121">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-123">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-123">Unused.</span></span> <span data-ttu-id="1c2b2-124">Numero totale di attività in attesa in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-125">**PermanentSubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-128">Numero di sottoscrizioni permanenti consentite per un determinato utente in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-129">**PermanentSubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-132">Numero totale di sottoscrizioni permanenti consentite per tutti gli utenti in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-133">**PollingInstructionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-136">Numero di query di eventi di polling consentite per un determinato utente in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-137">**PollingInstructionsTotal**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-140">Numero totale di istruzioni di polling consentite per tutti gli utenti in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-141">**PollingMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-144">La quantità di query di eventi di polling della memoria, rilasciata da un determinato utente, può essere utilizzata in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-145">**PollingMemoryTotal**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-148">La quantità totale di memoria che il polling delle query di eventi, per tutti gli utenti combinati, può essere usata in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-149">**QuotaRetryCount**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-152">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-152">Unused.</span></span> <span data-ttu-id="1c2b2-153">Numero di violazioni della quota consentite prima dell'annullamento di un'attività.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-154">**QuotaRetryWaitInterval**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-157">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-157">Unused.</span></span> <span data-ttu-id="1c2b2-158">Ritardo introdotto nell'esecuzione dell'attività in ogni violazione della quota.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-159">**TaskThreadsPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-162">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-162">Unused.</span></span> <span data-ttu-id="1c2b2-163">Numero massimo di thread attività associati a un utente specifico t una volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-164">**TaskThreadsTotal**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-167">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-167">Unused.</span></span> <span data-ttu-id="1c2b2-168">Numero massimo di thread attività.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-169">**TemporarySubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-172">Numero di sottoscrizioni temporanee consentite per un determinato utente in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-173">**TemporarySubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-174">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-176">Numero totale di sottoscrizioni temporanee consentite per tutti gli utenti in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-177">**TotalCacheDisk**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-178">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-180">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-180">Unused.</span></span> <span data-ttu-id="1c2b2-181">Totale della cache del disco associata a tutti gli utenti in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-182">**TotalCacheDiskPerTask**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-185">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-185">Unused.</span></span> <span data-ttu-id="1c2b2-186">Totale della cache del disco associata a una determinata attività in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-187">**TotalCacheDiskPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-188">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-190">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-190">Unused.</span></span> <span data-ttu-id="1c2b2-191">Totale della cache del disco associata a un determinato utente in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-192">**TotalCacheMemory**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-195">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-195">Unused.</span></span> <span data-ttu-id="1c2b2-196">Memoria totale della cache associata a tutti gli utenti in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-197">**TotalCacheMemoryPerTask**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-198">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-200">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-200">Unused.</span></span> <span data-ttu-id="1c2b2-201">Memoria totale della cache associata a un'attività specifica in un momento qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-202">**TotalCacheMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-205">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-205">Unused.</span></span> <span data-ttu-id="1c2b2-206">Memoria totale della cache associata a un determinato utente in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="1c2b2-207">**TotalUsers**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c2b2-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c2b2-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c2b2-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c2b2-210">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-210">Unused.</span></span> <span data-ttu-id="1c2b2-211">Numero massimo di utenti connessi.</span><span class="sxs-lookup"><span data-stu-id="1c2b2-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c2b2-212">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c2b2-212">Remarks</span></span>

<span data-ttu-id="1c2b2-213">**\_ \_ ArbitratorConfiguration** viene ereditato da [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="1c2b2-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2b2-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c2b2-214">Requirements</span></span>



| <span data-ttu-id="1c2b2-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c2b2-215">Requirement</span></span> | <span data-ttu-id="1c2b2-216">Valore</span><span class="sxs-lookup"><span data-stu-id="1c2b2-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1c2b2-217">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c2b2-217">Minimum supported client</span></span><br/> | <span data-ttu-id="1c2b2-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c2b2-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1c2b2-219">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c2b2-219">Minimum supported server</span></span><br/> | <span data-ttu-id="1c2b2-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c2b2-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1c2b2-221">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c2b2-221">Namespace</span></span><br/>                | <span data-ttu-id="1c2b2-222">Radice</span><span class="sxs-lookup"><span data-stu-id="1c2b2-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1c2b2-223">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c2b2-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2b2-224">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="1c2b2-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="1c2b2-225">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1c2b2-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

