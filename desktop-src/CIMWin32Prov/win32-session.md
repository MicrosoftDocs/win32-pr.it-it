---
description: La \_ classe della sessione Win32 definisce le informazioni sullo stato relative all'interazione tra un utente e una risorsa, ad esempio un sistema di computer o una sessione terminal.
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Classe Win32_Session
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049110"
---
# <a name="win32_session-class"></a><span data-ttu-id="75c22-103">\_Classe di sessione Win32</span><span class="sxs-lookup"><span data-stu-id="75c22-103">Win32\_Session class</span></span>

<span data-ttu-id="75c22-104">La classe della **\_ sessione Win32** definisce le informazioni sullo stato relative all'interazione tra un utente e una risorsa, ad esempio un sistema di computer o una sessione terminal.</span><span class="sxs-lookup"><span data-stu-id="75c22-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="75c22-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="75c22-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="75c22-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="75c22-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c22-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75c22-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="75c22-108">Members</span><span class="sxs-lookup"><span data-stu-id="75c22-108">Members</span></span>

<span data-ttu-id="75c22-109">La classe della **\_ sessione Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="75c22-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="75c22-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="75c22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75c22-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="75c22-111">Properties</span></span>

<span data-ttu-id="75c22-112">La classe della **\_ sessione Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="75c22-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75c22-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="75c22-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75c22-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75c22-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75c22-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75c22-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75c22-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="75c22-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="75c22-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="75c22-117">A short textual description of the object.</span></span>

<span data-ttu-id="75c22-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75c22-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c22-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="75c22-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75c22-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75c22-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75c22-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75c22-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75c22-122">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="75c22-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="75c22-123">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="75c22-123">A textual description of the object.</span></span>

<span data-ttu-id="75c22-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75c22-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c22-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="75c22-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75c22-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75c22-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75c22-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75c22-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75c22-128">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="75c22-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="75c22-129">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="75c22-129">Indicates when the object was installed.</span></span> <span data-ttu-id="75c22-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="75c22-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="75c22-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75c22-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c22-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="75c22-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75c22-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75c22-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75c22-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75c22-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75c22-135">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="75c22-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="75c22-136">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="75c22-136">Label by which the object is known.</span></span> <span data-ttu-id="75c22-137">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="75c22-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="75c22-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75c22-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75c22-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="75c22-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75c22-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75c22-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75c22-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75c22-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75c22-142">Ora di inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="75c22-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="75c22-143">**Status**</span><span class="sxs-lookup"><span data-stu-id="75c22-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75c22-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="75c22-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75c22-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="75c22-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75c22-146">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="75c22-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="75c22-147">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="75c22-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="75c22-148">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="75c22-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="75c22-149">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="75c22-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="75c22-150">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="75c22-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="75c22-151">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="75c22-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="75c22-152">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="75c22-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="75c22-153">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="75c22-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="75c22-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75c22-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="75c22-155">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="75c22-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="75c22-156">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="75c22-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="75c22-157">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="75c22-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="75c22-158">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="75c22-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="75c22-159">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="75c22-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="75c22-160">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="75c22-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="75c22-161">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="75c22-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="75c22-162">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="75c22-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="75c22-163">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="75c22-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="75c22-164">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="75c22-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="75c22-165">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="75c22-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="75c22-166">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="75c22-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="75c22-167">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="75c22-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="75c22-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="75c22-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="75c22-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="75c22-169">Remarks</span></span>

<span data-ttu-id="75c22-170">La classe della **\_ sessione Win32** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="75c22-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75c22-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75c22-171">Requirements</span></span>



| <span data-ttu-id="75c22-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c22-172">Requirement</span></span> | <span data-ttu-id="75c22-173">Valore</span><span class="sxs-lookup"><span data-stu-id="75c22-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c22-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75c22-174">Minimum supported client</span></span><br/> | <span data-ttu-id="75c22-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75c22-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75c22-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75c22-176">Minimum supported server</span></span><br/> | <span data-ttu-id="75c22-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75c22-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75c22-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="75c22-178">Namespace</span></span><br/>                | <span data-ttu-id="75c22-179">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="75c22-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75c22-180">MOF</span><span class="sxs-lookup"><span data-stu-id="75c22-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75c22-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75c22-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75c22-182">DLL</span><span class="sxs-lookup"><span data-stu-id="75c22-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c22-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c22-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75c22-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75c22-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c22-185">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="75c22-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
