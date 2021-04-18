---
description: La \_ classe WMI ClassicCOMClass Win32 rappresenta le proprietà di un componente com.
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305099"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="ad44f-103">Win32 \_ ClassicCOMClass (classe)</span><span class="sxs-lookup"><span data-stu-id="ad44f-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="ad44f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClass Win32** rappresenta le proprietà di un componente com.</span><span class="sxs-lookup"><span data-stu-id="ad44f-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="ad44f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ad44f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ad44f-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ad44f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad44f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad44f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="ad44f-108">Members</span><span class="sxs-lookup"><span data-stu-id="ad44f-108">Members</span></span>

<span data-ttu-id="ad44f-109">La classe **Win32 \_ ClassicCOMClass** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ad44f-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="ad44f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad44f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad44f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad44f-111">Properties</span></span>

<span data-ttu-id="ad44f-112">La classe **Win32 \_ ClassicCOMClass** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ad44f-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad44f-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ad44f-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad44f-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad44f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad44f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ad44f-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ad44f-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad44f-117">A short textual description of the object.</span></span>

<span data-ttu-id="ad44f-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad44f-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad44f-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="ad44f-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad44f-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad44f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad44f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-122">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Class \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="ad44f-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ad44f-123">Identificatore univoco globale (GUID) di questa classe COM.</span><span class="sxs-lookup"><span data-stu-id="ad44f-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="ad44f-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ad44f-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad44f-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad44f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad44f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-127">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ad44f-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ad44f-128">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad44f-128">A textual description of the object.</span></span>

<span data-ttu-id="ad44f-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad44f-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad44f-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ad44f-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad44f-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad44f-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad44f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-133">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ad44f-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ad44f-134">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="ad44f-134">Indicates when the object was installed.</span></span> <span data-ttu-id="ad44f-135">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="ad44f-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ad44f-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad44f-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad44f-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ad44f-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad44f-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad44f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad44f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-140">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="ad44f-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ad44f-141">La proprietà Name contiene il nome leggibile per la classe COM.</span><span class="sxs-lookup"><span data-stu-id="ad44f-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="ad44f-142">**Status**</span><span class="sxs-lookup"><span data-stu-id="ad44f-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad44f-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad44f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad44f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad44f-145">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ad44f-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ad44f-146">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad44f-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="ad44f-147">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="ad44f-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ad44f-148">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="ad44f-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ad44f-149">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="ad44f-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ad44f-150">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="ad44f-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ad44f-151">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="ad44f-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ad44f-152">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="ad44f-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ad44f-153">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad44f-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ad44f-154">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad44f-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ad44f-155">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ad44f-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ad44f-156">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ad44f-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ad44f-157">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ad44f-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad44f-158">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ad44f-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ad44f-159">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ad44f-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ad44f-160">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ad44f-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ad44f-161">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ad44f-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ad44f-162">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ad44f-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ad44f-163">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ad44f-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ad44f-164">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ad44f-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ad44f-165">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ad44f-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ad44f-166">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ad44f-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ad44f-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ad44f-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ad44f-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad44f-168">Remarks</span></span>

<span data-ttu-id="ad44f-169">La classe **Win32 \_ ClassicCOMClass** è derivata dalla [**\_ comclasse Win32**](win32-comclass.md).</span><span class="sxs-lookup"><span data-stu-id="ad44f-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad44f-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad44f-170">Requirements</span></span>



| <span data-ttu-id="ad44f-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad44f-171">Requirement</span></span> | <span data-ttu-id="ad44f-172">Valore</span><span class="sxs-lookup"><span data-stu-id="ad44f-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad44f-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad44f-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ad44f-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad44f-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad44f-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad44f-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ad44f-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad44f-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad44f-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad44f-177">Namespace</span></span><br/>                | <span data-ttu-id="ad44f-178">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ad44f-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad44f-179">MOF</span><span class="sxs-lookup"><span data-stu-id="ad44f-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad44f-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad44f-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad44f-181">DLL</span><span class="sxs-lookup"><span data-stu-id="ad44f-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad44f-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad44f-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad44f-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad44f-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad44f-184">**Comclasse Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ad44f-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="ad44f-185">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad44f-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

