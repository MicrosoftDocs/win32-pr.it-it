---
description: Consente di impostare i limiti nell'utilizzo del processo host delle risorse di sistema.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Classe __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231827"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="8a555-103">\_\_Classe ProviderHostQuotaConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a555-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="8a555-104">La classe di sistema **\_ \_ ProviderHostQuotaConfiguration** è una classe di configurazione per i processi del provider host.</span><span class="sxs-lookup"><span data-stu-id="8a555-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="8a555-105">Questa classe risiede nello spazio dei nomi radice e consente di impostare i limiti nell'utilizzo del processo host delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="8a555-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="8a555-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8a555-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8a555-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8a555-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a555-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a555-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="8a555-109">Members</span><span class="sxs-lookup"><span data-stu-id="8a555-109">Members</span></span>

<span data-ttu-id="8a555-110">La classe **\_ \_ ProviderHostQuotaConfiguration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8a555-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="8a555-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a555-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a555-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a555-112">Properties</span></span>

<span data-ttu-id="8a555-113">La classe **\_ \_ ProviderHostQuotaConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a555-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a555-114">**HandlesPerHost**</span><span class="sxs-lookup"><span data-stu-id="8a555-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a555-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a555-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a555-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8a555-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a555-117">Numero di handle di oggetti kernel che possono essere presenti in ogni host.</span><span class="sxs-lookup"><span data-stu-id="8a555-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="8a555-118">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="8a555-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a555-119">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8a555-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a555-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8a555-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a555-121">Quantità combinata di memoria privata in byte che può essere utilizzata da tutti gli host.</span><span class="sxs-lookup"><span data-stu-id="8a555-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="8a555-122">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8a555-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8a555-123">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="8a555-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a555-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8a555-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a555-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8a555-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a555-126">Quantità di memoria privata che può essere mantenuta da ogni host.</span><span class="sxs-lookup"><span data-stu-id="8a555-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="8a555-127">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8a555-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8a555-128">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="8a555-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a555-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a555-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a555-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8a555-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a555-131">Numero totale di processi host che possono essere eseguiti contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="8a555-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="8a555-132">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="8a555-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a555-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a555-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a555-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8a555-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a555-135">Numero di thread di proprietà di un host.</span><span class="sxs-lookup"><span data-stu-id="8a555-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a555-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a555-136">Remarks</span></span>

<span data-ttu-id="8a555-137">Le proprietà che rappresentano i limiti possono essere modificate, ma poiché la classe è un singleton, tutti gli host del provider condividono gli stessi limiti.</span><span class="sxs-lookup"><span data-stu-id="8a555-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="8a555-138">Quando si configurano i limiti per l'oggetto processo host, vengono utilizzati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a555-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="8a555-139">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="8a555-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="8a555-140">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="8a555-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="8a555-141">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="8a555-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="8a555-142">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="8a555-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="8a555-143">Il processo host esegue il polling dell'utilizzo e chiude il processo se la quota **HandlesPerHost** viene violata.</span><span class="sxs-lookup"><span data-stu-id="8a555-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="8a555-144">Le modifiche apportate a questi valori diventano effettive dopo il riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="8a555-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a555-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a555-145">Requirements</span></span>



| <span data-ttu-id="8a555-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a555-146">Requirement</span></span> | <span data-ttu-id="8a555-147">Valore</span><span class="sxs-lookup"><span data-stu-id="8a555-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8a555-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a555-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8a555-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a555-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8a555-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a555-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8a555-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a555-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8a555-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a555-152">Namespace</span></span><br/>                | <span data-ttu-id="8a555-153">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="8a555-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8a555-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a555-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a555-155">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="8a555-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="8a555-156">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8a555-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

