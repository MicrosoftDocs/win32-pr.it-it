---
description: La \_ classe CIM SoftwareElementVersionCheck rappresenta un tipo di elemento software che deve esistere nell'ambiente.
ms.assetid: a1c0f0d5-2586-499c-bd82-bbb107570d81
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck
- CIM_SoftwareElementVersionCheck.Caption
- CIM_SoftwareElementVersionCheck.CheckID
- CIM_SoftwareElementVersionCheck.CheckMode
- CIM_SoftwareElementVersionCheck.Description
- CIM_SoftwareElementVersionCheck.LowerSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Name
- CIM_SoftwareElementVersionCheck.SoftwareElementID
- CIM_SoftwareElementVersionCheck.SoftwareElementName
- CIM_SoftwareElementVersionCheck.SoftwareElementState
- CIM_SoftwareElementVersionCheck.SoftwareElementStateDesired
- CIM_SoftwareElementVersionCheck.TargetOperatingSystem
- CIM_SoftwareElementVersionCheck.TargetOperatingSystemDesired
- CIM_SoftwareElementVersionCheck.UpperSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb55a44a3aba9092567cdc91b668ba1b63e33174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225529"
---
# <a name="cim_softwareelementversioncheck-class"></a><span data-ttu-id="f96e9-103">CIM \_ SoftwareElementVersionCheck (classe)</span><span class="sxs-lookup"><span data-stu-id="f96e9-103">CIM\_SoftwareElementVersionCheck class</span></span>

