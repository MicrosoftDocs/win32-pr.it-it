---
title: Classe ReplicationProvider1
description: Classe base per l'istanza del provider.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Classe ReplicationProvider1 Active Directory
- Classe ReplicationProvider1 Active Directory, descritta
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048270"
---
# <a name="replicationprovider1-class"></a><span data-ttu-id="a6b12-105">Classe ReplicationProvider1</span><span class="sxs-lookup"><span data-stu-id="a6b12-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="a6b12-106">Classe base per l'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-106">The base class for the provider instance.</span></span>

<span data-ttu-id="a6b12-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a6b12-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b12-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6b12-108">Syntax</span></span>

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
  string   HostingModel;
};
```

## <a name="members"></a><span data-ttu-id="a6b12-109">Members</span><span class="sxs-lookup"><span data-stu-id="a6b12-109">Members</span></span>

<span data-ttu-id="a6b12-110">La classe **ReplicationProvider1** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6b12-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="a6b12-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6b12-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6b12-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6b12-112">Properties</span></span>

<span data-ttu-id="a6b12-113">La classe **ReplicationProvider1** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a6b12-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6b12-114">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="a6b12-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6b12-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-117">Identificatore di classe utilizzato da WMI per determinare se caricare o meno un provider a prestazioni elevate nel processo client o nel processo WMI.</span><span class="sxs-lookup"><span data-stu-id="a6b12-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="a6b12-118">Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="a6b12-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="a6b12-119">Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI.</span><span class="sxs-lookup"><span data-stu-id="a6b12-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="a6b12-120">WMI inoltre utilizza **ClientLoadableCLSID** per supportare le operazioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a6b12-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="a6b12-121">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="a6b12-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="a6b12-122">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="a6b12-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6b12-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-126">**GUID** che rappresenta l'identificatore di classe (**CLSID**) dell'oggetto com del provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="a6b12-127">Questo oggetto COM deve contenere un'implementazione dell'interfaccia [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="a6b12-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="a6b12-128">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-129">**Concorrenza**</span><span class="sxs-lookup"><span data-stu-id="a6b12-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6b12-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-132">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-132">Not used.</span></span>

<span data-ttu-id="a6b12-133">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-134">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="a6b12-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6b12-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-137">Identifica il computer in cui avviare il provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="a6b12-138">Se il provider viene eseguito nel computer locale, è **null**.</span><span class="sxs-lookup"><span data-stu-id="a6b12-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="a6b12-139">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-140">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="a6b12-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-141">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-143">Se **true**, questa istanza è abilitata e può essere utilizzata per completare le richieste del client.</span><span class="sxs-lookup"><span data-stu-id="a6b12-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="a6b12-144">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-145">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="a6b12-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6b12-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6b12-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-148">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span><span class="sxs-lookup"><span data-stu-id="a6b12-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-149">Contiene il modello di hosting del provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="a6b12-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-151">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6b12-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-153">Riservato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-153">Reserved.</span></span> <span data-ttu-id="a6b12-154">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="a6b12-154">The default value is zero (0).</span></span>

<span data-ttu-id="a6b12-155">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-156">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="a6b12-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-157">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6b12-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-159">Set di flag che forniscono informazioni sulla serializzazione.</span><span class="sxs-lookup"><span data-stu-id="a6b12-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="a6b12-160">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="a6b12-160">The default value is zero (0).</span></span>

<span data-ttu-id="a6b12-161">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a6b12-162"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="a6b12-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a6b12-163">Tutte le inizializzazioni del provider devono essere serializzate.</span><span class="sxs-lookup"><span data-stu-id="a6b12-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a6b12-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a6b12-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a6b12-165">Tutte le inizializzazioni del provider nello stesso spazio dei nomi devono essere serializzate.</span><span class="sxs-lookup"><span data-stu-id="a6b12-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="a6b12-166"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="a6b12-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="a6b12-167">Non è necessaria alcuna serializzazione dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="a6b12-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a6b12-168">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="a6b12-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-169">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6b12-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-171">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-171">Not used.</span></span>

<span data-ttu-id="a6b12-172">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-173">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="a6b12-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-174">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-176">**Windows Server 2003:** Questa proprietà è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a6b12-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="a6b12-177">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a6b12-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6b12-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-181">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a6b12-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-182">Nome provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-182">The provider name.</span></span>

<span data-ttu-id="a6b12-183">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-184">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="a6b12-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-185">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6b12-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-186">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-187">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-187">Not used.</span></span>

<span data-ttu-id="a6b12-188">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-189">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="a6b12-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-190">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-191">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-192">Se **true**, il provider viene inizializzato per ogni impostazione locale quando un utente si connette allo stesso spazio dei nomi più di una volta utilizzando impostazioni locali diverse.</span><span class="sxs-lookup"><span data-stu-id="a6b12-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="a6b12-193">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="a6b12-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="a6b12-194">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-195">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="a6b12-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-198">Se **true**, il provider viene inizializzato una volta per ogni utente di NT LAN Manager (NTLM) che effettua richieste al provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="a6b12-199">Se **false** (impostazione predefinita), il provider viene inizializzato una volta per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="a6b12-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="a6b12-200">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-201">**Puro**</span><span class="sxs-lookup"><span data-stu-id="a6b12-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-202">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-203">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-204">Se **true**, il provider accetta di preparare lo scaricamento chiamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in attesa quando WMI chiama il metodo **Release** della relativa interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="a6b12-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="a6b12-205">I provider che devono rimanere client di WMI dopo che non funzionano come provider devono impostare **pure** su **false**.</span><span class="sxs-lookup"><span data-stu-id="a6b12-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="a6b12-206">L'impostazione predefinita è **true**.</span><span class="sxs-lookup"><span data-stu-id="a6b12-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="a6b12-207">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="a6b12-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="a6b12-208">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a6b12-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6b12-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-212">Descrittore di sicurezza (SD) nel linguaggio SDDL (Security Descriptor Definition Language) che determina il set di utenti che possono chiamare correttamente [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) per il provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="a6b12-213">Per ulteriori informazioni, vedere l'argomento [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nella sezione security del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a6b12-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="a6b12-214">Questo descrittore di sicurezza viene usato solo per i provider disaccoppiati e non influisce su altri provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="a6b12-215">Per ulteriori informazioni, vedere [incorporamento di un provider in un'applicazione](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span><span class="sxs-lookup"><span data-stu-id="a6b12-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="a6b12-216">WMI esegue controlli di accesso per i provider disaccoppiati che utilizzano le interfacce [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="a6b12-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="a6b12-217">Se il descrittore di sicurezza è **null**, solo le applicazioni o i servizi eseguiti con gli account LocalSystem, NetworkService e LocalService possono eseguire un provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="a6b12-218">La stringa seguente mostra un provider disaccoppiato che deve essere eseguito solo dagli amministratori predefiniti ". O:BAG: BAD: (A;; 0 X1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="a6b12-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="a6b12-219">Per ulteriori informazioni sull'impostazione della proprietà **securityDescriptor** , vedere [gestione della sicurezza WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).</span><span class="sxs-lookup"><span data-stu-id="a6b12-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="a6b12-220">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-221">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="a6b12-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-222">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-224">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-224">Not used.</span></span>

<span data-ttu-id="a6b12-225">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-226">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b12-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-227">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-228">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-229">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-229">Not used.</span></span>

<span data-ttu-id="a6b12-230">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-231">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="a6b12-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-232">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-233">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-234">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-234">Not used.</span></span>

<span data-ttu-id="a6b12-235">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-236">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b12-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-237">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-239">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-239">Not used.</span></span>

<span data-ttu-id="a6b12-240">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-241">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="a6b12-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-242">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-243">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-244">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-244">Not used.</span></span>

<span data-ttu-id="a6b12-245">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-246">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="a6b12-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-247">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6b12-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-248">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-249">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-249">Not used.</span></span>

<span data-ttu-id="a6b12-250">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-251">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="a6b12-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-252">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6b12-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-254">[Formato di data e ora](/windows/desktop/WmiSdk/date-and-time-format) che specifica per quanto tempo WMI consente al provider di rimanere inattivo prima che venga scaricato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="a6b12-255">In genere, i provider richiedono che WMI attenda non più di cinque minuti.</span><span class="sxs-lookup"><span data-stu-id="a6b12-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="a6b12-256">Per la versione corrente di WMI, il valore di questa proprietà viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a6b12-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="a6b12-257">WMI Scarica il provider in base al valore di timeout in una classe interna nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="a6b12-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="a6b12-258">È consigliabile che i provider impostino **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="a6b12-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="a6b12-259">Per ulteriori informazioni, vedere [scaricamento di un provider](/windows/desktop/WmiSdk/unloading-a-provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="a6b12-260">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="a6b12-261">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a6b12-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b12-262">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6b12-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6b12-263">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6b12-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a6b12-264">Versione del provider.</span><span class="sxs-lookup"><span data-stu-id="a6b12-264">Version of the provider.</span></span> <span data-ttu-id="a6b12-265">Le versioni supportate sono 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="a6b12-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="a6b12-266">La versione 2 rafforza i controlli di validità per tutte le registrazioni delle proprietà associate, in particolare la proprietà [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .</span><span class="sxs-lookup"><span data-stu-id="a6b12-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="a6b12-267">Questa proprietà viene ereditata da [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="a6b12-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6b12-268">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6b12-268">Remarks</span></span>

<span data-ttu-id="a6b12-269">Un'istanza di questa classe rappresenta il provider WMI per Dominio di Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="a6b12-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="a6b12-270">I valori predefiniti sono</span><span class="sxs-lookup"><span data-stu-id="a6b12-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="a6b12-271">Nome = "ReplProv1"</span><span class="sxs-lookup"><span data-stu-id="a6b12-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="a6b12-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span><span class="sxs-lookup"><span data-stu-id="a6b12-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="a6b12-273">HostingModel = "NetworkServiceHost"</span><span class="sxs-lookup"><span data-stu-id="a6b12-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="a6b12-274">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6b12-274">Requirements</span></span>



| <span data-ttu-id="a6b12-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6b12-275">Requirement</span></span> | <span data-ttu-id="a6b12-276">Valore</span><span class="sxs-lookup"><span data-stu-id="a6b12-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b12-277">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6b12-277">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b12-278">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6b12-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a6b12-279">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6b12-279">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b12-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6b12-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6b12-281">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6b12-281">Namespace</span></span><br/>                | <span data-ttu-id="a6b12-282">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="a6b12-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="a6b12-283">MOF</span><span class="sxs-lookup"><span data-stu-id="a6b12-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6b12-284"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6b12-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6b12-285">DLL</span><span class="sxs-lookup"><span data-stu-id="a6b12-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6b12-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6b12-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b12-287">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6b12-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b12-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="a6b12-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

