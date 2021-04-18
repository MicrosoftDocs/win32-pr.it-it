---
title: Classe Win32_TSVm
description: Rappresenta una macchina virtuale Desktop remoto.
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVm Servizi Desktop remoto
- Classe Win32_TSVm Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301052"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="03a30-105">Win32 \_ TSVm (classe)</span><span class="sxs-lookup"><span data-stu-id="03a30-105">Win32\_TSVm class</span></span>

<span data-ttu-id="03a30-106">Rappresenta una macchina virtuale Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="03a30-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="03a30-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="03a30-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a30-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03a30-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="03a30-109">Members</span><span class="sxs-lookup"><span data-stu-id="03a30-109">Members</span></span>

<span data-ttu-id="03a30-110">La classe **Win32 \_ TSVm** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03a30-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="03a30-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="03a30-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="03a30-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03a30-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="03a30-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="03a30-113">Methods</span></span>

<span data-ttu-id="03a30-114">La classe **Win32 \_ TSVm** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="03a30-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="03a30-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="03a30-115">Method</span></span>                                                                | <span data-ttu-id="03a30-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03a30-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="03a30-117">**DumpVmInfo**</span><span class="sxs-lookup"><span data-stu-id="03a30-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="03a30-118">Solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="03a30-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="03a30-119">**Esportazione**</span><span class="sxs-lookup"><span data-stu-id="03a30-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="03a30-120">Ottiene le informazioni di monitoraggio della sessione della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="03a30-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="03a30-121">**QueryOfflineInformation**</span><span class="sxs-lookup"><span data-stu-id="03a30-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="03a30-122">Esegue una query sulle proprietà solo quando è offline.</span><span class="sxs-lookup"><span data-stu-id="03a30-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="03a30-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03a30-123">Properties</span></span>

<span data-ttu-id="03a30-124">La classe **Win32 \_ TSVm** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03a30-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03a30-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="03a30-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a30-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a30-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a30-128">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="03a30-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03a30-129">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a30-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="03a30-130">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03a30-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03a30-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="03a30-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a30-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a30-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a30-134">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a30-134">Description of the object.</span></span>

<span data-ttu-id="03a30-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03a30-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03a30-136">**EnlightmentSettings**</span><span class="sxs-lookup"><span data-stu-id="03a30-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a30-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="03a30-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03a30-139">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="03a30-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="03a30-140">BLOB XML che contiene le impostazioni di illuminazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03a30-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="03a30-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03a30-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-142">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03a30-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a30-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a30-144">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="03a30-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="03a30-145">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a30-145">The date the object was installed.</span></span> <span data-ttu-id="03a30-146">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="03a30-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="03a30-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03a30-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03a30-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="03a30-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a30-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a30-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a30-151">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a30-151">The name of the object.</span></span>

<span data-ttu-id="03a30-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03a30-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03a30-153">**Status**</span><span class="sxs-lookup"><span data-stu-id="03a30-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a30-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a30-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a30-156">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="03a30-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="03a30-157">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a30-157">Current status of the object.</span></span> <span data-ttu-id="03a30-158">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="03a30-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="03a30-159">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="03a30-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="03a30-160">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="03a30-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="03a30-161">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="03a30-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="03a30-162">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="03a30-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="03a30-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03a30-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="03a30-164">("OK")</span><span class="sxs-lookup"><span data-stu-id="03a30-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-165">("Errore")</span><span class="sxs-lookup"><span data-stu-id="03a30-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-166">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="03a30-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-167">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="03a30-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-168">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="03a30-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-169">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="03a30-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-170">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="03a30-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="03a30-171">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="03a30-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03a30-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="03a30-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a30-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a30-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a30-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a30-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a30-175">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="03a30-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="03a30-176">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="03a30-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03a30-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03a30-177">Requirements</span></span>



| <span data-ttu-id="03a30-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a30-178">Requirement</span></span> | <span data-ttu-id="03a30-179">Valore</span><span class="sxs-lookup"><span data-stu-id="03a30-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a30-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a30-180">Minimum supported client</span></span><br/> | <span data-ttu-id="03a30-181">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="03a30-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="03a30-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a30-182">Minimum supported server</span></span><br/> | <span data-ttu-id="03a30-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03a30-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="03a30-184">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03a30-184">Namespace</span></span><br/>                | <span data-ttu-id="03a30-185">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="03a30-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="03a30-186">MOF</span><span class="sxs-lookup"><span data-stu-id="03a30-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03a30-187"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03a30-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="03a30-188">DLL</span><span class="sxs-lookup"><span data-stu-id="03a30-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a30-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a30-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

