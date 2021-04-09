---
description: Il \_ Registro di sistema Win32&\# 8194; La classe WMI rappresenta il registro di sistema in un computer che esegue Windows.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Classe Win32_Registry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965975"
---
# <a name="win32_registry-class"></a><span data-ttu-id="54007-103">\_Classe Registry Win32</span><span class="sxs-lookup"><span data-stu-id="54007-103">Win32\_Registry class</span></span>

<span data-ttu-id="54007-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ del registro** di sistema Win32 rappresenta il registro di sistema in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="54007-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="54007-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="54007-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="54007-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="54007-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54007-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54007-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="54007-108">Members</span><span class="sxs-lookup"><span data-stu-id="54007-108">Members</span></span>

<span data-ttu-id="54007-109">La classe del **\_ Registro di sistema Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54007-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="54007-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54007-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54007-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54007-111">Properties</span></span>

<span data-ttu-id="54007-112">La **classe \_ del registro di sistema Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="54007-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54007-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="54007-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54007-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54007-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="54007-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="54007-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54007-117">A short textual description of the object.</span></span>

<span data-ttu-id="54007-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54007-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54007-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="54007-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54007-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54007-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-122">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemRegistryQuotaInformation"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="54007-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="54007-123">Dimensioni fisiche correnti del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="54007-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="54007-124">Esempio: 10</span><span class="sxs-lookup"><span data-stu-id="54007-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="54007-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="54007-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54007-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54007-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-128">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="54007-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="54007-129">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54007-129">A textual description of the object.</span></span>

<span data-ttu-id="54007-130">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54007-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54007-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="54007-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-132">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="54007-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54007-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-134">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="54007-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="54007-135">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="54007-135">Indicates when the object was installed.</span></span> <span data-ttu-id="54007-136">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="54007-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="54007-137">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54007-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54007-138">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="54007-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54007-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54007-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-141">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="54007-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="54007-142">Dimensioni massime del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="54007-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="54007-143">Se il sistema ha esito positivo utilizzando la proprietà **ProposedSize** , **MaximumSize** deve contenere lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="54007-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="54007-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="54007-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54007-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54007-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-147">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="54007-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="54007-148">Nome del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="54007-148">Name of the Windows registry.</span></span> <span data-ttu-id="54007-149">La lunghezza massima è 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="54007-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="54007-150">**ProposedSize**</span><span class="sxs-lookup"><span data-stu-id="54007-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54007-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54007-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="54007-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54007-153">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="54007-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="54007-154">Dimensioni proposte del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="54007-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="54007-155">Si tratta dell'unica impostazione del registro di sistema che può essere modificata e la relativa proposta viene tentata al successivo avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="54007-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="54007-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="54007-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54007-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54007-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54007-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54007-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54007-159">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="54007-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="54007-160">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54007-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="54007-161">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="54007-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="54007-162">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="54007-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="54007-163">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="54007-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="54007-164">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="54007-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="54007-165">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="54007-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="54007-166">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="54007-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="54007-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54007-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="54007-168">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="54007-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="54007-169">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="54007-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="54007-170">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="54007-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="54007-171">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="54007-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54007-172">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="54007-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="54007-173">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="54007-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="54007-174">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="54007-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="54007-175">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="54007-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="54007-176">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="54007-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="54007-177">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="54007-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="54007-178">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="54007-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="54007-179">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="54007-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="54007-180">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="54007-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="54007-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="54007-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="54007-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="54007-182">Remarks</span></span>

<span data-ttu-id="54007-183">La **classe \_ del registro di sistema Win32** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="54007-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54007-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54007-184">Requirements</span></span>



| <span data-ttu-id="54007-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="54007-185">Requirement</span></span> | <span data-ttu-id="54007-186">Valore</span><span class="sxs-lookup"><span data-stu-id="54007-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54007-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54007-187">Minimum supported client</span></span><br/> | <span data-ttu-id="54007-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54007-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54007-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54007-189">Minimum supported server</span></span><br/> | <span data-ttu-id="54007-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54007-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54007-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54007-191">Namespace</span></span><br/>                | <span data-ttu-id="54007-192">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="54007-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54007-193">MOF</span><span class="sxs-lookup"><span data-stu-id="54007-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54007-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54007-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54007-195">DLL</span><span class="sxs-lookup"><span data-stu-id="54007-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54007-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54007-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54007-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54007-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54007-198">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="54007-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="54007-199">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="54007-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
