---
title: Classe Win32_TSNetworkAdapterListSetting
description: Enumera l'elenco di schede di rete che possono essere configurate per un \_ terminale Win32, in base al protocollo Terminal e al metodo di trasporto specificati.
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSNetworkAdapterListSetting Servizi Desktop remoto
- Classe Win32_TSNetworkAdapterListSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301959"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="94a6e-105">Win32 \_ TSNetworkAdapterListSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="94a6e-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="94a6e-106">La classe WMI **\_ TSNetworkAdapterListSetting Win32** enumera l'elenco di schede di rete che possono essere configurate per un [**\_ terminale Win32**](win32-terminal.md), in base al protocollo Terminal e al metodo di trasporto specificati.</span><span class="sxs-lookup"><span data-stu-id="94a6e-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="94a6e-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="94a6e-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a6e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94a6e-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="94a6e-109">Members</span><span class="sxs-lookup"><span data-stu-id="94a6e-109">Members</span></span>

<span data-ttu-id="94a6e-110">La classe **Win32 \_ TSNetworkAdapterListSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94a6e-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="94a6e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94a6e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94a6e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94a6e-112">Properties</span></span>

<span data-ttu-id="94a6e-113">La classe **Win32 \_ TSNetworkAdapterListSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="94a6e-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94a6e-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="94a6e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="94a6e-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a6e-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="94a6e-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a6e-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a6e-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="94a6e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a6e-123">Description of the object.</span></span>

<span data-ttu-id="94a6e-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a6e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a6e-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="94a6e-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94a6e-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="94a6e-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a6e-129">The date the object was installed.</span></span> <span data-ttu-id="94a6e-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="94a6e-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="94a6e-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a6e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a6e-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="94a6e-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-135">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a6e-135">The name of the object.</span></span>

<span data-ttu-id="94a6e-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a6e-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94a6e-137">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="94a6e-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-140">GUID della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="94a6e-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="94a6e-141">**NetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="94a6e-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-144">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94a6e-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-145">Indirizzo IP della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="94a6e-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="94a6e-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="94a6e-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-149">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="94a6e-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-150">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94a6e-150">Current status of the object.</span></span> <span data-ttu-id="94a6e-151">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="94a6e-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="94a6e-152">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="94a6e-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="94a6e-153">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="94a6e-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="94a6e-154">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="94a6e-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="94a6e-155">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="94a6e-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="94a6e-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94a6e-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="94a6e-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="94a6e-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-158">("Errore")</span><span class="sxs-lookup"><span data-stu-id="94a6e-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-159">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="94a6e-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-160">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="94a6e-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-161">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="94a6e-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-162">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="94a6e-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-163">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="94a6e-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="94a6e-164">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="94a6e-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94a6e-165">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="94a6e-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a6e-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94a6e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94a6e-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94a6e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94a6e-168">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="94a6e-168">The name of the terminal.</span></span>

<span data-ttu-id="94a6e-169">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="94a6e-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94a6e-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="94a6e-170">Remarks</span></span>

<span data-ttu-id="94a6e-171">Per connettersi allo \\ \\ spazio dei nomi "root cimv2 TerminalServices", il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="94a6e-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="94a6e-172">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="94a6e-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="94a6e-173">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="94a6e-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="94a6e-174">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="94a6e-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="94a6e-175">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="94a6e-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="94a6e-176">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="94a6e-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="94a6e-177">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="94a6e-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="94a6e-178">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="94a6e-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="94a6e-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94a6e-179">Requirements</span></span>



| <span data-ttu-id="94a6e-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="94a6e-180">Requirement</span></span> | <span data-ttu-id="94a6e-181">Valore</span><span class="sxs-lookup"><span data-stu-id="94a6e-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94a6e-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94a6e-182">Minimum supported client</span></span><br/> | <span data-ttu-id="94a6e-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94a6e-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94a6e-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94a6e-184">Minimum supported server</span></span><br/> | <span data-ttu-id="94a6e-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94a6e-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94a6e-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94a6e-186">Namespace</span></span><br/>                | <span data-ttu-id="94a6e-187">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="94a6e-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="94a6e-188">MOF</span><span class="sxs-lookup"><span data-stu-id="94a6e-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94a6e-189"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94a6e-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="94a6e-190">DLL</span><span class="sxs-lookup"><span data-stu-id="94a6e-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94a6e-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94a6e-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a6e-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94a6e-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a6e-193">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="94a6e-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="94a6e-194">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="94a6e-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

