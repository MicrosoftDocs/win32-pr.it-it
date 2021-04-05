---
title: Classe Win32_TSPublishedApplicationList
description: Rappresenta l'elenco di programmi presenti nell'elenco programmi RemoteApp in un server Host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSPublishedApplicationList Servizi Desktop remoto
- Classe Win32_TSPublishedApplicationList Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048231"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="96c41-105">Win32 \_ TSPublishedApplicationList (classe)</span><span class="sxs-lookup"><span data-stu-id="96c41-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="96c41-106">Rappresenta l'elenco di programmi presenti nell'elenco programmi RemoteApp in un server Host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="96c41-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96c41-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="96c41-108">Members</span><span class="sxs-lookup"><span data-stu-id="96c41-108">Members</span></span>

<span data-ttu-id="96c41-109">La classe **Win32 \_ TSPublishedApplicationList** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="96c41-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="96c41-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96c41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96c41-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96c41-111">Properties</span></span>

<span data-ttu-id="96c41-112">La classe **Win32 \_ TSPublishedApplicationList** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="96c41-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96c41-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="96c41-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96c41-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96c41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c41-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="96c41-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="96c41-117">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96c41-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="96c41-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96c41-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c41-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="96c41-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96c41-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96c41-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c41-122">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96c41-122">Description of the object.</span></span>

<span data-ttu-id="96c41-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96c41-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c41-124">**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="96c41-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-125">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="96c41-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="96c41-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="96c41-127">Indica se il server Host sessione Desktop remoto limita i programmi che un utente può avviare sulla connessione iniziale ai programmi presenti nell'elenco programmi RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="96c41-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="96c41-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="96c41-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-129">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="96c41-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96c41-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c41-131">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="96c41-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="96c41-132">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96c41-132">The date the object was installed.</span></span> <span data-ttu-id="96c41-133">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="96c41-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="96c41-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96c41-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c41-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="96c41-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96c41-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96c41-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c41-138">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96c41-138">The name of the object.</span></span>

<span data-ttu-id="96c41-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96c41-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c41-140">**PolicySourceDisabled**</span><span class="sxs-lookup"><span data-stu-id="96c41-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96c41-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96c41-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c41-143">Indica se la proprietà **disabled** è configurata.</span><span class="sxs-lookup"><span data-stu-id="96c41-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="96c41-144">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="96c41-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="96c41-145">0</span><span class="sxs-lookup"><span data-stu-id="96c41-145">0</span></span>
</dt> <dd>

<span data-ttu-id="96c41-146">L'impostazione viene configurata nel server tramite Gestione RemoteApp o il provider WMI RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="96c41-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="96c41-147">1</span><span class="sxs-lookup"><span data-stu-id="96c41-147">1</span></span>
</dt> <dd>

<span data-ttu-id="96c41-148">L'impostazione viene configurata tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="96c41-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="96c41-149">2</span><span class="sxs-lookup"><span data-stu-id="96c41-149">2</span></span>
</dt> <dd>

<span data-ttu-id="96c41-150">L'impostazione non è configurata.</span><span class="sxs-lookup"><span data-stu-id="96c41-150">The setting is not configured.</span></span> <span data-ttu-id="96c41-151">Per la proprietà **disabled** viene utilizzato il valore predefinito **false** .</span><span class="sxs-lookup"><span data-stu-id="96c41-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="96c41-152">**Status**</span><span class="sxs-lookup"><span data-stu-id="96c41-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c41-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="96c41-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c41-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96c41-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c41-155">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="96c41-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="96c41-156">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96c41-156">Current status of the object.</span></span> <span data-ttu-id="96c41-157">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="96c41-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="96c41-158">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="96c41-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="96c41-159">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="96c41-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="96c41-160">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="96c41-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="96c41-161">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="96c41-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="96c41-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96c41-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="96c41-163">("OK")</span><span class="sxs-lookup"><span data-stu-id="96c41-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-164">("Errore")</span><span class="sxs-lookup"><span data-stu-id="96c41-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-165">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="96c41-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-166">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="96c41-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-167">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="96c41-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-168">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="96c41-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-169">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="96c41-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96c41-170">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="96c41-170">("Service")</span></span>


<span data-ttu-id="96c41-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="96c41-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="96c41-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="96c41-172">Remarks</span></span>

<span data-ttu-id="96c41-173">Per impostare le proprietà tramite questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="96c41-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="96c41-174">La proprietà **disabled** non impedisce agli utenti di avviare programmi non in elenco in remoto dopo la connessione al server Host sessione Desktop remoto tramite un programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="96c41-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="96c41-175">La proprietà **disabled** verrà impostata sul valore 2 solo se manca la seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="96c41-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="96c41-176">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WindowsNT** \\ **CurrentVersion** \\ **TerminalServer** \\ **TSAppAllowList** \\ **fDisabledAllowList**</span><span class="sxs-lookup"><span data-stu-id="96c41-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="96c41-177">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="96c41-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="96c41-178">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="96c41-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="96c41-179">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="96c41-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="96c41-180">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="96c41-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="96c41-181">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="96c41-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="96c41-182">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="96c41-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="96c41-183">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="96c41-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="96c41-184">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="96c41-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="96c41-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96c41-185">Requirements</span></span>



| <span data-ttu-id="96c41-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c41-186">Requirement</span></span> | <span data-ttu-id="96c41-187">Valore</span><span class="sxs-lookup"><span data-stu-id="96c41-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c41-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96c41-188">Minimum supported client</span></span><br/> | <span data-ttu-id="96c41-189">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="96c41-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="96c41-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96c41-190">Minimum supported server</span></span><br/> | <span data-ttu-id="96c41-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96c41-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96c41-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96c41-192">Namespace</span></span><br/>                | <span data-ttu-id="96c41-193">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="96c41-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="96c41-194">MOF</span><span class="sxs-lookup"><span data-stu-id="96c41-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96c41-195"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96c41-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="96c41-196">DLL</span><span class="sxs-lookup"><span data-stu-id="96c41-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96c41-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c41-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

