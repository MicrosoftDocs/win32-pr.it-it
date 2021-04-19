---
description: La \_ classe CIM MemoryCheck specifica una condizione per la quantità minima di memoria che deve essere disponibile in un sistema.
ms.assetid: a7d22f31-a285-41c4-b069-47c54865ddf5
ms.tgt_platform: multiple
title: Classe CIM_MemoryCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck
- CIM_MemoryCheck.CheckID
- CIM_MemoryCheck.Caption
- CIM_MemoryCheck.Description
- CIM_MemoryCheck.CheckMode
- CIM_MemoryCheck.Name
- CIM_MemoryCheck.TargetOperatingSystem
- CIM_MemoryCheck.Version
- CIM_MemoryCheck.SoftwareElementID
- CIM_MemoryCheck.SoftwareElementState
- CIM_MemoryCheck.MemorySize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4265b108bd57bcb91aa903fd163ff14bd91311ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304966"
---
# <a name="cim_memorycheck-class"></a><span data-ttu-id="63a86-103">CIM \_ MemoryCheck (classe)</span><span class="sxs-lookup"><span data-stu-id="63a86-103">CIM\_MemoryCheck class</span></span>

<span data-ttu-id="63a86-104">La classe **CIM \_ MemoryCheck** specifica una condizione per la quantità minima di memoria che deve essere disponibile in un sistema.</span><span class="sxs-lookup"><span data-stu-id="63a86-104">The **CIM\_MemoryCheck** class specifies a condition for the minimum amount of memory that must be available on a system.</span></span> <span data-ttu-id="63a86-105">Il valore specificato nella proprietà **MemorySize** .</span><span class="sxs-lookup"><span data-stu-id="63a86-105">The amount is specified in the **MemorySize** property.</span></span> <span data-ttu-id="63a86-106">I dettagli dei controlli vengono confrontati con il valore della proprietà **FreePhysicalMemory** dell'oggetto [**CIM \_ OperatingSystem**](cim-operatingsystem.md) a cui fa riferimento un'associazione [**CIM \_ installato**](cim-installedos.md) per l'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) che descrive l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="63a86-106">Details of the checks are compared with the value of the **FreePhysicalMemory** property of the [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="63a86-107">Se il valore della proprietà **FreePhysicalMemory** è maggiore o uguale al valore specificato in **MemorySize**, la condizione viene soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="63a86-107">When the value of the **FreePhysicalMemory** property is greater than or equal to the value specified in **MemorySize**, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63a86-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="63a86-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="63a86-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="63a86-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="63a86-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="63a86-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="63a86-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="63a86-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a86-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63a86-112">Syntax</span></span>

``` syntax
[UUID("{DC0E96FE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_MemoryCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint64  MemorySize;
};
```

## <a name="members"></a><span data-ttu-id="63a86-113">Members</span><span class="sxs-lookup"><span data-stu-id="63a86-113">Members</span></span>

<span data-ttu-id="63a86-114">La classe **CIM \_ MemoryCheck** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="63a86-114">The **CIM\_MemoryCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="63a86-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="63a86-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="63a86-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63a86-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63a86-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="63a86-117">Methods</span></span>

<span data-ttu-id="63a86-118">La classe **CIM \_ MemoryCheck** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="63a86-118">The **CIM\_MemoryCheck** class has these methods.</span></span>



| <span data-ttu-id="63a86-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="63a86-119">Method</span></span>                                                   | <span data-ttu-id="63a86-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63a86-120">Description</span></span>                                                   |
|:---------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="63a86-121">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="63a86-121">**Invoke**</span></span>](invoke-method-in-class-cim-memorycheck.md) | <span data-ttu-id="63a86-122">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="63a86-122">Takes a particular action.</span></span> <span data-ttu-id="63a86-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="63a86-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="63a86-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63a86-124">Properties</span></span>

<span data-ttu-id="63a86-125">La classe **CIM \_ MemoryCheck** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="63a86-125">The **CIM\_MemoryCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63a86-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="63a86-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63a86-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="63a86-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="63a86-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="63a86-130">A short textual description of the subject.</span></span>

<span data-ttu-id="63a86-131">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="63a86-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63a86-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-135">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="63a86-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="63a86-136">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="63a86-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="63a86-137">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="63a86-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="63a86-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63a86-141">Se **true**, la condizione dovrebbe esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="63a86-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="63a86-142">Un file, ad esempio, dovrebbe trovarsi in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="63a86-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="63a86-143">Se **false**, la condizione non è prevista.</span><span class="sxs-lookup"><span data-stu-id="63a86-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="63a86-144">Un file, ad esempio, non si trova in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="63a86-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="63a86-145">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-146">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="63a86-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63a86-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63a86-149">Descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="63a86-149">A description of the objects.</span></span>

<span data-ttu-id="63a86-150">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-151">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="63a86-151">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-152">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63a86-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-154">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="63a86-154">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="63a86-155">Quantità di memoria che deve esistere in un sistema di computer per l'esecuzione corretta di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="63a86-155">Amount of memory that needs to exist on a computer system for a software element to execute properly.</span></span>

