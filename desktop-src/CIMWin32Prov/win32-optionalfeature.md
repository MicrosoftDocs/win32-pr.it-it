---
description: Rappresenta lo stato delle funzionalità facoltative presenti nel sistema operativo.
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: Classe Win32_OptionalFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305161"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="fde62-103">Win32 \_ OptionalFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="fde62-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="fde62-104">Rappresenta lo stato delle funzionalità facoltative presenti nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fde62-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="fde62-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fde62-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde62-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fde62-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="fde62-107">Members</span><span class="sxs-lookup"><span data-stu-id="fde62-107">Members</span></span>

<span data-ttu-id="fde62-108">La classe **Win32 \_ OptionalFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fde62-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="fde62-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fde62-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fde62-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fde62-110">Properties</span></span>

<span data-ttu-id="fde62-111">La classe **Win32 \_ OptionalFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fde62-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fde62-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fde62-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde62-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fde62-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde62-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fde62-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde62-115">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) (didascalia), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="fde62-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="fde62-116">Nome visualizzato della funzionalità facoltativa.</span><span class="sxs-lookup"><span data-stu-id="fde62-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="fde62-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fde62-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde62-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fde62-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde62-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fde62-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde62-120">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fde62-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fde62-121">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fde62-121">A textual description of the object.</span></span>

<span data-ttu-id="fde62-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fde62-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fde62-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fde62-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde62-124">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fde62-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fde62-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fde62-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde62-126">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="fde62-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fde62-127">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="fde62-127">Indicates when the object was installed.</span></span> <span data-ttu-id="fde62-128">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="fde62-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fde62-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fde62-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fde62-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="fde62-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde62-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fde62-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fde62-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fde62-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fde62-133">Identifica lo stato della funzionalità facoltativa.</span><span class="sxs-lookup"><span data-stu-id="fde62-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="fde62-134">Sono possibili gli Stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="fde62-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fde62-135">**Abilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="fde62-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fde62-136">**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="fde62-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="fde62-137">**Assente** (3)</span><span class="sxs-lookup"><span data-stu-id="fde62-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fde62-138">**Sconosciuto** (4)</span><span class="sxs-lookup"><span data-stu-id="fde62-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fde62-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fde62-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde62-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fde62-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde62-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fde62-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde62-142">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) (Name), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="fde62-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="fde62-143">Rappresenta il nome della funzionalità facoltativa.</span><span class="sxs-lookup"><span data-stu-id="fde62-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="fde62-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="fde62-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde62-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fde62-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde62-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fde62-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde62-147">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="fde62-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fde62-148">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fde62-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="fde62-149">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="fde62-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fde62-150">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="fde62-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fde62-151">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="fde62-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fde62-152">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="fde62-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fde62-153">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="fde62-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fde62-154">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="fde62-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fde62-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fde62-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fde62-156">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fde62-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fde62-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="fde62-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fde62-158">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="fde62-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fde62-159">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="fde62-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fde62-160">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="fde62-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fde62-161">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="fde62-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fde62-162">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="fde62-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fde62-163">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="fde62-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fde62-164">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="fde62-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fde62-165">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="fde62-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fde62-166">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="fde62-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fde62-167">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="fde62-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fde62-168">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="fde62-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="fde62-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fde62-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fde62-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fde62-170">Requirements</span></span>



| <span data-ttu-id="fde62-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde62-171">Requirement</span></span> | <span data-ttu-id="fde62-172">Valore</span><span class="sxs-lookup"><span data-stu-id="fde62-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde62-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fde62-173">Minimum supported client</span></span><br/> | <span data-ttu-id="fde62-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fde62-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="fde62-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fde62-175">Minimum supported server</span></span><br/> | <span data-ttu-id="fde62-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fde62-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="fde62-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fde62-177">Namespace</span></span><br/>                | <span data-ttu-id="fde62-178">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fde62-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fde62-179">MOF</span><span class="sxs-lookup"><span data-stu-id="fde62-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fde62-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fde62-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fde62-181">DLL</span><span class="sxs-lookup"><span data-stu-id="fde62-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde62-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde62-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde62-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fde62-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde62-184">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="fde62-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="fde62-185">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fde62-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="fde62-186">Esecuzione di query sullo stato delle funzionalità facoltative</span><span class="sxs-lookup"><span data-stu-id="fde62-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
