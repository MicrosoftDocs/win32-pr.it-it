---
title: Classe Win32_TSApplicationFileExtensions
description: Estensioni di file gestite da un'applicazione in un server di host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSApplicationFileExtensions Servizi Desktop remoto
- Classe Win32_TSApplicationFileExtensions Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302431"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="790f7-105">Win32 \_ TSApplicationFileExtensions (classe)</span><span class="sxs-lookup"><span data-stu-id="790f7-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="790f7-106">Descrive le estensioni di file gestite da un'applicazione in un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="790f7-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="790f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="790f7-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="790f7-108">Members</span><span class="sxs-lookup"><span data-stu-id="790f7-108">Members</span></span>

<span data-ttu-id="790f7-109">La classe **Win32 \_ TSApplicationFileExtensions** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="790f7-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="790f7-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="790f7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="790f7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="790f7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="790f7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="790f7-112">Methods</span></span>

<span data-ttu-id="790f7-113">La classe **Win32 \_ TSApplicationFileExtensions** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="790f7-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="790f7-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="790f7-114">Method</span></span>                                                                         | <span data-ttu-id="790f7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="790f7-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="790f7-116">**FileAssociations**</span><span class="sxs-lookup"><span data-stu-id="790f7-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="790f7-117">Analizza il registro di sistema per ottenere le associazioni di file correnti per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="790f7-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="790f7-118">**FileExtension**</span><span class="sxs-lookup"><span data-stu-id="790f7-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="790f7-119">Fornisce un elenco delle estensioni dei nomi di file gestite da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="790f7-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="790f7-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="790f7-120">Properties</span></span>

<span data-ttu-id="790f7-121">La classe **Win32 \_ TSApplicationFileExtensions** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="790f7-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="790f7-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="790f7-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790f7-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="790f7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="790f7-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="790f7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="790f7-125">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="790f7-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="790f7-126">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="790f7-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="790f7-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="790f7-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="790f7-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="790f7-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790f7-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="790f7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="790f7-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="790f7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="790f7-131">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="790f7-131">Description of the object.</span></span>

<span data-ttu-id="790f7-132">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="790f7-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="790f7-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="790f7-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790f7-134">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="790f7-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="790f7-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="790f7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="790f7-136">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="790f7-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="790f7-137">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="790f7-137">The date the object was installed.</span></span> <span data-ttu-id="790f7-138">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="790f7-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="790f7-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="790f7-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="790f7-140">**Nome**</span><span class="sxs-lookup"><span data-stu-id="790f7-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790f7-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="790f7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="790f7-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="790f7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="790f7-143">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="790f7-143">The name of the object.</span></span>

<span data-ttu-id="790f7-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="790f7-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="790f7-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="790f7-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790f7-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="790f7-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="790f7-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="790f7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="790f7-148">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="790f7-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="790f7-149">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="790f7-149">Current status of the object.</span></span> <span data-ttu-id="790f7-150">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="790f7-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="790f7-151">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="790f7-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="790f7-152">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="790f7-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="790f7-153">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="790f7-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="790f7-154">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="790f7-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="790f7-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="790f7-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="790f7-156">("OK")</span><span class="sxs-lookup"><span data-stu-id="790f7-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-157">("Errore")</span><span class="sxs-lookup"><span data-stu-id="790f7-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-158">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="790f7-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-159">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="790f7-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-160">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="790f7-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-161">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="790f7-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-162">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="790f7-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="790f7-163">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="790f7-163">("Service")</span></span>


<span data-ttu-id="790f7-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="790f7-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="790f7-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="790f7-165">Remarks</span></span>

<span data-ttu-id="790f7-166">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="790f7-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="790f7-167">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="790f7-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="790f7-168">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="790f7-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="790f7-169">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="790f7-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="790f7-170">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="790f7-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="790f7-171">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="790f7-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="790f7-172">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="790f7-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="790f7-173">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="790f7-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="790f7-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="790f7-174">Requirements</span></span>



| <span data-ttu-id="790f7-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="790f7-175">Requirement</span></span> | <span data-ttu-id="790f7-176">Valore</span><span class="sxs-lookup"><span data-stu-id="790f7-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="790f7-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="790f7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="790f7-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="790f7-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="790f7-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="790f7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="790f7-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="790f7-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="790f7-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="790f7-181">Namespace</span></span><br/>                | <span data-ttu-id="790f7-182">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="790f7-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="790f7-183">MOF</span><span class="sxs-lookup"><span data-stu-id="790f7-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="790f7-184"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="790f7-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="790f7-185">DLL</span><span class="sxs-lookup"><span data-stu-id="790f7-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="790f7-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="790f7-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