<span data-ttu-id="63a86-156">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63a86-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-157">**Nome**</span><span class="sxs-lookup"><span data-stu-id="63a86-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63a86-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-160">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="63a86-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="63a86-161">Nome usato per identificare l'elemento software</span><span class="sxs-lookup"><span data-stu-id="63a86-161">Name used to identify the software element</span></span>

<span data-ttu-id="63a86-162">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="63a86-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63a86-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-166">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="63a86-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="63a86-167">Si tratta di un identificatore per questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="63a86-167">This is an identifier for this software element.</span></span>

<span data-ttu-id="63a86-168">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a86-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="63a86-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-170">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63a86-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-172">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63a86-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63a86-173">Stato dell'elemento software di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="63a86-173">The software element state of a software element.</span></span>

<span data-ttu-id="63a86-174">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-174">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="63a86-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="63a86-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-176">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="63a86-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="63a86-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="63a86-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-178">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="63a86-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="63a86-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="63a86-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-180">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="63a86-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="63a86-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="63a86-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-182">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="63a86-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63a86-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="63a86-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63a86-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-186">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="63a86-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="63a86-187">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="63a86-187">Target operating system of the software element.</span></span>

<span data-ttu-id="63a86-188">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63a86-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="63a86-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63a86-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="63a86-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="63a86-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="63a86-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="63a86-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="63a86-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="63a86-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-194">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="63a86-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="63a86-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="63a86-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="63a86-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="63a86-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="63a86-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="63a86-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="63a86-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="63a86-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-199">Apri VM</span><span class="sxs-lookup"><span data-stu-id="63a86-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="63a86-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="63a86-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="63a86-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="63a86-202"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="63a86-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="63a86-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="63a86-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="63a86-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="63a86-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="63a86-205"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="63a86-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="63a86-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="63a86-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-207">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="63a86-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="63a86-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="63a86-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="63a86-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="63a86-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="63a86-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="63a86-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="63a86-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="63a86-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="63a86-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="63a86-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="63a86-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="63a86-215"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="63a86-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="63a86-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="63a86-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="63a86-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="63a86-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="63a86-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="63a86-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="63a86-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="63a86-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="63a86-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="63a86-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="63a86-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="63a86-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="63a86-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="63a86-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="63a86-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="63a86-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="63a86-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="63a86-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="63a86-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="63a86-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="63a86-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="63a86-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="63a86-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="63a86-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="63a86-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="63a86-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="63a86-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="63a86-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="63a86-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="63a86-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="63a86-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-233">Serie A</span><span class="sxs-lookup"><span data-stu-id="63a86-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="63a86-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="63a86-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-235">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="63a86-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="63a86-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="63a86-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-237">NT tandem</span><span class="sxs-lookup"><span data-stu-id="63a86-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="63a86-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="63a86-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="63a86-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="63a86-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="63a86-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="63a86-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="63a86-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="63a86-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="63a86-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="63a86-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="63a86-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="63a86-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="63a86-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="63a86-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="63a86-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-246">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="63a86-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="63a86-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="63a86-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="63a86-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="63a86-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="63a86-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="63a86-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="63a86-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="63a86-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="63a86-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="63a86-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="63a86-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="63a86-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="63a86-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="63a86-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="63a86-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="63a86-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="63a86-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="63a86-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="63a86-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="63a86-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="63a86-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="63a86-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="63a86-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="63a86-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="63a86-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="63a86-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="63a86-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="63a86-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="63a86-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="63a86-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="63a86-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="63a86-263">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="63a86-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="63a86-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="63a86-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="63a86-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="63a86-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="63a86-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="63a86-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="63a86-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="63a86-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="63a86-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="63a86-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63a86-269">**Versione**</span><span class="sxs-lookup"><span data-stu-id="63a86-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a86-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="63a86-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a86-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="63a86-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a86-272">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="63a86-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="63a86-273">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="63a86-273">Version of the operation.</span></span>

<span data-ttu-id="63a86-274">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="63a86-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="63a86-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="63a86-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="63a86-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="63a86-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="63a86-277">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63a86-278">Commenti</span><span class="sxs-lookup"><span data-stu-id="63a86-278">Remarks</span></span>

<span data-ttu-id="63a86-279">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="63a86-279">WMI does not implement this class.</span></span>

<span data-ttu-id="63a86-280">La classe **CIM \_ MemoryCheck** viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="63a86-280">The **CIM\_MemoryCheck** class is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<span data-ttu-id="63a86-281">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="63a86-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="63a86-282">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="63a86-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a86-283">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63a86-283">Requirements</span></span>



| <span data-ttu-id="63a86-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a86-284">Requirement</span></span> | <span data-ttu-id="63a86-285">Valore</span><span class="sxs-lookup"><span data-stu-id="63a86-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63a86-286">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63a86-286">Minimum supported client</span></span><br/> | <span data-ttu-id="63a86-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63a86-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63a86-288">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63a86-288">Minimum supported server</span></span><br/> | <span data-ttu-id="63a86-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63a86-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63a86-290">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="63a86-290">Namespace</span></span><br/>                | <span data-ttu-id="63a86-291">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="63a86-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63a86-292">MOF</span><span class="sxs-lookup"><span data-stu-id="63a86-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63a86-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63a86-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63a86-294">DLL</span><span class="sxs-lookup"><span data-stu-id="63a86-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63a86-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a86-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a86-296">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63a86-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a86-297">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="63a86-297">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