<span data-ttu-id="f96e9-104">La classe **CIM \_ SoftwareElementVersionCheck** rappresenta un tipo di elemento software che deve esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="f96e9-104">The **CIM\_SoftwareElementVersionCheck** class represents a type of software element that must exist in the environment.</span></span> <span data-ttu-id="f96e9-105">Questo controllo può essere per un valore specifico, minimo, massimo o un intervallo di versioni.</span><span class="sxs-lookup"><span data-stu-id="f96e9-105">This check can be for a specific, minimum, maximum, or a range of versions.</span></span> <span data-ttu-id="f96e9-106">Per specificare una versione specifica, le versioni inferiore e superiore devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="f96e9-106">To specify a specific version, the lower and upper versions must be the same.</span></span> <span data-ttu-id="f96e9-107">Per specificare una versione minima, specificare solo la versione precedente.</span><span class="sxs-lookup"><span data-stu-id="f96e9-107">To specify a minimum version, specify only the lower version.</span></span> <span data-ttu-id="f96e9-108">Per specificare una versione massima, specificare solo la versione superiore.</span><span class="sxs-lookup"><span data-stu-id="f96e9-108">To specify a maximum version, specify only the upper version.</span></span> <span data-ttu-id="f96e9-109">Per specificare un intervallo, è necessario specificare entrambe le versioni superiore e inferiore.</span><span class="sxs-lookup"><span data-stu-id="f96e9-109">To specify a range, both upper and lower versions must be specified.</span></span> <span data-ttu-id="f96e9-110">I dettagli dei controlli vengono confrontati con i dettagli corrispondenti presenti in un oggetto [**CIM \_ SoftwareElement**](cim-softwareelement.md) a cui fa riferimento un'associazione [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) per l'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="f96e9-110">Details of the checks are compared with the corresponding details found in a [**CIM\_SoftwareElement**](cim-softwareelement.md) object referenced by a [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object.</span></span> <span data-ttu-id="f96e9-111">Almeno un **CIM \_ SoftwareElement** deve soddisfare i dettagli della condizione affinché il controllo venga soddisfatto.</span><span class="sxs-lookup"><span data-stu-id="f96e9-111">At least one **CIM\_SoftwareElement** needs to satisfy the details of the condition for the check to be satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f96e9-112">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f96e9-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f96e9-113">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f96e9-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f96e9-114">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f96e9-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f96e9-115">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f96e9-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96e9-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f96e9-116">Syntax</span></span>

``` syntax
[UUID("{4D23FBD0-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareElementVersionCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  string  Description;
  string  LowerSoftwareElementVersion;
  string  Name;
  string  SoftwareElementID;
  string  SoftwareElementName;
  uint16  SoftwareElementState;
  uint16  SoftwareElementStateDesired;
  uint16  TargetOperatingSystem;
  uint16  TargetOperatingSystemDesired;
  string  UpperSoftwareElementVersion;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="f96e9-117">Members</span><span class="sxs-lookup"><span data-stu-id="f96e9-117">Members</span></span>

<span data-ttu-id="f96e9-118">La classe **CIM \_ SoftwareElementVersionCheck** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f96e9-118">The **CIM\_SoftwareElementVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="f96e9-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="f96e9-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="f96e9-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f96e9-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f96e9-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="f96e9-121">Methods</span></span>

<span data-ttu-id="f96e9-122">La classe **CIM \_ SoftwareElementVersionCheck** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f96e9-122">The **CIM\_SoftwareElementVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="f96e9-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="f96e9-123">Method</span></span>                                                                   | <span data-ttu-id="f96e9-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f96e9-124">Description</span></span>                                                   |
|:-------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="f96e9-125">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="f96e9-125">**Invoke**</span></span>](invoke-method-in-class-cim-softwareelementversioncheck.md) | <span data-ttu-id="f96e9-126">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="f96e9-126">Takes a particular action.</span></span> <span data-ttu-id="f96e9-127">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f96e9-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f96e9-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f96e9-128">Properties</span></span>

<span data-ttu-id="f96e9-129">La classe **CIM \_ SoftwareElementVersionCheck** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f96e9-129">The **CIM\_SoftwareElementVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f96e9-130">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f96e9-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-133">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f96e9-133">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-134">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f96e9-134">Short textual description of the object.</span></span>

<span data-ttu-id="f96e9-135">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-135">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-136">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="f96e9-136">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-139">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f96e9-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-140">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-140">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="f96e9-141">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-141">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-142">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="f96e9-142">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f96e9-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-145">Se **true**, la condizione dovrebbe esistere nell'ambiente (ad esempio, se un file si trova in un sistema, il metodo [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) deve restituire **true**).</span><span class="sxs-lookup"><span data-stu-id="f96e9-145">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="f96e9-146">Se **false**, la condizione non deve esistere, ad esempio se un file non si trova in un sistema, il metodo **Invoke** deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="f96e9-146">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="f96e9-147">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-147">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-148">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f96e9-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-151">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f96e9-151">Description of the object.</span></span>

<span data-ttu-id="f96e9-152">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-153">**LowerSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="f96e9-153">**LowerSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-156">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versione**")</span><span class="sxs-lookup"><span data-stu-id="f96e9-156">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-157">Versione minima di un elemento software verificato.</span><span class="sxs-lookup"><span data-stu-id="f96e9-157">Minimum version of a software elements being checked.</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f96e9-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-161">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f96e9-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-162">Nome utilizzato per identificare l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f96e9-162">Name used to identify the software element.</span></span>

<span data-ttu-id="f96e9-163">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-163">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-164">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="f96e9-164">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-167">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f96e9-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-168">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f96e9-168">Identifier for the software element.</span></span>

<span data-ttu-id="f96e9-169">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-169">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-170">**SoftwareElementName**</span><span class="sxs-lookup"><span data-stu-id="f96e9-170">**SoftwareElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-173">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="f96e9-173">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-174">Nome dell'elemento software da verificare.</span><span class="sxs-lookup"><span data-stu-id="f96e9-174">Name of the software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-175">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="f96e9-175">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-176">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f96e9-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-178">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f96e9-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-179">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="f96e9-179">State of a software element.</span></span>

<span data-ttu-id="f96e9-180">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-180">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="f96e9-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f96e9-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-182">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-182">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="f96e9-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="f96e9-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-184">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-184">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="f96e9-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="f96e9-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-186">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-186">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f96e9-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="f96e9-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-188">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="f96e9-188">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f96e9-189">**SoftwareElementStateDesired**</span><span class="sxs-lookup"><span data-stu-id="f96e9-189">**SoftwareElementStateDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f96e9-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span><span class="sxs-lookup"><span data-stu-id="f96e9-192">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-193">Stato dell'elemento software da verificare.</span><span class="sxs-lookup"><span data-stu-id="f96e9-193">State of the software element being checked.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="f96e9-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f96e9-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-195">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-195">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="f96e9-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="f96e9-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-197">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-197">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="f96e9-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="f96e9-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-199">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f96e9-199">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f96e9-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="f96e9-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-201">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="f96e9-201">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f96e9-202">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="f96e9-202">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-203">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f96e9-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-205">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="f96e9-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-206">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f96e9-206">Target operating system of the software element.</span></span>

<span data-ttu-id="f96e9-207">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f96e9-207">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f96e9-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f96e9-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f96e9-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f96e9-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="f96e9-210"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="f96e9-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-211">Mac OS</span><span class="sxs-lookup"><span data-stu-id="f96e9-211">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="f96e9-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="f96e9-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-213">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="f96e9-213">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="f96e9-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="f96e9-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="f96e9-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="f96e9-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="f96e9-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="f96e9-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="f96e9-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="f96e9-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-218">Apri VM</span><span class="sxs-lookup"><span data-stu-id="f96e9-218">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="f96e9-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="f96e9-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-220">HP-UX</span><span class="sxs-lookup"><span data-stu-id="f96e9-220">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="f96e9-221"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="f96e9-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="f96e9-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="f96e9-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="f96e9-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="f96e9-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="f96e9-224"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="f96e9-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="f96e9-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="f96e9-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-226">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="f96e9-226">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="f96e9-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="f96e9-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="f96e9-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="f96e9-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-229">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="f96e9-229">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="f96e9-230"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="f96e9-230"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-231">Windows 95</span><span class="sxs-lookup"><span data-stu-id="f96e9-231">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="f96e9-232"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="f96e9-232"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-233">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f96e9-233">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="f96e9-234"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="f96e9-234"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-235">Windows NT</span><span class="sxs-lookup"><span data-stu-id="f96e9-235">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="f96e9-236"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="f96e9-236"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-237">Windows CE</span><span class="sxs-lookup"><span data-stu-id="f96e9-237">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="f96e9-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="f96e9-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-239">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="f96e9-239">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="f96e9-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="f96e9-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="f96e9-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="f96e9-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="f96e9-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="f96e9-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="f96e9-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="f96e9-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="f96e9-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="f96e9-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="f96e9-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="f96e9-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="f96e9-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="f96e9-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="f96e9-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="f96e9-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="f96e9-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="f96e9-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="f96e9-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="f96e9-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="f96e9-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="f96e9-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="f96e9-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="f96e9-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-252">Serie A</span><span class="sxs-lookup"><span data-stu-id="f96e9-252">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="f96e9-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="f96e9-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-254">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="f96e9-254">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="f96e9-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="f96e9-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-256">NT tandem</span><span class="sxs-lookup"><span data-stu-id="f96e9-256">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="f96e9-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="f96e9-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-258">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="f96e9-258">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="f96e9-259"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="f96e9-259"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="f96e9-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="f96e9-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="f96e9-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="f96e9-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="f96e9-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="f96e9-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="f96e9-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="f96e9-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="f96e9-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="f96e9-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-265">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="f96e9-265">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="f96e9-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="f96e9-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="f96e9-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="f96e9-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="f96e9-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="f96e9-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="f96e9-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="f96e9-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-270">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="f96e9-270">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="f96e9-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="f96e9-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="f96e9-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="f96e9-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="f96e9-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="f96e9-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="f96e9-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="f96e9-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="f96e9-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="f96e9-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="f96e9-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="f96e9-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="f96e9-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="f96e9-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="f96e9-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="f96e9-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="f96e9-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="f96e9-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="f96e9-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="f96e9-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="f96e9-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="f96e9-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-282">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="f96e9-282">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="f96e9-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="f96e9-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="f96e9-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="f96e9-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="f96e9-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="f96e9-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="f96e9-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="f96e9-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="f96e9-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="f96e9-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f96e9-288">**TargetOperatingSystemDesired**</span><span class="sxs-lookup"><span data-stu-id="f96e9-288">**TargetOperatingSystemDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-289">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f96e9-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-291">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span><span class="sxs-lookup"><span data-stu-id="f96e9-291">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-292">Sistema operativo di destinazione dell'elemento software da verificare.</span><span class="sxs-lookup"><span data-stu-id="f96e9-292">Target operating system of the software element being checked.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f96e9-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f96e9-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f96e9-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f96e9-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="f96e9-295"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="f96e9-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-296">Mac OS</span><span class="sxs-lookup"><span data-stu-id="f96e9-296">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="f96e9-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="f96e9-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-298">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="f96e9-298">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="f96e9-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="f96e9-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="f96e9-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="f96e9-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="f96e9-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="f96e9-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="f96e9-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="f96e9-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-303">Apri VM</span><span class="sxs-lookup"><span data-stu-id="f96e9-303">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="f96e9-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="f96e9-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-305">HP-UX</span><span class="sxs-lookup"><span data-stu-id="f96e9-305">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="f96e9-306"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="f96e9-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="f96e9-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="f96e9-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="f96e9-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="f96e9-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="f96e9-309"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="f96e9-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="f96e9-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="f96e9-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-311">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="f96e9-311">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="f96e9-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="f96e9-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="f96e9-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="f96e9-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-314">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="f96e9-314">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="f96e9-315"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="f96e9-315"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-316">Windows 95</span><span class="sxs-lookup"><span data-stu-id="f96e9-316">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="f96e9-317"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="f96e9-317"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-318">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f96e9-318">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="f96e9-319"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="f96e9-319"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-320">Windows NT</span><span class="sxs-lookup"><span data-stu-id="f96e9-320">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="f96e9-321"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="f96e9-321"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-322">Windows CE</span><span class="sxs-lookup"><span data-stu-id="f96e9-322">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="f96e9-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="f96e9-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-324">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="f96e9-324">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="f96e9-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="f96e9-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="f96e9-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="f96e9-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="f96e9-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="f96e9-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="f96e9-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="f96e9-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="f96e9-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="f96e9-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="f96e9-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="f96e9-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="f96e9-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="f96e9-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="f96e9-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="f96e9-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="f96e9-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="f96e9-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="f96e9-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="f96e9-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="f96e9-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="f96e9-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="f96e9-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="f96e9-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-337">Serie A</span><span class="sxs-lookup"><span data-stu-id="f96e9-337">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="f96e9-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="f96e9-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-339">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="f96e9-339">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="f96e9-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="f96e9-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-341">NT tandem</span><span class="sxs-lookup"><span data-stu-id="f96e9-341">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="f96e9-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="f96e9-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-343">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="f96e9-343">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="f96e9-344"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="f96e9-344"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="f96e9-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="f96e9-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="f96e9-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="f96e9-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="f96e9-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="f96e9-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="f96e9-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="f96e9-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="f96e9-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="f96e9-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-350">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="f96e9-350">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="f96e9-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="f96e9-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="f96e9-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="f96e9-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="f96e9-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="f96e9-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="f96e9-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="f96e9-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-355">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="f96e9-355">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="f96e9-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="f96e9-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="f96e9-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="f96e9-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="f96e9-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="f96e9-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="f96e9-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="f96e9-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="f96e9-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="f96e9-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="f96e9-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="f96e9-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="f96e9-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="f96e9-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="f96e9-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="f96e9-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="f96e9-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="f96e9-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="f96e9-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="f96e9-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="f96e9-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="f96e9-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="f96e9-367">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="f96e9-367">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="f96e9-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="f96e9-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="f96e9-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="f96e9-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="f96e9-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="f96e9-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="f96e9-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="f96e9-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="f96e9-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="f96e9-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f96e9-373">**UpperSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="f96e9-373">**UpperSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-376">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versione**")</span><span class="sxs-lookup"><span data-stu-id="f96e9-376">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-377">Versione massima di un elemento software verificato.</span><span class="sxs-lookup"><span data-stu-id="f96e9-377">Maximum version of a software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="f96e9-378">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f96e9-378">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f96e9-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f96e9-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f96e9-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f96e9-381">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f96e9-381">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f96e9-382">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f96e9-382">Version of the operation.</span></span>

<span data-ttu-id="f96e9-383">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="f96e9-383">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="f96e9-384"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="f96e9-384"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="f96e9-385"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="f96e9-385"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="f96e9-386">Questa proprietà viene ereditata dalla classe di [**\_ controllo CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="f96e9-386">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f96e9-387">Commenti</span><span class="sxs-lookup"><span data-stu-id="f96e9-387">Remarks</span></span>

<span data-ttu-id="f96e9-388">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f96e9-388">WMI does not implement this class.</span></span>

<span data-ttu-id="f96e9-389">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f96e9-389">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f96e9-390">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f96e9-390">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96e9-391">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f96e9-391">Requirements</span></span>



| <span data-ttu-id="f96e9-392">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96e9-392">Requirement</span></span> | <span data-ttu-id="f96e9-393">Valore</span><span class="sxs-lookup"><span data-stu-id="f96e9-393">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f96e9-394">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f96e9-394">Minimum supported client</span></span><br/> | <span data-ttu-id="f96e9-395">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f96e9-395">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f96e9-396">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f96e9-396">Minimum supported server</span></span><br/> | <span data-ttu-id="f96e9-397">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f96e9-397">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f96e9-398">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f96e9-398">Namespace</span></span><br/>                | <span data-ttu-id="f96e9-399">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f96e9-399">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f96e9-400">MOF</span><span class="sxs-lookup"><span data-stu-id="f96e9-400">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f96e9-401"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f96e9-401"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f96e9-402">DLL</span><span class="sxs-lookup"><span data-stu-id="f96e9-402">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f96e9-403"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f96e9-403"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96e9-404">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f96e9-404">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96e9-405">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="f96e9-405">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

