---
title: Classe Win32_TSExpandEnvironmentVariables
description: Espande le variabili di ambiente definite dal sistema. | Classe Win32_TSExpandEnvironmentVariables
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSExpandEnvironmentVariables Servizi Desktop remoto
- Classe Win32_TSExpandEnvironmentVariables Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886181"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="e4af2-106">Win32 \_ TSExpandEnvironmentVariables (classe)</span><span class="sxs-lookup"><span data-stu-id="e4af2-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="e4af2-107">Espande le variabili di ambiente definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4af2-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4af2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4af2-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="e4af2-109">Members</span><span class="sxs-lookup"><span data-stu-id="e4af2-109">Members</span></span>

<span data-ttu-id="e4af2-110">La classe **Win32 \_ TSExpandEnvironmentVariables** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e4af2-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="e4af2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e4af2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4af2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4af2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4af2-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e4af2-113">Methods</span></span>

<span data-ttu-id="e4af2-114">La classe **Win32 \_ TSExpandEnvironmentVariables** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e4af2-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="e4af2-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="e4af2-115">Method</span></span>                                                                                  | <span data-ttu-id="e4af2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4af2-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="e4af2-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="e4af2-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="e4af2-118">Espande le variabili di ambiente definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4af2-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e4af2-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4af2-119">Properties</span></span>

<span data-ttu-id="e4af2-120">La classe **Win32 \_ TSExpandEnvironmentVariables** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4af2-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4af2-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e4af2-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4af2-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e4af2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4af2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e4af2-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e4af2-125">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e4af2-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e4af2-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e4af2-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4af2-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e4af2-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4af2-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e4af2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4af2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4af2-130">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e4af2-130">Description of the object.</span></span>

<span data-ttu-id="e4af2-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e4af2-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4af2-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e4af2-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4af2-133">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e4af2-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4af2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-135">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e4af2-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e4af2-136">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e4af2-136">The date the object was installed.</span></span> <span data-ttu-id="e4af2-137">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="e4af2-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e4af2-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e4af2-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4af2-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e4af2-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4af2-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e4af2-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4af2-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4af2-142">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e4af2-142">The name of the object.</span></span>

<span data-ttu-id="e4af2-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e4af2-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4af2-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="e4af2-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4af2-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e4af2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4af2-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4af2-147">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e4af2-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e4af2-148">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e4af2-148">Current status of the object.</span></span> <span data-ttu-id="e4af2-149">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="e4af2-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e4af2-150">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="e4af2-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e4af2-151">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="e4af2-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e4af2-152">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="e4af2-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e4af2-153">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="e4af2-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e4af2-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e4af2-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e4af2-155">("OK")</span><span class="sxs-lookup"><span data-stu-id="e4af2-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-156">("Errore")</span><span class="sxs-lookup"><span data-stu-id="e4af2-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-157">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="e4af2-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-158">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e4af2-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-159">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="e4af2-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-160">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="e4af2-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-161">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="e4af2-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e4af2-162">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="e4af2-162">("Service")</span></span>


<span data-ttu-id="e4af2-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e4af2-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e4af2-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4af2-164">Remarks</span></span>

<span data-ttu-id="e4af2-165">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e4af2-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="e4af2-166">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="e4af2-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="e4af2-167">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="e4af2-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="e4af2-168">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e4af2-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="e4af2-169">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e4af2-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e4af2-170">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e4af2-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e4af2-171">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e4af2-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e4af2-172">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e4af2-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4af2-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4af2-173">Requirements</span></span>



| <span data-ttu-id="e4af2-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4af2-174">Requirement</span></span> | <span data-ttu-id="e4af2-175">Valore</span><span class="sxs-lookup"><span data-stu-id="e4af2-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af2-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4af2-176">Minimum supported client</span></span><br/> | <span data-ttu-id="e4af2-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4af2-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4af2-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4af2-178">Minimum supported server</span></span><br/> | <span data-ttu-id="e4af2-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4af2-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4af2-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4af2-180">Namespace</span></span><br/>                | <span data-ttu-id="e4af2-181">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e4af2-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e4af2-182">MOF</span><span class="sxs-lookup"><span data-stu-id="e4af2-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4af2-183"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4af2-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="e4af2-184">DLL</span><span class="sxs-lookup"><span data-stu-id="e4af2-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4af2-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4af2-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

