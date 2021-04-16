---
description: Win32 \_ PageFileUsage&\# 8194; Classe WMI rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un sistema Win32. Le informazioni contenute all'interno di oggetti di cui è stata creata un'istanza da questa classe specificano lo stato di run-time del file di paging.
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Classe Win32_PageFileUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524097"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="d756a-104">Win32 \_ PageFileUsage (classe)</span><span class="sxs-lookup"><span data-stu-id="d756a-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="d756a-105">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileUsage Win32** rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="d756a-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="d756a-106">Le informazioni contenute all'interno di oggetti di cui è stata creata un'istanza da questa classe specificano lo stato di run-time del file di paging.</span><span class="sxs-lookup"><span data-stu-id="d756a-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="d756a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d756a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d756a-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d756a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d756a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d756a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="d756a-110">Members</span><span class="sxs-lookup"><span data-stu-id="d756a-110">Members</span></span>

<span data-ttu-id="d756a-111">La classe **Win32 \_ PageFileUsage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d756a-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="d756a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d756a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d756a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d756a-113">Properties</span></span>

<span data-ttu-id="d756a-114">La classe **Win32 \_ PageFileUsage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d756a-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d756a-115">**AllocatedBaseSize**</span><span class="sxs-lookup"><span data-stu-id="d756a-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d756a-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-118">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="d756a-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-119">Quantità effettiva di spazio su disco allocata per l'utilizzo con il file di paging.</span><span class="sxs-lookup"><span data-stu-id="d756a-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="d756a-120">Questo valore corrisponde all'intervallo stabilito in [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md) nelle proprietà **InitialSize** e **MaximumSize** , impostato all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d756a-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="d756a-121">Esempio: 178</span><span class="sxs-lookup"><span data-stu-id="d756a-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="d756a-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d756a-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d756a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-125">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d756a-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-126">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d756a-126">A short textual description of the object.</span></span>

<span data-ttu-id="d756a-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d756a-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d756a-128">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="d756a-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d756a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-131">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="d756a-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-132">Quantità di spazio su disco attualmente utilizzata dal file di paging.</span><span class="sxs-lookup"><span data-stu-id="d756a-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="d756a-133">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d756a-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d756a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-136">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d756a-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-137">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d756a-137">A textual description of the object.</span></span>

<span data-ttu-id="d756a-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d756a-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d756a-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d756a-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d756a-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-142">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="d756a-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-143">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="d756a-143">Indicates when the object was installed.</span></span> <span data-ttu-id="d756a-144">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="d756a-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d756a-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d756a-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d756a-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d756a-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d756a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-149">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d756a-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-150">Nome del file di paging.</span><span class="sxs-lookup"><span data-stu-id="d756a-150">Name of the page file.</span></span>

<span data-ttu-id="d756a-151">Esempio: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="d756a-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="d756a-152">**PeakUsage**</span><span class="sxs-lookup"><span data-stu-id="d756a-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d756a-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-155">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="d756a-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-156">File di paging con utilizzo più elevato.</span><span class="sxs-lookup"><span data-stu-id="d756a-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="d756a-157">**Status**</span><span class="sxs-lookup"><span data-stu-id="d756a-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d756a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-160">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="d756a-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-161">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d756a-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="d756a-162">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="d756a-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d756a-163">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="d756a-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d756a-164">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="d756a-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d756a-165">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="d756a-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d756a-166">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d756a-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d756a-167">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d756a-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d756a-168">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d756a-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d756a-169">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d756a-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d756a-170">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d756a-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d756a-171">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="d756a-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d756a-172">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="d756a-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d756a-173">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d756a-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d756a-174">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="d756a-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d756a-175">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="d756a-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d756a-176">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="d756a-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d756a-177">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="d756a-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d756a-178">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="d756a-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d756a-179">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="d756a-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d756a-180">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="d756a-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d756a-181">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="d756a-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d756a-182">**TempPageFile**</span><span class="sxs-lookup"><span data-stu-id="d756a-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d756a-183">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d756a-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d756a-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d756a-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d756a-185">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| TempPageFile")</span><span class="sxs-lookup"><span data-stu-id="d756a-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="d756a-186">Se **true**, è stato creato un file di paging temporaneo, in genere perché non è presente alcun file di paging permanente nel computer corrente.</span><span class="sxs-lookup"><span data-stu-id="d756a-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d756a-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="d756a-187">Remarks</span></span>

<span data-ttu-id="d756a-188">La classe **Win32 \_ PageFileUsage** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d756a-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d756a-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d756a-189">Requirements</span></span>



| <span data-ttu-id="d756a-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="d756a-190">Requirement</span></span> | <span data-ttu-id="d756a-191">Valore</span><span class="sxs-lookup"><span data-stu-id="d756a-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d756a-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d756a-192">Minimum supported client</span></span><br/> | <span data-ttu-id="d756a-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d756a-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d756a-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d756a-194">Minimum supported server</span></span><br/> | <span data-ttu-id="d756a-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d756a-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d756a-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d756a-196">Namespace</span></span><br/>                | <span data-ttu-id="d756a-197">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d756a-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d756a-198">MOF</span><span class="sxs-lookup"><span data-stu-id="d756a-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d756a-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d756a-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d756a-200">DLL</span><span class="sxs-lookup"><span data-stu-id="d756a-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d756a-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d756a-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d756a-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d756a-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d756a-203">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="d756a-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="d756a-204">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d756a-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
