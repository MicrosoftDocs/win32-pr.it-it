---
description: La \_ classe WMI networkclient Win32 rappresenta un client di rete in un sistema Windows. Qualsiasi sistema di computer nella rete con una relazione client con il sistema è un discendente (o membro) di questa classe.
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Classe Win32_NetworkClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966296"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="a4398-104">Win32 \_ networkclient (classe)</span><span class="sxs-lookup"><span data-stu-id="a4398-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="a4398-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ networkclient Win32** rappresenta un client di rete in un sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="a4398-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="a4398-106">Qualsiasi sistema di computer nella rete con una relazione client con il sistema è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a4398-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="a4398-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a4398-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a4398-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a4398-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4398-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4398-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="a4398-110">Members</span><span class="sxs-lookup"><span data-stu-id="a4398-110">Members</span></span>

<span data-ttu-id="a4398-111">La classe **Win32 \_ networkclient** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a4398-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="a4398-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4398-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4398-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4398-113">Properties</span></span>

<span data-ttu-id="a4398-114">La classe **Win32 \_ networkclient** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4398-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4398-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a4398-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4398-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4398-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4398-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4398-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4398-118">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a4398-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a4398-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4398-119">A short textual description of the object.</span></span>

<span data-ttu-id="a4398-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4398-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4398-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a4398-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4398-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4398-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4398-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4398-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4398-124">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a4398-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a4398-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4398-125">A textual description of the object.</span></span>

<span data-ttu-id="a4398-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4398-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4398-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a4398-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4398-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a4398-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a4398-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4398-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4398-130">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a4398-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a4398-131">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a4398-131">Indicates when the object was installed.</span></span> <span data-ttu-id="a4398-132">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a4398-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a4398-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4398-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4398-134">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="a4398-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4398-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4398-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4398-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4398-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4398-137">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| MFG")</span><span class="sxs-lookup"><span data-stu-id="a4398-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="a4398-138">Nome del produttore del client di rete in esecuzione nel computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="a4398-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="a4398-139">Esempio: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="a4398-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="a4398-140">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a4398-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4398-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4398-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4398-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4398-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4398-143">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| Name")</span><span class="sxs-lookup"><span data-stu-id="a4398-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="a4398-144">Nome di rete del client di rete in esecuzione nel computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="a4398-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="a4398-145">Esempio: "rete Microsoft Windows"</span><span class="sxs-lookup"><span data-stu-id="a4398-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="a4398-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="a4398-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4398-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4398-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4398-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4398-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4398-149">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a4398-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a4398-150">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4398-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="a4398-151">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a4398-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a4398-152">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a4398-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a4398-153">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a4398-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a4398-154">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a4398-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a4398-155">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a4398-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a4398-156">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a4398-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a4398-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4398-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a4398-158">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4398-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a4398-159">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a4398-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a4398-160">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a4398-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a4398-161">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a4398-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a4398-162">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a4398-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a4398-163">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a4398-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a4398-164">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a4398-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a4398-165">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a4398-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a4398-166">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a4398-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a4398-167">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a4398-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a4398-168">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a4398-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a4398-169">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a4398-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a4398-170">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a4398-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a4398-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a4398-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a4398-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4398-172">Remarks</span></span>

<span data-ttu-id="a4398-173">La classe **Win32 \_ networkclient** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a4398-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4398-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4398-174">Requirements</span></span>



| <span data-ttu-id="a4398-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4398-175">Requirement</span></span> | <span data-ttu-id="a4398-176">Valore</span><span class="sxs-lookup"><span data-stu-id="a4398-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4398-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4398-177">Minimum supported client</span></span><br/> | <span data-ttu-id="a4398-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4398-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4398-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4398-179">Minimum supported server</span></span><br/> | <span data-ttu-id="a4398-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4398-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4398-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4398-181">Namespace</span></span><br/>                | <span data-ttu-id="a4398-182">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a4398-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4398-183">MOF</span><span class="sxs-lookup"><span data-stu-id="a4398-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4398-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4398-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4398-185">DLL</span><span class="sxs-lookup"><span data-stu-id="a4398-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4398-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4398-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4398-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4398-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4398-188">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a4398-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="a4398-189">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a4398-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
