---
description: La \_ classe WMI LoadOrderGroup Win32 rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127483"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="2cc6b-103">Win32 \_ LoadOrderGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="2cc6b-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="2cc6b-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LoadOrderGroup Win32** rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="2cc6b-105">I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="2cc6b-106">Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="2cc6b-107">I dati in questa classe sono derivati dal provider dalla chiave del registro di sistema: **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="2cc6b-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2cc6b-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc6b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cc6b-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="2cc6b-111">Members</span><span class="sxs-lookup"><span data-stu-id="2cc6b-111">Members</span></span>

<span data-ttu-id="2cc6b-112">La classe **Win32 \_ LoadOrderGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2cc6b-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="2cc6b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cc6b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cc6b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cc6b-114">Properties</span></span>

<span data-ttu-id="2cc6b-115">La classe **Win32 \_ LoadOrderGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cc6b-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-120">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-120">A short textual description of the object.</span></span>

<span data-ttu-id="2cc6b-121">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cc6b-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cc6b-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-125">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-126">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-126">A textual description of the object.</span></span>

<span data-ttu-id="2cc6b-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cc6b-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cc6b-128">**DriverEnabled**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-132">Indica se il gruppo di ordini di caricamento può includere i driver insieme ai servizi di sistema.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="2cc6b-133">**GroupOrder**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-136">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-137">Sequenza in cui viene caricato il gruppo di servizi nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="2cc6b-138">Esempio: 2</span><span class="sxs-lookup"><span data-stu-id="2cc6b-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="2cc6b-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-142">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-143">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-143">Indicates when the object was installed.</span></span> <span data-ttu-id="2cc6b-144">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2cc6b-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cc6b-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cc6b-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-149">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-150">Nome del gruppo dell'ordine di caricamento.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-150">Name of the load order group.</span></span>

<span data-ttu-id="2cc6b-151">Esempio: "disco principale"</span><span class="sxs-lookup"><span data-stu-id="2cc6b-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="2cc6b-152">**Status**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc6b-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc6b-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc6b-155">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2cc6b-156">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="2cc6b-157">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2cc6b-158">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="2cc6b-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2cc6b-159">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2cc6b-160">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="2cc6b-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2cc6b-161">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2cc6b-162">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2cc6b-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cc6b-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2cc6b-164">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2cc6b-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2cc6b-165">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2cc6b-166">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2cc6b-167">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2cc6b-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2cc6b-168">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2cc6b-169">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2cc6b-170">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2cc6b-171">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2cc6b-172">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2cc6b-173">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2cc6b-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2cc6b-174">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2cc6b-175">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2cc6b-176">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2cc6b-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2cc6b-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2cc6b-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2cc6b-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cc6b-178">Remarks</span></span>

<span data-ttu-id="2cc6b-179">La classe **Win32 \_ LoadOrderGroup** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cc6b-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc6b-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cc6b-180">Requirements</span></span>



| <span data-ttu-id="2cc6b-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc6b-181">Requirement</span></span> | <span data-ttu-id="2cc6b-182">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc6b-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc6b-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc6b-183">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc6b-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cc6b-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2cc6b-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc6b-185">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc6b-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cc6b-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2cc6b-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2cc6b-187">Namespace</span></span><br/>                | <span data-ttu-id="2cc6b-188">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2cc6b-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2cc6b-189">MOF</span><span class="sxs-lookup"><span data-stu-id="2cc6b-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cc6b-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cc6b-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cc6b-191">DLL</span><span class="sxs-lookup"><span data-stu-id="2cc6b-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cc6b-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cc6b-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc6b-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cc6b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc6b-194">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="2cc6b-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="2cc6b-195">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2cc6b-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

