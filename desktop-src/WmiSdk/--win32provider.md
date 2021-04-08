---
description: Registra le informazioni sull'implementazione fisica di un provider in WMI. I provider che non impostano la proprietà HostingModel vengono caricati per impostazione predefinita per l'esecuzione in un processo di Wmiprvse.exe come NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Classe __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968374"
---
# <a name="__win32provider-class"></a><span data-ttu-id="f1906-104">\_\_Classe Win32Provider</span><span class="sxs-lookup"><span data-stu-id="f1906-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="f1906-105">La classe di sistema **\_ \_ Win32Provider** registra informazioni sull'implementazione fisica di un provider in WMI.</span><span class="sxs-lookup"><span data-stu-id="f1906-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="f1906-106">I provider che non impostano la proprietà **HostingModel** vengono caricati per impostazione predefinita per l'esecuzione in un processo di Wmiprvse.exe come **NetworkServiceHostOrSelfHost**.</span><span class="sxs-lookup"><span data-stu-id="f1906-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="f1906-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f1906-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f1906-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f1906-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1906-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1906-109">Syntax</span></span>

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
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
};
```

## <a name="members"></a><span data-ttu-id="f1906-110">Members</span><span class="sxs-lookup"><span data-stu-id="f1906-110">Members</span></span>

<span data-ttu-id="f1906-111">La classe **\_ \_ Win32Provider** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1906-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="f1906-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1906-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1906-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1906-113">Properties</span></span>

<span data-ttu-id="f1906-114">La classe **\_ \_ Win32Provider** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1906-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1906-115">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="f1906-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1906-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-118">Identificatore di classe utilizzato da WMI per determinare se caricare o meno un provider a prestazioni elevate nel processo client o nel processo WMI.</span><span class="sxs-lookup"><span data-stu-id="f1906-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="f1906-119">Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="f1906-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="f1906-120">Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI.</span><span class="sxs-lookup"><span data-stu-id="f1906-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="f1906-121">WMI inoltre utilizza **ClientLoadableCLSID** per supportare le operazioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f1906-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="f1906-122">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di High-Performance.](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="f1906-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="f1906-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="f1906-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1906-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-126">**GUID** che rappresenta l'identificatore di classe (**CLSID**) dell'oggetto com del provider.</span><span class="sxs-lookup"><span data-stu-id="f1906-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="f1906-127">Questo oggetto COM deve contenere un'implementazione dell'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="f1906-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-128">**Concorrenza**</span><span class="sxs-lookup"><span data-stu-id="f1906-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f1906-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-131">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-132">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="f1906-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1906-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-135">Identifica il computer in cui avviare il provider.</span><span class="sxs-lookup"><span data-stu-id="f1906-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="f1906-136">Se il provider viene eseguito nel computer locale, è **null**.</span><span class="sxs-lookup"><span data-stu-id="f1906-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="f1906-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-140">Se **true**, questa istanza è abilitata e può essere utilizzata per completare le richieste del client.</span><span class="sxs-lookup"><span data-stu-id="f1906-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-141">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="f1906-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1906-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-144">Questa proprietà è costituita dai valori delle proprietà **HostingGroup** e **HostingSpecification** dei [**\_ provider MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .</span><span class="sxs-lookup"><span data-stu-id="f1906-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="f1906-145">Il valore di questa proprietà specifica il modo in cui WMI carica il provider e l'account di sicurezza in cui viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1906-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="f1906-146">Per ulteriori informazioni sull'impostazione della proprietà **HostingModel** , vedere [hosting e sicurezza del provider](provider-hosting-and-security.md) e [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f1906-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1906-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="f1906-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-148">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f1906-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-150">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f1906-150">Reserved.</span></span> <span data-ttu-id="f1906-151">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="f1906-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="f1906-152">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="f1906-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f1906-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-155">Set di flag che forniscono informazioni sulla serializzazione.</span><span class="sxs-lookup"><span data-stu-id="f1906-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="f1906-156">Il valore predefinito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="f1906-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="f1906-157">0</span><span class="sxs-lookup"><span data-stu-id="f1906-157">0</span></span>
</dt> <dd>

<span data-ttu-id="f1906-158">Tutte le inizializzazioni del provider devono essere serializzate.</span><span class="sxs-lookup"><span data-stu-id="f1906-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-159">1</span><span class="sxs-lookup"><span data-stu-id="f1906-159">1</span></span>
</dt> <dd>

<span data-ttu-id="f1906-160">Tutte le inizializzazioni del provider nello stesso spazio dei nomi devono essere serializzate.</span><span class="sxs-lookup"><span data-stu-id="f1906-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-161">2</span><span class="sxs-lookup"><span data-stu-id="f1906-161">2</span></span>
</dt> <dd>

<span data-ttu-id="f1906-162">Non è necessaria alcuna serializzazione dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="f1906-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1906-163">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="f1906-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-164">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1906-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-166">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-167">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="f1906-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-170">TBD</span><span class="sxs-lookup"><span data-stu-id="f1906-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="f1906-171">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f1906-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1906-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f1906-174">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f1906-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f1906-175">Nome provider.</span><span class="sxs-lookup"><span data-stu-id="f1906-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-176">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="f1906-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-177">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1906-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-179">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-180">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="f1906-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-181">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-183">Se **true**, il provider viene inizializzato per ogni impostazione locale quando un utente si connette allo stesso spazio dei nomi più di una volta utilizzando impostazioni locali diverse.</span><span class="sxs-lookup"><span data-stu-id="f1906-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="f1906-184">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="f1906-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-185">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="f1906-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-186">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-188">Se **true**, il provider viene inizializzato una volta per ogni utente di NT LAN Manager (NTLM) che effettua richieste al provider.</span><span class="sxs-lookup"><span data-stu-id="f1906-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="f1906-189">Se **false** (impostazione predefinita), il provider viene inizializzato una volta per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f1906-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-190">**Puro**</span><span class="sxs-lookup"><span data-stu-id="f1906-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-191">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-193">Se **true**, il provider accetta di preparare lo scaricamento chiamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in attesa quando WMI chiama il metodo **Release** della relativa interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="f1906-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="f1906-194">I provider che devono rimanere client di WMI dopo che non funzionano come provider devono impostare **pure** su **false**.</span><span class="sxs-lookup"><span data-stu-id="f1906-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="f1906-195">L'impostazione predefinita è **true**.</span><span class="sxs-lookup"><span data-stu-id="f1906-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="f1906-196">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f1906-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f1906-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1906-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-200">Descrittore di sicurezza (SD) nel linguaggio SDDL (Security Descriptor Definition Language) che determina il set di utenti che possono chiamare correttamente [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) per il provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="f1906-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="f1906-201">Per ulteriori informazioni, vedere l'argomento [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) nella sezione security del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f1906-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="f1906-202">Questo descrittore di sicurezza viene usato solo per i provider disaccoppiati e non influisce su altri provider.</span><span class="sxs-lookup"><span data-stu-id="f1906-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="f1906-203">Per ulteriori informazioni, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="f1906-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="f1906-204">WMI esegue controlli di accesso per i provider disaccoppiati che utilizzano le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="f1906-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="f1906-205">Se il descrittore di sicurezza è **null**, solo le applicazioni o i servizi eseguiti con gli account LocalSystem, NetworkService e LocalService possono eseguire un provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="f1906-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="f1906-206">La stringa seguente mostra un provider disaccoppiato che deve essere eseguito solo dagli amministratori predefiniti ". O:BAG: BAD: (A;; 0 X1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="f1906-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="f1906-207">Per ulteriori informazioni sull'impostazione della proprietà **securityDescriptor** , vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="f1906-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1906-208">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="f1906-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-209">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-210">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-211">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-212">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="f1906-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-213">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-215">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-216">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="f1906-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-217">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-218">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-219">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-220">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="f1906-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-221">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-222">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-223">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-224">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="f1906-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-225">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-227">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-228">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="f1906-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-229">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f1906-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-230">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-231">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1906-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1906-232">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="f1906-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-233">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1906-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-234">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-235">[Formato di data e ora](date-and-time-format.md) che specifica per quanto tempo WMI consente al provider di rimanere inattivo prima che venga scaricato.</span><span class="sxs-lookup"><span data-stu-id="f1906-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="f1906-236">In genere, i provider richiedono che WMI attenda non più di cinque minuti.</span><span class="sxs-lookup"><span data-stu-id="f1906-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="f1906-237">Per la versione corrente di WMI, il valore di questa proprietà viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f1906-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="f1906-238">WMI Scarica il provider in base al valore di timeout in una classe interna nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="f1906-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="f1906-239">È consigliabile che i provider impostino **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="f1906-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="f1906-240">Per ulteriori informazioni, vedere [scaricamento di un provider](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f1906-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1906-241">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f1906-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1906-242">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1906-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1906-243">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1906-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f1906-244">Versione del provider.</span><span class="sxs-lookup"><span data-stu-id="f1906-244">Version of the provider.</span></span> <span data-ttu-id="f1906-245">Le versioni supportate sono 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="f1906-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="f1906-246">La versione 2 rafforza i controlli di validità per tutte le registrazioni delle proprietà associate, in particolare la proprietà [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="f1906-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1906-247">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1906-247">Remarks</span></span>

<span data-ttu-id="f1906-248">La classe **\_ \_ Win32Provider** è derivata dal [**\_ \_ provider**](--provider.md).</span><span class="sxs-lookup"><span data-stu-id="f1906-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="f1906-249">La maggior parte dei provider può accettare i valori predefiniti per la proprietà **InitializationReentrancy** .</span><span class="sxs-lookup"><span data-stu-id="f1906-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="f1906-250">Tuttavia, se un provider è in grado di supportare l'inizializzazione simultanea per utenti distinti, questa proprietà può essere impostata su 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="f1906-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="f1906-251">Se è necessaria l'inizializzazione serializzata, **InitializationReentrancy** rimane 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f1906-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="f1906-252">In entrambe le istanze, **PerUserInitialization** è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="f1906-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="f1906-253">Un provider pure o un provider che imposta la proprietà **pure** su **true** esiste solo per le richieste di servizio da applicazioni e WMI.</span><span class="sxs-lookup"><span data-stu-id="f1906-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="f1906-254">La maggior parte dei provider sono provider puri.</span><span class="sxs-lookup"><span data-stu-id="f1906-254">Most providers are pure providers.</span></span> <span data-ttu-id="f1906-255">Un provider non pure è l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f1906-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="f1906-256">I provider non puri passano al ruolo di client dopo aver completato le richieste di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="f1906-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="f1906-257">Un esempio di provider non pure è un provider di push che inizia a eseguire query ed effettua richieste di WMI dopo aver completato l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="f1906-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="f1906-258">Un provider di push non ha responsabilità ad eccezione dell'aggiornamento del repository CIM con i dati in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="f1906-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="f1906-259">Dopo l'aggiornamento del repository, un provider di push può rimanere in attesa di essere scaricato o passare al ruolo del client.</span><span class="sxs-lookup"><span data-stu-id="f1906-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="f1906-260">Il provider di push che attende di essere scaricato è un provider puro.</span><span class="sxs-lookup"><span data-stu-id="f1906-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="f1906-261">Il provider di push che partecipa alle attività del client non è puro.</span><span class="sxs-lookup"><span data-stu-id="f1906-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="f1906-262">WMI deve essere in grado di distinguere i provider puri da provider non puri, in modo che sia possibile determinare quando è sicuro arrestarsi.</span><span class="sxs-lookup"><span data-stu-id="f1906-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="f1906-263">WMI deve attendere il completamento di tutte le operazioni che coinvolgono provider non puri prima che sia possibile arrestarlo in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="f1906-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1906-264">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1906-264">Requirements</span></span>



| <span data-ttu-id="f1906-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1906-265">Requirement</span></span> | <span data-ttu-id="f1906-266">Valore</span><span class="sxs-lookup"><span data-stu-id="f1906-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f1906-267">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1906-267">Minimum supported client</span></span><br/> | <span data-ttu-id="f1906-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1906-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f1906-269">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1906-269">Minimum supported server</span></span><br/> | <span data-ttu-id="f1906-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1906-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f1906-271">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1906-271">Namespace</span></span><br/>                | <span data-ttu-id="f1906-272">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="f1906-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f1906-273">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1906-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1906-274">**\_\_Provider**</span><span class="sxs-lookup"><span data-stu-id="f1906-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="f1906-275">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f1906-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f1906-276">Registrazione di un provider</span><span class="sxs-lookup"><span data-stu-id="f1906-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

