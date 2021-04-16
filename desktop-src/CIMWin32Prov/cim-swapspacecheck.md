---
description: La \_ classe CIM SwapSpaceCheck specifica la quantità di spazio di swapping che deve essere disponibile nel sistema.
ms.assetid: c5e5ec68-bc62-4bdf-93b7-ce868e738dee
ms.tgt_platform: multiple
title: Classe CIM_SwapSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwapSpaceCheck
- CIM_SwapSpaceCheck.CheckID
- CIM_SwapSpaceCheck.Caption
- CIM_SwapSpaceCheck.Description
- CIM_SwapSpaceCheck.CheckMode
- CIM_SwapSpaceCheck.Name
- CIM_SwapSpaceCheck.TargetOperatingSystem
- CIM_SwapSpaceCheck.Version
- CIM_SwapSpaceCheck.SoftwareElementID
- CIM_SwapSpaceCheck.SoftwareElementState
- CIM_SwapSpaceCheck.SwapSpaceSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992d8a314797c7a977e9a672ecb9d3dcdb561292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523810"
---
# <a name="cim_swapspacecheck-class"></a><span data-ttu-id="416d8-103">CIM \_ SwapSpaceCheck (classe)</span><span class="sxs-lookup"><span data-stu-id="416d8-103">CIM\_SwapSpaceCheck class</span></span>

<span data-ttu-id="416d8-104">La classe **CIM \_ SwapSpaceCheck** specifica la quantità di spazio di swapping che deve essere disponibile nel sistema.</span><span class="sxs-lookup"><span data-stu-id="416d8-104">The **CIM\_SwapSpaceCheck** class specifies the amount of swap space that must be available on the system.</span></span> <span data-ttu-id="416d8-105">Il valore specificato nella proprietà **SwapSpaceSize** .</span><span class="sxs-lookup"><span data-stu-id="416d8-105">The amount is specified in the **SwapSpaceSize** property.</span></span> <span data-ttu-id="416d8-106">I dettagli di questo controllo vengono confrontati con i dettagli corrispondenti presenti in un oggetto [**CIM \_ OperatingSystem**](cim-operatingsystem.md) a cui fa riferimento l'associazione [**CIM \_ Installatoos**](cim-installedos.md) per l'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) che descrive l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="416d8-106">Details of this check are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by the [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="416d8-107">Se il valore della proprietà **TotalSwapSpaceSize** è maggiore o uguale al valore specificato nella proprietà **SwapSpaceSize** , la condizione viene soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="416d8-107">When the value of the **TotalSwapSpaceSize** property is greater than or equal to the value specified in the **SwapSpaceSize** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="416d8-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="416d8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="416d8-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="416d8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="416d8-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="416d8-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="416d8-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="416d8-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="416d8-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="416d8-112">Syntax</span></span>

``` syntax
[UUID("{A5AE701E-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SwapSpaceCheck : CIM_Check
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
  uint64  SwapSpaceSize;
};
```

## <a name="members"></a><span data-ttu-id="416d8-113">Members</span><span class="sxs-lookup"><span data-stu-id="416d8-113">Members</span></span>

<span data-ttu-id="416d8-114">La classe **CIM \_ SwapSpaceCheck** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="416d8-114">The **CIM\_SwapSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="416d8-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="416d8-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="416d8-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="416d8-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="416d8-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="416d8-117">Methods</span></span>

<span data-ttu-id="416d8-118">La classe **CIM \_ SwapSpaceCheck** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="416d8-118">The **CIM\_SwapSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="416d8-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="416d8-119">Method</span></span>                                                      | <span data-ttu-id="416d8-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="416d8-120">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="416d8-121">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="416d8-121">**Invoke**</span></span>](invoke-method-in-class-cim-swapspacecheck.md) | <span data-ttu-id="416d8-122">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="416d8-122">Takes a particular action.</span></span> <span data-ttu-id="416d8-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="416d8-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="416d8-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="416d8-124">Properties</span></span>

<span data-ttu-id="416d8-125">La classe **CIM \_ SwapSpaceCheck** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="416d8-125">The **CIM\_SwapSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="416d8-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="416d8-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="416d8-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="416d8-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="416d8-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="416d8-130">A short textual description of the subject.</span></span>

<span data-ttu-id="416d8-131">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="416d8-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="416d8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-135">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="416d8-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="416d8-136">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="416d8-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="416d8-137">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="416d8-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="416d8-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416d8-141">Se **true**, la condizione dovrebbe esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="416d8-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="416d8-142">Un file, ad esempio, dovrebbe trovarsi in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="416d8-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="416d8-143">Se **false**, la condizione non è prevista.</span><span class="sxs-lookup"><span data-stu-id="416d8-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="416d8-144">Un file, ad esempio, non si trova in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="416d8-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="416d8-145">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-146">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="416d8-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="416d8-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416d8-149">Descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="416d8-149">A description of the objects.</span></span>

<span data-ttu-id="416d8-150">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-151">**Nome**</span><span class="sxs-lookup"><span data-stu-id="416d8-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="416d8-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-154">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="416d8-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="416d8-155">Nome usato per identificare l'elemento software</span><span class="sxs-lookup"><span data-stu-id="416d8-155">Name used to identify the software element</span></span>

<span data-ttu-id="416d8-156">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-156">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-157">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="416d8-157">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="416d8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-160">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="416d8-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="416d8-161">Si tratta di un identificatore per questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="416d8-161">This is an identifier for this software element.</span></span>

