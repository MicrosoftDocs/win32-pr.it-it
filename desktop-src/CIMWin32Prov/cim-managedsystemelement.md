---
description: La \_ classe CIM ManagedSystemElement è la classe di base per la gerarchia degli elementi di sistema. Qualsiasi componente di sistema distinguibile è un candidato per l'inclusione in questa classe.
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: Classe CIM_ManagedSystemElement (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126943"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="8dfdc-104">Classe CIM_ManagedSystemElement (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8dfdc-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8dfdc-105">La classe **CIM \_ ManagedSystemElement** è la classe di base per la gerarchia degli elementi di sistema.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="8dfdc-106">Qualsiasi componente di sistema distinguibile è un candidato per l'inclusione in questa classe.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="8dfdc-107">Gli esempi includono componenti software, ad esempio file; dispositivi, ad esempio unità disco e controller; e componenti fisici, ad esempio chip e schede.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dfdc-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8dfdc-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8dfdc-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8dfdc-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8dfdc-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfdc-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8dfdc-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8dfdc-113">Members</span><span class="sxs-lookup"><span data-stu-id="8dfdc-113">Members</span></span>

<span data-ttu-id="8dfdc-114">La classe **CIM \_ ManagedSystemElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8dfdc-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="8dfdc-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8dfdc-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dfdc-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8dfdc-116">Properties</span></span>

<span data-ttu-id="8dfdc-117">La classe **CIM \_ ManagedSystemElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dfdc-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdc-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8dfdc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8dfdc-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8dfdc-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdc-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8dfdc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-126">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8dfdc-127">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8dfdc-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdc-129">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8dfdc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8dfdc-132">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-132">Indicates when the object was installed.</span></span> <span data-ttu-id="8dfdc-133">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="8dfdc-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdc-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8dfdc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-137">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8dfdc-138">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-138">Label by which the object is known.</span></span> <span data-ttu-id="8dfdc-139">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="8dfdc-140">**Status**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdc-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8dfdc-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8dfdc-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdc-143">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8dfdc-144">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="8dfdc-145">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8dfdc-146">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="8dfdc-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8dfdc-147">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8dfdc-148">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="8dfdc-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8dfdc-149">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8dfdc-150">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8dfdc-151">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8dfdc-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8dfdc-152">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8dfdc-153">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8dfdc-154">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="8dfdc-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8dfdc-155">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8dfdc-156">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8dfdc-157">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8dfdc-158">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8dfdc-159">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8dfdc-160">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="8dfdc-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8dfdc-161">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8dfdc-162">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8dfdc-163">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="8dfdc-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8dfdc-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8dfdc-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8dfdc-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="8dfdc-165">Remarks</span></span>

<span data-ttu-id="8dfdc-166">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-166">WMI does not implement this class.</span></span> <span data-ttu-id="8dfdc-167">Per le classi WMI derivate da questa classe, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8dfdc-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8dfdc-168">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8dfdc-169">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfdc-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dfdc-170">Requirements</span></span>



| <span data-ttu-id="8dfdc-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dfdc-171">Requirement</span></span> | <span data-ttu-id="8dfdc-172">Valore</span><span class="sxs-lookup"><span data-stu-id="8dfdc-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfdc-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dfdc-173">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfdc-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dfdc-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8dfdc-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dfdc-175">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfdc-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dfdc-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8dfdc-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8dfdc-177">Namespace</span></span><br/>                | <span data-ttu-id="8dfdc-178">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8dfdc-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8dfdc-179">MOF</span><span class="sxs-lookup"><span data-stu-id="8dfdc-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dfdc-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8dfdc-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dfdc-181">DLL</span><span class="sxs-lookup"><span data-stu-id="8dfdc-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dfdc-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dfdc-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

