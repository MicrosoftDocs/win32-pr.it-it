---
description: La \_ classe WMI astratta ComClass di Win32 rappresenta le proprietà di un componente Component Object Model (com).
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Classe Win32_COMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966267"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="e0b46-103">\_Classe ComClass Win32</span><span class="sxs-lookup"><span data-stu-id="e0b46-103">Win32\_COMClass class</span></span>

<span data-ttu-id="e0b46-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) astratta **\_ ComClass di Win32** rappresenta le proprietà di un componente Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="e0b46-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="e0b46-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e0b46-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e0b46-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e0b46-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b46-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0b46-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="e0b46-108">Members</span><span class="sxs-lookup"><span data-stu-id="e0b46-108">Members</span></span>

<span data-ttu-id="e0b46-109">I tipi di membri della classe **\_ comclasse Win32** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0b46-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="e0b46-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0b46-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b46-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0b46-111">Properties</span></span>

<span data-ttu-id="e0b46-112">La classe di **\_ comclasse Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0b46-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0b46-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e0b46-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b46-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0b46-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0b46-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e0b46-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e0b46-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0b46-117">A short textual description of the object.</span></span>

<span data-ttu-id="e0b46-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0b46-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0b46-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e0b46-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b46-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0b46-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0b46-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-122">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e0b46-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e0b46-123">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0b46-123">A textual description of the object.</span></span>

<span data-ttu-id="e0b46-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0b46-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0b46-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e0b46-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b46-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0b46-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0b46-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="e0b46-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e0b46-129">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="e0b46-129">Indicates when the object was installed.</span></span> <span data-ttu-id="e0b46-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="e0b46-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e0b46-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0b46-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0b46-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e0b46-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b46-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0b46-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0b46-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-135">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e0b46-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e0b46-136">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e0b46-136">Label by which the object is known.</span></span> <span data-ttu-id="e0b46-137">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="e0b46-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e0b46-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0b46-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0b46-139">**Status**</span><span class="sxs-lookup"><span data-stu-id="e0b46-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b46-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0b46-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0b46-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b46-142">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e0b46-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e0b46-143">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0b46-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="e0b46-144">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="e0b46-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e0b46-145">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="e0b46-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e0b46-146">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="e0b46-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e0b46-147">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="e0b46-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e0b46-148">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="e0b46-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e0b46-149">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="e0b46-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e0b46-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0b46-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e0b46-151">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0b46-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e0b46-152">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e0b46-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e0b46-153">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="e0b46-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e0b46-154">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="e0b46-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e0b46-155">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e0b46-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e0b46-156">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="e0b46-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e0b46-157">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e0b46-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e0b46-158">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="e0b46-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e0b46-159">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="e0b46-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e0b46-160">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="e0b46-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e0b46-161">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="e0b46-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e0b46-162">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="e0b46-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e0b46-163">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="e0b46-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="e0b46-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e0b46-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e0b46-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0b46-165">Remarks</span></span>

<span data-ttu-id="e0b46-166">La classe di **\_ comclasse Win32** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0b46-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b46-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0b46-167">Requirements</span></span>



| <span data-ttu-id="e0b46-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b46-168">Requirement</span></span> | <span data-ttu-id="e0b46-169">Valore</span><span class="sxs-lookup"><span data-stu-id="e0b46-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b46-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b46-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b46-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0b46-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0b46-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b46-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b46-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0b46-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0b46-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0b46-174">Namespace</span></span><br/>                | <span data-ttu-id="e0b46-175">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e0b46-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0b46-176">MOF</span><span class="sxs-lookup"><span data-stu-id="e0b46-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0b46-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0b46-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0b46-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b46-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b46-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b46-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b46-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0b46-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b46-181">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="e0b46-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="e0b46-182">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0b46-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

