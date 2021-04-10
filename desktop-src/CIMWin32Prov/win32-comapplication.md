---
description: La \_ classe WMI abstract Comapplication Win32 rappresenta un'applicazione Component Object Model (com). In questo contesto, un'applicazione COM è un raggruppamento logico di classi COM.
ms.assetid: a70939e2-5812-4ade-aa75-819c8d4b9173
ms.tgt_platform: multiple
title: Classe Win32_COMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplication
- Win32_COMApplication.Caption
- Win32_COMApplication.Description
- Win32_COMApplication.InstallDate
- Win32_COMApplication.Name
- Win32_COMApplication.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 705f0f7b3c17ffca809de9a124748a74b5537f26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049246"
---
# <a name="win32_comapplication-class"></a><span data-ttu-id="239f9-104">\_Classe Comapplication Win32</span><span class="sxs-lookup"><span data-stu-id="239f9-104">Win32\_COMApplication class</span></span>

<span data-ttu-id="239f9-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Abstract **\_ comapplication Win32** rappresenta un'applicazione Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="239f9-105">The **Win32\_COMApplication** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a Component Object Model (COM) application.</span></span> <span data-ttu-id="239f9-106">In questo contesto, un'applicazione COM è un raggruppamento logico di classi COM.</span><span class="sxs-lookup"><span data-stu-id="239f9-106">In this context, a COM application is a logical grouping of COM classes.</span></span>

<span data-ttu-id="239f9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="239f9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="239f9-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="239f9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="239f9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="239f9-109">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED4F-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="239f9-110">Members</span><span class="sxs-lookup"><span data-stu-id="239f9-110">Members</span></span>

<span data-ttu-id="239f9-111">La **classe \_ comapplication Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="239f9-111">The **Win32\_COMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="239f9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="239f9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="239f9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="239f9-113">Properties</span></span>

<span data-ttu-id="239f9-114">La **classe \_ comapplication Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="239f9-114">The **Win32\_COMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="239f9-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="239f9-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="239f9-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="239f9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="239f9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="239f9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="239f9-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="239f9-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="239f9-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="239f9-119">A short textual description of the object.</span></span>

<span data-ttu-id="239f9-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="239f9-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="239f9-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="239f9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="239f9-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="239f9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="239f9-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="239f9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="239f9-124">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="239f9-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="239f9-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="239f9-125">A textual description of the object.</span></span>

<span data-ttu-id="239f9-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="239f9-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="239f9-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="239f9-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="239f9-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="239f9-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="239f9-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="239f9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="239f9-130">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="239f9-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="239f9-131">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="239f9-131">Indicates when the object was installed.</span></span> <span data-ttu-id="239f9-132">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="239f9-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="239f9-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="239f9-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="239f9-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="239f9-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="239f9-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="239f9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="239f9-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="239f9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="239f9-137">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="239f9-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="239f9-138">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="239f9-138">Label by which the object is known.</span></span> <span data-ttu-id="239f9-139">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="239f9-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="239f9-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="239f9-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="239f9-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="239f9-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="239f9-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="239f9-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="239f9-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="239f9-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="239f9-144">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="239f9-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="239f9-145">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="239f9-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="239f9-146">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="239f9-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="239f9-147">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="239f9-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="239f9-148">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="239f9-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="239f9-149">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="239f9-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="239f9-150">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="239f9-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="239f9-151">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="239f9-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="239f9-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="239f9-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="239f9-153">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="239f9-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="239f9-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="239f9-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="239f9-155">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="239f9-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="239f9-156">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="239f9-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="239f9-157">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="239f9-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="239f9-158">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="239f9-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="239f9-159">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="239f9-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="239f9-160">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="239f9-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="239f9-161">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="239f9-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="239f9-162">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="239f9-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="239f9-163">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="239f9-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="239f9-164">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="239f9-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="239f9-165">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="239f9-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="239f9-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="239f9-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="239f9-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="239f9-167">Remarks</span></span>

<span data-ttu-id="239f9-168">La classe della **\_ comApplicazione Win32** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="239f9-168">The **Win32\_COMApplication** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="239f9-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="239f9-169">Requirements</span></span>



| <span data-ttu-id="239f9-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="239f9-170">Requirement</span></span> | <span data-ttu-id="239f9-171">Valore</span><span class="sxs-lookup"><span data-stu-id="239f9-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="239f9-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="239f9-172">Minimum supported client</span></span><br/> | <span data-ttu-id="239f9-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="239f9-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="239f9-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="239f9-174">Minimum supported server</span></span><br/> | <span data-ttu-id="239f9-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="239f9-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="239f9-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="239f9-176">Namespace</span></span><br/>                | <span data-ttu-id="239f9-177">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="239f9-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="239f9-178">MOF</span><span class="sxs-lookup"><span data-stu-id="239f9-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="239f9-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="239f9-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="239f9-180">DLL</span><span class="sxs-lookup"><span data-stu-id="239f9-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="239f9-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="239f9-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239f9-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="239f9-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239f9-183">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="239f9-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="239f9-184">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="239f9-184">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

