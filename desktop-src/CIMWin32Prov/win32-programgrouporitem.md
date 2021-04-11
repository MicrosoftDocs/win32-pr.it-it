---
description: La \_ classe WMI astratta Win32 ProgramGroupOrItem rappresenta un raggruppamento logico di programmi nel \\ menu Start Programs dell'utente. Contiene gruppi di programmi ed elementi del gruppo di programmi.
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupOrItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126087"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="7baf9-104">Win32 \_ ProgramGroupOrItem (classe)</span><span class="sxs-lookup"><span data-stu-id="7baf9-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="7baf9-105">La [classe WMI](../wmisdk/retrieving-a-class.md) astratta **Win32 \_ ProgramGroupOrItem** rappresenta un raggruppamento logico di programmi nel menu **Start \\ Programs** dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7baf9-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="7baf9-106">Contiene gruppi di programmi ed elementi del gruppo di programmi.</span><span class="sxs-lookup"><span data-stu-id="7baf9-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="7baf9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7baf9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7baf9-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7baf9-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7baf9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7baf9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="7baf9-110">Members</span><span class="sxs-lookup"><span data-stu-id="7baf9-110">Members</span></span>

<span data-ttu-id="7baf9-111">La classe **Win32 \_ ProgramGroupOrItem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7baf9-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="7baf9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7baf9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7baf9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7baf9-113">Properties</span></span>

<span data-ttu-id="7baf9-114">La classe **Win32 \_ ProgramGroupOrItem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7baf9-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7baf9-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7baf9-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7baf9-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7baf9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7baf9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-118">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7baf9-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7baf9-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7baf9-119">A short textual description of the object.</span></span>

<span data-ttu-id="7baf9-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7baf9-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7baf9-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7baf9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7baf9-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7baf9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7baf9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-124">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7baf9-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7baf9-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7baf9-125">A textual description of the object.</span></span>

<span data-ttu-id="7baf9-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7baf9-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7baf9-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7baf9-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7baf9-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7baf9-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7baf9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-130">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="7baf9-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7baf9-131">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="7baf9-131">Indicates when the object was installed.</span></span> <span data-ttu-id="7baf9-132">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="7baf9-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7baf9-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7baf9-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7baf9-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7baf9-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7baf9-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7baf9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7baf9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-137">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7baf9-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7baf9-138">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="7baf9-138">Label by which the object is known.</span></span> <span data-ttu-id="7baf9-139">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="7baf9-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7baf9-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7baf9-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7baf9-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="7baf9-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7baf9-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7baf9-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7baf9-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7baf9-144">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="7baf9-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7baf9-145">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7baf9-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="7baf9-146">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="7baf9-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7baf9-147">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="7baf9-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7baf9-148">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="7baf9-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7baf9-149">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="7baf9-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7baf9-150">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="7baf9-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7baf9-151">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="7baf9-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7baf9-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7baf9-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7baf9-153">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7baf9-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7baf9-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7baf9-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7baf9-155">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="7baf9-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7baf9-156">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="7baf9-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7baf9-157">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="7baf9-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7baf9-158">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="7baf9-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7baf9-159">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="7baf9-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7baf9-160">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="7baf9-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7baf9-161">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="7baf9-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7baf9-162">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="7baf9-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7baf9-163">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="7baf9-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7baf9-164">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="7baf9-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7baf9-165">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="7baf9-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7baf9-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7baf9-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7baf9-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="7baf9-167">Remarks</span></span>

<span data-ttu-id="7baf9-168">La classe **Win32 \_ ProgramGroupOrItem** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7baf9-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7baf9-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7baf9-169">Requirements</span></span>



| <span data-ttu-id="7baf9-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="7baf9-170">Requirement</span></span> | <span data-ttu-id="7baf9-171">Valore</span><span class="sxs-lookup"><span data-stu-id="7baf9-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7baf9-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7baf9-172">Minimum supported client</span></span><br/> | <span data-ttu-id="7baf9-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7baf9-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7baf9-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7baf9-174">Minimum supported server</span></span><br/> | <span data-ttu-id="7baf9-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7baf9-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7baf9-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7baf9-176">Namespace</span></span><br/>                | <span data-ttu-id="7baf9-177">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7baf9-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7baf9-178">MOF</span><span class="sxs-lookup"><span data-stu-id="7baf9-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7baf9-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7baf9-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7baf9-180">DLL</span><span class="sxs-lookup"><span data-stu-id="7baf9-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7baf9-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7baf9-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7baf9-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7baf9-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7baf9-183">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="7baf9-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="7baf9-184">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7baf9-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
