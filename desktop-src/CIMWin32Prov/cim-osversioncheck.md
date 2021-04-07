---
description: La \_ classe CIM OSVersionCheck specifica le versioni del sistema operativo in grado di supportare un elemento software.
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: Classe CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049206"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="af121-103">CIM \_ OSVersionCheck (classe)</span><span class="sxs-lookup"><span data-stu-id="af121-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="af121-104">La classe **CIM \_ OSVersionCheck** specifica le versioni del sistema operativo in grado di supportare un elemento software.</span><span class="sxs-lookup"><span data-stu-id="af121-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="af121-105">Il controllo può essere eseguito per uno specifico, minimo, massimo o un intervallo di versioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="af121-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="af121-106">Per specificare una versione specifica del sistema operativo, le versioni minime e massime devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="af121-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="af121-107">Per specificare la versione minima, è necessario specificare solo la versione minima.</span><span class="sxs-lookup"><span data-stu-id="af121-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="af121-108">Per specificare una versione massima, è necessario specificare solo la versione massima.</span><span class="sxs-lookup"><span data-stu-id="af121-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="af121-109">Per specificare un intervallo, è necessario specificare sia le versioni minime che quelle massime.</span><span class="sxs-lookup"><span data-stu-id="af121-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="af121-110">Il tipo di sistema operativo è specificato nella proprietà **TargetOperatingSystem** dell'elemento software proprietario.</span><span class="sxs-lookup"><span data-stu-id="af121-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="af121-111">I dettagli dei controlli vengono confrontati con i dettagli corrispondenti presenti in un oggetto [**CIM \_ OperatingSystem**](cim-operatingsystem.md) a cui fa riferimento un'associazione [**CIM \_ Installatoos**](cim-installedos.md) per l'oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) che descrive l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="af121-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="af121-112">Almeno una classe **CIM \_ OperatingSystem** deve soddisfare i dettagli della condizione affinché il controllo venga soddisfatto.</span><span class="sxs-lookup"><span data-stu-id="af121-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="af121-113">In altre parole, non tutti i sistemi operativi nel computer pertinente devono soddisfare la condizione.</span><span class="sxs-lookup"><span data-stu-id="af121-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="af121-114">Inoltre, la proprietà **OSType** della classe **CIM \_ OperatingSystem** deve corrispondere al tipo della proprietà **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="af121-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af121-115">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="af121-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="af121-116">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="af121-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="af121-117">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="af121-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="af121-118">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="af121-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af121-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af121-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
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
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="af121-120">Members</span><span class="sxs-lookup"><span data-stu-id="af121-120">Members</span></span>

<span data-ttu-id="af121-121">La classe **CIM \_ OSVersionCheck** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af121-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="af121-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="af121-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="af121-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af121-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="af121-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="af121-124">Methods</span></span>

<span data-ttu-id="af121-125">La classe **CIM \_ OSVersionCheck** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="af121-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="af121-126">Metodo</span><span class="sxs-lookup"><span data-stu-id="af121-126">Method</span></span>                                                      | <span data-ttu-id="af121-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af121-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="af121-128">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="af121-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="af121-129">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="af121-129">Takes a particular action.</span></span> <span data-ttu-id="af121-130">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="af121-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="af121-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af121-131">Properties</span></span>

<span data-ttu-id="af121-132">La classe **CIM \_ OSVersionCheck** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af121-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af121-133">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="af121-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-136">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af121-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af121-137">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af121-137">A short textual description of the subject.</span></span>

<span data-ttu-id="af121-138">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="af121-139">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="af121-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-142">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="af121-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="af121-143">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="af121-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="af121-144">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="af121-145">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="af121-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af121-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af121-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af121-148">Se **true**, la condizione dovrebbe esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="af121-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="af121-149">Un file, ad esempio, dovrebbe trovarsi in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="af121-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="af121-150">Se **false**, la condizione non è prevista.</span><span class="sxs-lookup"><span data-stu-id="af121-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="af121-151">Un file, ad esempio, non si trova in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="af121-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="af121-152">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="af121-153">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="af121-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af121-156">Descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="af121-156">A description of the objects.</span></span>

<span data-ttu-id="af121-157">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="af121-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="af121-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-161">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Versione**")</span><span class="sxs-lookup"><span data-stu-id="af121-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="af121-162">Versione massima del sistema operativo richiesto.</span><span class="sxs-lookup"><span data-stu-id="af121-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="af121-163">Il valore viene codificato in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="af121-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="af121-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="af121-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="af121-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="af121-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="af121-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="af121-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-169">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Versione**")</span><span class="sxs-lookup"><span data-stu-id="af121-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="af121-170">Versione minima del sistema operativo richiesto.</span><span class="sxs-lookup"><span data-stu-id="af121-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="af121-171">Il valore viene codificato in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="af121-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="af121-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="af121-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="af121-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="af121-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="af121-174">**Nome**</span><span class="sxs-lookup"><span data-stu-id="af121-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-177">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="af121-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="af121-178">Nome usato per identificare l'elemento software</span><span class="sxs-lookup"><span data-stu-id="af121-178">Name used to identify the software element</span></span>