<span data-ttu-id="416d8-162">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-163">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="416d8-163">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416d8-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-166">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="416d8-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="416d8-167">Stato dell'elemento software di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="416d8-167">The software element state of a software element.</span></span>

<span data-ttu-id="416d8-168">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="416d8-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="416d8-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-170">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="416d8-170">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="416d8-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="416d8-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-172">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="416d8-172">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="416d8-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="416d8-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-174">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="416d8-174">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="416d8-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="416d8-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-176">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="416d8-176">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="416d8-177">**SwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="416d8-177">**SwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-178">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="416d8-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-180">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="416d8-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="416d8-181">Dimensioni minime dello spazio di swapping, in kilobyte, che devono essere disponibili nel sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="416d8-181">Minimum swap-space size, in kilobytes, that must be available on the target system.</span></span>

<span data-ttu-id="416d8-182">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="416d8-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="416d8-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="416d8-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416d8-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-186">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="416d8-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="416d8-187">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="416d8-187">Target operating system of the software element.</span></span>

<span data-ttu-id="416d8-188">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="416d8-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="416d8-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="416d8-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="416d8-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="416d8-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="416d8-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="416d8-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="416d8-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="416d8-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-194">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="416d8-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="416d8-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="416d8-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="416d8-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="416d8-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="416d8-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="416d8-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="416d8-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="416d8-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-199">Apri VM</span><span class="sxs-lookup"><span data-stu-id="416d8-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="416d8-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="416d8-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="416d8-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="416d8-202"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="416d8-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="416d8-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="416d8-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="416d8-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="416d8-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="416d8-205"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="416d8-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="416d8-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="416d8-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-207">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="416d8-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="416d8-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="416d8-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="416d8-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="416d8-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="416d8-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="416d8-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="416d8-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="416d8-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="416d8-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="416d8-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="416d8-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="416d8-215"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="416d8-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="416d8-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="416d8-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="416d8-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="416d8-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="416d8-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="416d8-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="416d8-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="416d8-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="416d8-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="416d8-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="416d8-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="416d8-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="416d8-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="416d8-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="416d8-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="416d8-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="416d8-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="416d8-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="416d8-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="416d8-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="416d8-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="416d8-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="416d8-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="416d8-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="416d8-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="416d8-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="416d8-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="416d8-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="416d8-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="416d8-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="416d8-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-233">Serie A</span><span class="sxs-lookup"><span data-stu-id="416d8-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="416d8-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="416d8-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-235">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="416d8-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="416d8-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="416d8-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-237">NT tandem</span><span class="sxs-lookup"><span data-stu-id="416d8-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="416d8-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="416d8-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="416d8-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="416d8-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="416d8-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="416d8-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="416d8-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="416d8-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="416d8-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="416d8-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="416d8-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="416d8-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="416d8-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="416d8-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="416d8-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-246">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="416d8-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="416d8-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="416d8-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="416d8-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="416d8-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="416d8-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="416d8-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="416d8-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="416d8-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="416d8-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="416d8-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="416d8-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="416d8-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="416d8-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="416d8-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="416d8-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="416d8-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="416d8-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="416d8-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="416d8-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="416d8-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="416d8-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="416d8-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="416d8-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="416d8-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="416d8-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="416d8-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="416d8-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="416d8-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="416d8-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="416d8-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="416d8-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="416d8-263">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="416d8-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="416d8-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="416d8-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="416d8-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="416d8-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="416d8-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="416d8-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="416d8-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="416d8-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="416d8-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="416d8-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="416d8-269">**Versione**</span><span class="sxs-lookup"><span data-stu-id="416d8-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416d8-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="416d8-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416d8-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="416d8-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416d8-272">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="416d8-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="416d8-273">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="416d8-273">Version of the operation.</span></span>

<span data-ttu-id="416d8-274">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="416d8-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="416d8-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="416d8-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="416d8-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="416d8-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="416d8-277">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="416d8-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="416d8-278">Commenti</span><span class="sxs-lookup"><span data-stu-id="416d8-278">Remarks</span></span>

<span data-ttu-id="416d8-279">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="416d8-279">WMI does not implement this class.</span></span>

<span data-ttu-id="416d8-280">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="416d8-280">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="416d8-281">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="416d8-281">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="416d8-282">Requisiti</span><span class="sxs-lookup"><span data-stu-id="416d8-282">Requirements</span></span>



| <span data-ttu-id="416d8-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="416d8-283">Requirement</span></span> | <span data-ttu-id="416d8-284">Valore</span><span class="sxs-lookup"><span data-stu-id="416d8-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="416d8-285">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="416d8-285">Minimum supported client</span></span><br/> | <span data-ttu-id="416d8-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="416d8-286">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="416d8-287">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="416d8-287">Minimum supported server</span></span><br/> | <span data-ttu-id="416d8-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="416d8-288">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="416d8-289">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="416d8-289">Namespace</span></span><br/>                | <span data-ttu-id="416d8-290">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="416d8-290">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="416d8-291">MOF</span><span class="sxs-lookup"><span data-stu-id="416d8-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="416d8-292"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-292"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="416d8-293">DLL</span><span class="sxs-lookup"><span data-stu-id="416d8-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416d8-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-294"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="416d8-295">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="416d8-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416d8-296">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="416d8-296">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

