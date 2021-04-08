---
description: Win32 \_ LogicalProgramGroup&\# 8194; Classe WMI rappresenta un gruppo di programmi in un computer che esegue Windows. Ad esempio, accessori o avvio.
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878145"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="36922-104">Win32 \_ LogicalProgramGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="36922-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="36922-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroup Win32** rappresenta un gruppo di programmi in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="36922-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="36922-106">Ad esempio, accessori o avvio.</span><span class="sxs-lookup"><span data-stu-id="36922-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="36922-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="36922-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="36922-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="36922-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36922-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36922-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="36922-110">Members</span><span class="sxs-lookup"><span data-stu-id="36922-110">Members</span></span>

<span data-ttu-id="36922-111">La classe **Win32 \_ LogicalProgramGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="36922-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="36922-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="36922-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36922-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="36922-113">Properties</span></span>

<span data-ttu-id="36922-114">La classe **Win32 \_ LogicalProgramGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="36922-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36922-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="36922-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36922-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36922-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="36922-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="36922-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36922-119">A short textual description of the object.</span></span>

<span data-ttu-id="36922-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36922-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36922-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="36922-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36922-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36922-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-124">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="36922-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="36922-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36922-125">A textual description of the object.</span></span>

<span data-ttu-id="36922-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36922-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36922-127">**GroupName**</span><span class="sxs-lookup"><span data-stu-id="36922-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36922-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36922-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-130">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| CWbemProviderGlue Class methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="36922-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="36922-131">Nome del gruppo di programmi di Windows.</span><span class="sxs-lookup"><span data-stu-id="36922-131">Name of the Windows program group.</span></span> <span data-ttu-id="36922-132">I gruppi di programmi vengono implementati come cartelle di file in Win32.</span><span class="sxs-lookup"><span data-stu-id="36922-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="36922-133">Esempio: "accessori di \\ sistema strumenti"</span><span class="sxs-lookup"><span data-stu-id="36922-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="36922-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="36922-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-135">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="36922-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36922-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-137">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="36922-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="36922-138">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="36922-138">Indicates when the object was installed.</span></span> <span data-ttu-id="36922-139">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="36922-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="36922-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36922-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36922-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="36922-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36922-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36922-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-144">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| CWbemProviderGlue Class methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="36922-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="36922-145">Nome assegnato dall'utente seguito dal nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="36922-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="36922-146">I gruppi di programmi vengono implementati come cartelle di file in Win32.</span><span class="sxs-lookup"><span data-stu-id="36922-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="36922-147">Esempio: "tutti gli utenti: accessori di \\ sistema degli accessori"</span><span class="sxs-lookup"><span data-stu-id="36922-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="36922-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="36922-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36922-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36922-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="36922-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="36922-152">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36922-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="36922-153">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="36922-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="36922-154">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="36922-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="36922-155">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="36922-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="36922-156">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="36922-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="36922-157">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="36922-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="36922-158">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="36922-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="36922-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36922-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="36922-160">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="36922-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="36922-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="36922-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="36922-162">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="36922-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="36922-163">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="36922-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36922-164">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="36922-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="36922-165">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="36922-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="36922-166">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="36922-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="36922-167">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="36922-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="36922-168">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="36922-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="36922-169">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="36922-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="36922-170">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="36922-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="36922-171">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="36922-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="36922-172">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="36922-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36922-173">**UserName**</span><span class="sxs-lookup"><span data-stu-id="36922-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36922-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36922-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36922-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36922-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36922-176">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| CWbemProviderGlue Class methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="36922-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="36922-177">Utenti che possono accedere al gruppo di programmi di Windows.</span><span class="sxs-lookup"><span data-stu-id="36922-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="36922-178">I gruppi di programmi vengono implementati come cartelle di file in Win32.</span><span class="sxs-lookup"><span data-stu-id="36922-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="36922-179">Esempio: "tutti gli utenti"</span><span class="sxs-lookup"><span data-stu-id="36922-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36922-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="36922-180">Remarks</span></span>

<span data-ttu-id="36922-181">La classe **Win32 \_ LogicalProgramGroup** è derivata da [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="36922-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="36922-182">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36922-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="36922-183">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="36922-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="36922-184">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="36922-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="36922-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36922-185">Requirements</span></span>



| <span data-ttu-id="36922-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="36922-186">Requirement</span></span> | <span data-ttu-id="36922-187">Valore</span><span class="sxs-lookup"><span data-stu-id="36922-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36922-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36922-188">Minimum supported client</span></span><br/> | <span data-ttu-id="36922-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36922-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36922-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36922-190">Minimum supported server</span></span><br/> | <span data-ttu-id="36922-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36922-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36922-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="36922-192">Namespace</span></span><br/>                | <span data-ttu-id="36922-193">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="36922-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36922-194">MOF</span><span class="sxs-lookup"><span data-stu-id="36922-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36922-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36922-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36922-196">DLL</span><span class="sxs-lookup"><span data-stu-id="36922-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36922-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36922-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36922-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36922-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36922-199">**\_ProgramGroupOrItem Win32**</span><span class="sxs-lookup"><span data-stu-id="36922-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="36922-200">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36922-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

