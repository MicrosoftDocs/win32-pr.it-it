---
title: Classe Win32_TSStartMenuApplication
description: Descrive le applicazioni presenti nel menu Start di un server di host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSStartMenuApplication Servizi Desktop remoto
- Classe Win32_TSStartMenuApplication Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743594"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="776d2-105">Win32 \_ TSStartMenuApplication (classe)</span><span class="sxs-lookup"><span data-stu-id="776d2-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="776d2-106">Descrive le applicazioni presenti nel menu Start di un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="776d2-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="776d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="776d2-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="776d2-108">Members</span><span class="sxs-lookup"><span data-stu-id="776d2-108">Members</span></span>

<span data-ttu-id="776d2-109">La classe **Win32 \_ TSStartMenuApplication** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="776d2-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="776d2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="776d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="776d2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="776d2-111">Properties</span></span>

<span data-ttu-id="776d2-112">La classe **Win32 \_ TSStartMenuApplication** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="776d2-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="776d2-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="776d2-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776d2-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="776d2-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="776d2-117">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="776d2-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="776d2-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="776d2-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="776d2-119">**CommandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="776d2-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776d2-122">Argomenti della riga di comando da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="776d2-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="776d2-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="776d2-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776d2-126">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="776d2-126">Description of the object.</span></span>

<span data-ttu-id="776d2-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="776d2-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="776d2-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="776d2-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="776d2-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776d2-131">Indice o ID dell'icona.</span><span class="sxs-lookup"><span data-stu-id="776d2-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="776d2-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="776d2-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776d2-135">Percorso dell'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="776d2-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="776d2-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="776d2-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-137">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="776d2-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776d2-139">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="776d2-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="776d2-140">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="776d2-140">The date the object was installed.</span></span> <span data-ttu-id="776d2-141">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="776d2-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="776d2-142">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="776d2-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="776d2-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="776d2-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776d2-146">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="776d2-146">The name of the object.</span></span>

<span data-ttu-id="776d2-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="776d2-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="776d2-148">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="776d2-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776d2-151">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="776d2-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="776d2-152">Percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="776d2-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="776d2-153">**Status**</span><span class="sxs-lookup"><span data-stu-id="776d2-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776d2-156">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="776d2-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="776d2-157">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="776d2-157">Current status of the object.</span></span> <span data-ttu-id="776d2-158">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="776d2-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="776d2-159">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="776d2-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="776d2-160">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="776d2-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="776d2-161">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="776d2-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="776d2-162">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="776d2-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="776d2-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="776d2-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="776d2-164">("OK")</span><span class="sxs-lookup"><span data-stu-id="776d2-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-165">("Errore")</span><span class="sxs-lookup"><span data-stu-id="776d2-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-166">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="776d2-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-167">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="776d2-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-168">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="776d2-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-169">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="776d2-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-170">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="776d2-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="776d2-171">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="776d2-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="776d2-172">**VPath**</span><span class="sxs-lookup"><span data-stu-id="776d2-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776d2-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="776d2-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776d2-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="776d2-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776d2-175">Percorso virtuale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="776d2-175">The virtual path of the application.</span></span> <span data-ttu-id="776d2-176">Sono incluse le variabili di ambiente di sistema, ad esempio% windir%.</span><span class="sxs-lookup"><span data-stu-id="776d2-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="776d2-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="776d2-177">Remarks</span></span>

<span data-ttu-id="776d2-178">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="776d2-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="776d2-179">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="776d2-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="776d2-180">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="776d2-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="776d2-181">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="776d2-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="776d2-182">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="776d2-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="776d2-183">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="776d2-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="776d2-184">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="776d2-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="776d2-185">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="776d2-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="776d2-186">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="776d2-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="776d2-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="776d2-187">Requirements</span></span>



| <span data-ttu-id="776d2-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="776d2-188">Requirement</span></span> | <span data-ttu-id="776d2-189">Valore</span><span class="sxs-lookup"><span data-stu-id="776d2-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="776d2-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="776d2-190">Minimum supported client</span></span><br/> | <span data-ttu-id="776d2-191">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="776d2-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="776d2-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="776d2-192">Minimum supported server</span></span><br/> | <span data-ttu-id="776d2-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="776d2-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="776d2-194">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="776d2-194">Namespace</span></span><br/>                | <span data-ttu-id="776d2-195">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="776d2-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="776d2-196">MOF</span><span class="sxs-lookup"><span data-stu-id="776d2-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="776d2-197"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="776d2-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="776d2-198">DLL</span><span class="sxs-lookup"><span data-stu-id="776d2-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="776d2-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="776d2-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

