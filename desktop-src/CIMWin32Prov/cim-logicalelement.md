---
description: La \_ classe CIM LogicalElement è la classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità del sistema, sotto forma di dispositivi logici.
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: Classe CIM_LogicalElement (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877409"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="aee89-103">Classe CIM_LogicalElement (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="aee89-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="aee89-104">La classe **CIM \_ LogicalElement** è la classe di base per tutti i componenti di sistema che rappresentano componenti di sistema astratti, ad esempio profili, processi o funzionalità del sistema, sotto forma di dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="aee89-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aee89-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="aee89-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aee89-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aee89-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aee89-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aee89-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aee89-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="aee89-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee89-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aee89-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="aee89-110">Members</span><span class="sxs-lookup"><span data-stu-id="aee89-110">Members</span></span>

<span data-ttu-id="aee89-111">La classe **CIM \_ LogicalElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aee89-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="aee89-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aee89-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aee89-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aee89-113">Properties</span></span>

<span data-ttu-id="aee89-114">La classe **CIM \_ LogicalElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aee89-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aee89-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="aee89-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee89-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aee89-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee89-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aee89-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee89-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aee89-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aee89-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aee89-119">A short textual description of the object.</span></span>

<span data-ttu-id="aee89-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee89-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee89-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="aee89-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee89-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aee89-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee89-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aee89-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee89-124">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="aee89-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aee89-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aee89-125">A textual description of the object.</span></span>

<span data-ttu-id="aee89-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee89-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee89-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aee89-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee89-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aee89-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aee89-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aee89-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee89-130">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="aee89-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aee89-131">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="aee89-131">Indicates when the object was installed.</span></span> <span data-ttu-id="aee89-132">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="aee89-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="aee89-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee89-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee89-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="aee89-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee89-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aee89-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee89-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aee89-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee89-137">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aee89-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aee89-138">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="aee89-138">Label by which the object is known.</span></span> <span data-ttu-id="aee89-139">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="aee89-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="aee89-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee89-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee89-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="aee89-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee89-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aee89-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee89-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aee89-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee89-144">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="aee89-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aee89-145">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aee89-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="aee89-146">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="aee89-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="aee89-147">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="aee89-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="aee89-148">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="aee89-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="aee89-149">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="aee89-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aee89-150">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="aee89-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aee89-151">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="aee89-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aee89-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee89-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aee89-153">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aee89-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aee89-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="aee89-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aee89-155">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="aee89-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aee89-156">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="aee89-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aee89-157">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aee89-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aee89-158">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="aee89-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aee89-159">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="aee89-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aee89-160">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="aee89-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aee89-161">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="aee89-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aee89-162">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="aee89-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aee89-163">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="aee89-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aee89-164">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="aee89-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aee89-165">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="aee89-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="aee89-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aee89-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="aee89-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="aee89-167">Remarks</span></span>

<span data-ttu-id="aee89-168">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="aee89-168">WMI does not implement this class.</span></span> <span data-ttu-id="aee89-169">Per le classi derivate da **CIM \_ LogicalElement**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aee89-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aee89-170">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="aee89-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aee89-171">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="aee89-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee89-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aee89-172">Requirements</span></span>



| <span data-ttu-id="aee89-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee89-173">Requirement</span></span> | <span data-ttu-id="aee89-174">Valore</span><span class="sxs-lookup"><span data-stu-id="aee89-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee89-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee89-175">Minimum supported client</span></span><br/> | <span data-ttu-id="aee89-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee89-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aee89-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee89-177">Minimum supported server</span></span><br/> | <span data-ttu-id="aee89-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee89-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aee89-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aee89-179">Namespace</span></span><br/>                | <span data-ttu-id="aee89-180">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aee89-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aee89-181">MOF</span><span class="sxs-lookup"><span data-stu-id="aee89-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aee89-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aee89-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aee89-183">DLL</span><span class="sxs-lookup"><span data-stu-id="aee89-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee89-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee89-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee89-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aee89-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee89-186">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="aee89-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