<span data-ttu-id="af121-179">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="af121-180">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="af121-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-183">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="af121-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="af121-184">Si tratta di un identificatore per questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="af121-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="af121-185">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="af121-186">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="af121-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af121-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af121-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-189">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af121-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af121-190">Stato dell'elemento software di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="af121-190">The software element state of a software element.</span></span>

<span data-ttu-id="af121-191">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="af121-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="af121-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="af121-193">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="af121-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="af121-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="af121-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="af121-195">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="af121-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="af121-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="af121-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af121-197">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="af121-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="af121-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="af121-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af121-199">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="af121-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af121-200">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="af121-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-201">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af121-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af121-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-203">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="af121-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="af121-204">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="af121-204">Target operating system of the software element.</span></span>

<span data-ttu-id="af121-205">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af121-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af121-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af121-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af121-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="af121-208"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="af121-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af121-209">Mac OS</span><span class="sxs-lookup"><span data-stu-id="af121-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="af121-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="af121-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af121-211">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="af121-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="af121-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="af121-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="af121-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="af121-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="af121-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="af121-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="af121-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="af121-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="af121-216">Apri VM</span><span class="sxs-lookup"><span data-stu-id="af121-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="af121-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="af121-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="af121-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="af121-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="af121-219"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="af121-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="af121-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="af121-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="af121-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="af121-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="af121-222"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="af121-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="af121-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="af121-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="af121-224">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="af121-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="af121-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="af121-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="af121-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="af121-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="af121-227">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="af121-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="af121-228"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="af121-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="af121-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="af121-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="af121-230"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="af121-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="af121-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="af121-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="af121-232"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="af121-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="af121-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="af121-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="af121-234"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="af121-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="af121-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="af121-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="af121-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="af121-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="af121-237">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="af121-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="af121-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="af121-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="af121-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="af121-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="af121-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="af121-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="af121-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="af121-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="af121-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="af121-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="af121-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="af121-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="af121-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="af121-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="af121-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="af121-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="af121-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="af121-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="af121-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="af121-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="af121-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="af121-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="af121-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="af121-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="af121-250">Serie A</span><span class="sxs-lookup"><span data-stu-id="af121-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="af121-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="af121-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="af121-252">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="af121-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="af121-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="af121-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="af121-254">NT tandem</span><span class="sxs-lookup"><span data-stu-id="af121-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="af121-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="af121-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="af121-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="af121-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="af121-257"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="af121-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="af121-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="af121-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="af121-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="af121-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="af121-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="af121-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="af121-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="af121-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="af121-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="af121-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="af121-263">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="af121-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="af121-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="af121-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="af121-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="af121-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="af121-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="af121-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="af121-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="af121-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="af121-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="af121-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="af121-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="af121-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="af121-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="af121-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="af121-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="af121-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="af121-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="af121-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="af121-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="af121-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="af121-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="af121-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="af121-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="af121-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="af121-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="af121-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="af121-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="af121-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="af121-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="af121-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="af121-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="af121-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="af121-280">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="af121-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="af121-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="af121-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="af121-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="af121-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="af121-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="af121-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="af121-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="af121-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="af121-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="af121-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af121-286">**Versione**</span><span class="sxs-lookup"><span data-stu-id="af121-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af121-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af121-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af121-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af121-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af121-289">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="af121-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="af121-290">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="af121-290">Version of the operation.</span></span>

<span data-ttu-id="af121-291">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="af121-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="af121-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="af121-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="af121-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="af121-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="af121-294">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="af121-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af121-295">Commenti</span><span class="sxs-lookup"><span data-stu-id="af121-295">Remarks</span></span>

<span data-ttu-id="af121-296">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="af121-296">WMI does not implement this class.</span></span>

<span data-ttu-id="af121-297">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="af121-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="af121-298">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="af121-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="af121-299">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af121-299">Requirements</span></span>



| <span data-ttu-id="af121-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="af121-300">Requirement</span></span> | <span data-ttu-id="af121-301">Valore</span><span class="sxs-lookup"><span data-stu-id="af121-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af121-302">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af121-302">Minimum supported client</span></span><br/> | <span data-ttu-id="af121-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af121-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af121-304">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af121-304">Minimum supported server</span></span><br/> | <span data-ttu-id="af121-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af121-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af121-306">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af121-306">Namespace</span></span><br/>                | <span data-ttu-id="af121-307">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="af121-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af121-308">MOF</span><span class="sxs-lookup"><span data-stu-id="af121-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af121-309"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af121-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af121-310">DLL</span><span class="sxs-lookup"><span data-stu-id="af121-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af121-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af121-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af121-312">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af121-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af121-313">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="af121-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

