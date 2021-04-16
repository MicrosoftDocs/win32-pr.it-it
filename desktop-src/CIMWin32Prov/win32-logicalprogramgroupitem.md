---
description: Win32 \_ LogicalProgramGroupItem&\# 8194; La classe WMI rappresenta un elemento contenuto da un \_ LogicalProgramGroup Win32 che non è anche un'altra \_ istanza di LogicalProgramGroup Win32.
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524274"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="5c269-103">Win32 \_ LogicalProgramGroupItem (classe)</span><span class="sxs-lookup"><span data-stu-id="5c269-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="5c269-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroupItem Win32** rappresenta un elemento contenuto da un [**\_ LogicalProgramGroup Win32**](win32-logicalprogramgroup.md) che non è anche un'altra istanza di **\_ LogicalProgramGroup Win32** .</span><span class="sxs-lookup"><span data-stu-id="5c269-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="5c269-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c269-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5c269-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5c269-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c269-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c269-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="5c269-108">Members</span><span class="sxs-lookup"><span data-stu-id="5c269-108">Members</span></span>

<span data-ttu-id="5c269-109">La classe **Win32 \_ LogicalProgramGroupItem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c269-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="5c269-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c269-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c269-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c269-111">Properties</span></span>

<span data-ttu-id="5c269-112">La classe **Win32 \_ LogicalProgramGroupItem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c269-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c269-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5c269-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c269-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c269-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c269-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c269-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c269-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5c269-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5c269-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c269-117">A short textual description of the object.</span></span>

<span data-ttu-id="5c269-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c269-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c269-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5c269-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c269-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c269-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c269-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c269-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c269-122">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5c269-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5c269-123">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c269-123">A textual description of the object.</span></span>

<span data-ttu-id="5c269-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c269-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c269-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c269-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c269-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c269-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c269-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c269-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c269-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="5c269-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5c269-129">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="5c269-129">Indicates when the object was installed.</span></span> <span data-ttu-id="5c269-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="5c269-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5c269-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c269-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c269-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5c269-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c269-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c269-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c269-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c269-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c269-135">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| CWbemProviderGlue Class methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="5c269-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="5c269-136">Istanza all'interno di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="5c269-136">Instance within a computer system.</span></span> <span data-ttu-id="5c269-137">I gruppi di programmi vengono implementati come cartelle di file in Win32.</span><span class="sxs-lookup"><span data-stu-id="5c269-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="5c269-138">È necessario specificare i nomi dei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="5c269-138">Full path names should be provided.</span></span>

<span data-ttu-id="5c269-139">Esempio: "C: \\ utenti di \\ *un utente* \\ AppData \\ roaming \\ Microsoft \\ Windows \\ menu Start \\ programmi \\ Accessoris \\ notepad. lnk"</span><span class="sxs-lookup"><span data-stu-id="5c269-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="5c269-140">**Status**</span><span class="sxs-lookup"><span data-stu-id="5c269-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c269-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c269-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c269-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c269-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c269-143">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5c269-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5c269-144">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c269-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="5c269-145">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="5c269-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5c269-146">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="5c269-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5c269-147">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="5c269-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5c269-148">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5c269-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5c269-149">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5c269-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5c269-150">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5c269-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5c269-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c269-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5c269-152">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c269-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5c269-153">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5c269-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5c269-154">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="5c269-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5c269-155">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="5c269-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c269-156">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5c269-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5c269-157">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="5c269-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5c269-158">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="5c269-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5c269-159">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="5c269-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5c269-160">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="5c269-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5c269-161">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="5c269-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5c269-162">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="5c269-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5c269-163">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="5c269-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5c269-164">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="5c269-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5c269-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5c269-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5c269-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c269-166">Remarks</span></span>

<span data-ttu-id="5c269-167">La classe **Win32 \_ LogicalProgramGroupItem** è derivata da [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="5c269-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="5c269-168">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5c269-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="5c269-169">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="5c269-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="5c269-170">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="5c269-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c269-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c269-171">Requirements</span></span>



| <span data-ttu-id="5c269-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c269-172">Requirement</span></span> | <span data-ttu-id="5c269-173">Valore</span><span class="sxs-lookup"><span data-stu-id="5c269-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c269-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c269-174">Minimum supported client</span></span><br/> | <span data-ttu-id="5c269-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c269-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c269-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c269-176">Minimum supported server</span></span><br/> | <span data-ttu-id="5c269-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c269-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c269-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c269-178">Namespace</span></span><br/>                | <span data-ttu-id="5c269-179">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5c269-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c269-180">MOF</span><span class="sxs-lookup"><span data-stu-id="5c269-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c269-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c269-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c269-182">DLL</span><span class="sxs-lookup"><span data-stu-id="5c269-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c269-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c269-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c269-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c269-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c269-185">**\_ProgramGroupOrItem Win32**</span><span class="sxs-lookup"><span data-stu-id="5c269-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="5c269-186">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c269-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

