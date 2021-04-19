---
title: Classe Win32_TSPermissionsSetting
description: Include un metodo per aggiungere nuovi account al terminale e un metodo per ripristinare le autorizzazioni predefinite per un terminale.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSPermissionsSetting Servizi Desktop remoto
- Classe Win32_TSPermissionsSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302424"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="26282-105">Win32 \_ TSPermissionsSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="26282-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="26282-106">La classe WMI **Win32 \_ TSPermissionsSetting** include un metodo per aggiungere nuovi account al terminale e un metodo per ripristinare le autorizzazioni predefinite per un terminale.</span><span class="sxs-lookup"><span data-stu-id="26282-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="26282-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="26282-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="26282-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="26282-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="26282-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26282-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="26282-110">Members</span><span class="sxs-lookup"><span data-stu-id="26282-110">Members</span></span>

<span data-ttu-id="26282-111">La classe **Win32 \_ TSPermissionsSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="26282-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="26282-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="26282-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="26282-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26282-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="26282-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="26282-114">Methods</span></span>

<span data-ttu-id="26282-115">La classe **Win32 \_ TSPermissionsSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="26282-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="26282-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="26282-116">Method</span></span>                                                                | <span data-ttu-id="26282-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26282-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26282-118">**AddAccount**</span><span class="sxs-lookup"><span data-stu-id="26282-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="26282-119">Aggiunge un account al terminale con il set di autorizzazioni specificato nel valore del parametro *PermissionPreSet* .</span><span class="sxs-lookup"><span data-stu-id="26282-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="26282-120">**RestoreDefaults**</span><span class="sxs-lookup"><span data-stu-id="26282-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="26282-121">Ripristina i valori predefiniti del set di autorizzazioni per il terminale.</span><span class="sxs-lookup"><span data-stu-id="26282-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="26282-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26282-122">Properties</span></span>

<span data-ttu-id="26282-123">La classe **Win32 \_ TSPermissionsSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="26282-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26282-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="26282-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26282-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26282-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26282-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="26282-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="26282-128">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26282-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="26282-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26282-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26282-130">**DenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="26282-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26282-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26282-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26282-133">Specifica se l'amministratore locale dispone dell'autorizzazione per la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="26282-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="26282-134">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="26282-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26282-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26282-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26282-137">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26282-137">Description of the object.</span></span>

<span data-ttu-id="26282-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26282-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26282-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="26282-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26282-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26282-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26282-142">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="26282-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="26282-143">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26282-143">The date the object was installed.</span></span> <span data-ttu-id="26282-144">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="26282-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="26282-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26282-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26282-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="26282-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26282-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26282-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26282-149">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26282-149">The name of the object.</span></span>

<span data-ttu-id="26282-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26282-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26282-151">**PolicySourceDenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="26282-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26282-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26282-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26282-154">Indica se la proprietà **MinEncryptionLevel** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26282-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="26282-155">0</span><span class="sxs-lookup"><span data-stu-id="26282-155">0</span></span>
</dt> <dd>

<span data-ttu-id="26282-156">Server</span><span class="sxs-lookup"><span data-stu-id="26282-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="26282-157">1</span><span class="sxs-lookup"><span data-stu-id="26282-157">1</span></span>
</dt> <dd>

<span data-ttu-id="26282-158">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="26282-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26282-159">**Status**</span><span class="sxs-lookup"><span data-stu-id="26282-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26282-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26282-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26282-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="26282-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="26282-163">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26282-163">Current status of the object.</span></span> <span data-ttu-id="26282-164">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="26282-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="26282-165">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="26282-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="26282-166">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="26282-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="26282-167">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="26282-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="26282-168">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="26282-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="26282-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26282-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="26282-170">("OK")</span><span class="sxs-lookup"><span data-stu-id="26282-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-171">("Errore")</span><span class="sxs-lookup"><span data-stu-id="26282-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-172">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="26282-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-173">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="26282-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-174">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="26282-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-175">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="26282-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-176">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="26282-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26282-177">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="26282-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26282-178">**StringSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="26282-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26282-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26282-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26282-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26282-181">Descrittore di sicurezza associato al terminale nel formato di matrice di byte binario.</span><span class="sxs-lookup"><span data-stu-id="26282-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="26282-182">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="26282-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26282-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26282-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26282-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26282-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26282-185">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="26282-185">The name of the terminal.</span></span>

<span data-ttu-id="26282-186">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="26282-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26282-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="26282-187">Remarks</span></span>

<span data-ttu-id="26282-188">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="26282-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="26282-189">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="26282-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="26282-190">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="26282-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="26282-191">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="26282-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="26282-192">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="26282-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26282-193">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="26282-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="26282-194">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="26282-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26282-195">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="26282-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="26282-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26282-196">Requirements</span></span>



| <span data-ttu-id="26282-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="26282-197">Requirement</span></span> | <span data-ttu-id="26282-198">Valore</span><span class="sxs-lookup"><span data-stu-id="26282-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26282-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26282-199">Minimum supported client</span></span><br/> | <span data-ttu-id="26282-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26282-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26282-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26282-201">Minimum supported server</span></span><br/> | <span data-ttu-id="26282-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26282-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26282-203">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26282-203">Namespace</span></span><br/>                | <span data-ttu-id="26282-204">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="26282-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="26282-205">MOF</span><span class="sxs-lookup"><span data-stu-id="26282-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26282-206"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26282-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="26282-207">DLL</span><span class="sxs-lookup"><span data-stu-id="26282-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26282-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26282-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26282-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26282-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26282-210">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="26282-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

