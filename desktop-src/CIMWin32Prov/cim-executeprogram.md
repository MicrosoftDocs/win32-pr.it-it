---
description: La \_ classe CIM ExecuteProgram rappresenta i file che possono essere eseguiti nel sistema in cui è installato l'elemento software.
ms.assetid: 4329d228-4069-4a5a-b1eb-2dbad9644118
ms.tgt_platform: multiple
title: Classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram
- CIM_ExecuteProgram.ActionID
- CIM_ExecuteProgram.Caption
- CIM_ExecuteProgram.Description
- CIM_ExecuteProgram.Direction
- CIM_ExecuteProgram.Name
- CIM_ExecuteProgram.SoftwareElementID
- CIM_ExecuteProgram.SoftwareElementState
- CIM_ExecuteProgram.TargetOperatingSystem
- CIM_ExecuteProgram.Version
- CIM_ExecuteProgram.CommandLine
- CIM_ExecuteProgram.ProgramPath
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76743d255bc50d213a4ce3f44057d97830078ccd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126986"
---
# <a name="cim_executeprogram-class"></a><span data-ttu-id="ba23b-103">CIM \_ ExecuteProgram (classe)</span><span class="sxs-lookup"><span data-stu-id="ba23b-103">CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="ba23b-104">La classe **CIM \_ ExecuteProgram** rappresenta i file che possono essere eseguiti nel sistema in cui è installato l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ba23b-104">The **CIM\_ExecuteProgram** class represents files that can be executed on the system where the software element is installed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba23b-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ba23b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ba23b-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ba23b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ba23b-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ba23b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ba23b-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ba23b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba23b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba23b-109">Syntax</span></span>

``` syntax
[UUID("{149ADDEE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ExecuteProgram : CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
  string CommandLine;
  string ProgramPath;
};
```

## <a name="members"></a><span data-ttu-id="ba23b-110">Members</span><span class="sxs-lookup"><span data-stu-id="ba23b-110">Members</span></span>

<span data-ttu-id="ba23b-111">La classe **CIM \_ ExecuteProgram** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba23b-111">The **CIM\_ExecuteProgram** class has these types of members:</span></span>

-   [<span data-ttu-id="ba23b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ba23b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ba23b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba23b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ba23b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="ba23b-114">Methods</span></span>

<span data-ttu-id="ba23b-115">La classe **CIM \_ ExecuteProgram** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ba23b-115">The **CIM\_ExecuteProgram** class has these methods.</span></span>



| <span data-ttu-id="ba23b-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="ba23b-116">Method</span></span>                                                      | <span data-ttu-id="ba23b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba23b-117">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="ba23b-118">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="ba23b-118">**Invoke**</span></span>](invoke-method-in-class-cim-executeprogram.md) | <span data-ttu-id="ba23b-119">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="ba23b-119">Takes a particular action.</span></span> <span data-ttu-id="ba23b-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ba23b-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ba23b-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba23b-121">Properties</span></span>

<span data-ttu-id="ba23b-122">La classe **CIM \_ ExecuteProgram** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba23b-122">The **CIM\_ExecuteProgram** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba23b-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="ba23b-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-126">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba23b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-127">Identificatore univoco assegnato a una determinata azione per un elemento software.</span><span class="sxs-lookup"><span data-stu-id="ba23b-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="ba23b-128">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-129">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ba23b-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-132">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ba23b-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-133">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba23b-133">Short textual description of the object.</span></span>

<span data-ttu-id="ba23b-134">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-135">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="ba23b-135">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-138">Stringa che può essere richiamata in una riga di comando di sistema.</span><span class="sxs-lookup"><span data-stu-id="ba23b-138">String that can be invoked on a system command line.</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ba23b-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-142">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba23b-142">Description of the object.</span></span>

<span data-ttu-id="ba23b-143">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-143">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-144">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="ba23b-144">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba23b-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-147">Indica se un particolare [**oggetto \_ azione CIM**](cim-action.md) fa parte di una sequenza di azioni per la transizione dell'elemento software corrente allo stato successivo, ad esempio "Install", o per rimuovere l'elemento software corrente, ad esempio "uninstall".</span><span class="sxs-lookup"><span data-stu-id="ba23b-147">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="ba23b-148">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="ba23b-149">**Installazione** (0)</span><span class="sxs-lookup"><span data-stu-id="ba23b-149">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="ba23b-150">**Disinstalla** (1)</span><span class="sxs-lookup"><span data-stu-id="ba23b-150">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ba23b-151">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ba23b-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-154">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba23b-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-155">Identifica l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ba23b-155">Identifies the software element.</span></span>

<span data-ttu-id="ba23b-156">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-156">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-157">**ProgramPath**</span><span class="sxs-lookup"><span data-stu-id="ba23b-157">**ProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-160">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="ba23b-160">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-161">Percorso del programma.</span><span class="sxs-lookup"><span data-stu-id="ba23b-161">Path to the program.</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-162">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ba23b-162">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-165">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba23b-165">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-166">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ba23b-166">Identifier for the software element.</span></span>

<span data-ttu-id="ba23b-167">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-167">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba23b-168">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ba23b-168">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-169">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba23b-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-171">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba23b-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-172">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="ba23b-172">State of a software element.</span></span>

<span data-ttu-id="ba23b-173">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-173">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ba23b-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="ba23b-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-175">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ba23b-175">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ba23b-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="ba23b-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-177">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ba23b-177">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ba23b-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="ba23b-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-179">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ba23b-179">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ba23b-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="ba23b-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-181">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="ba23b-181">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba23b-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ba23b-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba23b-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-185">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="ba23b-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-186">Sistema operativo di destinazione dell'elemento software proprietario.</span><span class="sxs-lookup"><span data-stu-id="ba23b-186">Target operating system of the owning software element.</span></span>

<span data-ttu-id="ba23b-187">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-187">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba23b-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ba23b-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ba23b-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ba23b-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ba23b-190"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ba23b-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ba23b-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ba23b-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="ba23b-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ba23b-193"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="ba23b-193"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ba23b-194"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="ba23b-194"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ba23b-195"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="ba23b-195"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ba23b-196"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ba23b-196"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-197">Apri VM</span><span class="sxs-lookup"><span data-stu-id="ba23b-197">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ba23b-198"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="ba23b-198"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-199">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ba23b-199">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ba23b-200"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="ba23b-200"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ba23b-201"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ba23b-201"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ba23b-202"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ba23b-202"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ba23b-203"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ba23b-203"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ba23b-204"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="ba23b-204"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-205">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="ba23b-205">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ba23b-206"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="ba23b-206"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ba23b-207"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ba23b-207"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-208">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ba23b-208">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ba23b-209"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ba23b-209"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-210">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ba23b-210">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ba23b-211"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ba23b-211"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-212">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ba23b-212">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ba23b-213"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="ba23b-213"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-214">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ba23b-214">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ba23b-215"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ba23b-215"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-216">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ba23b-216">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ba23b-217"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ba23b-217"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-218">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ba23b-218">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ba23b-219"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ba23b-219"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ba23b-220"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="ba23b-220"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ba23b-221"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="ba23b-221"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ba23b-222"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="ba23b-222"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ba23b-223"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ba23b-223"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ba23b-224"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ba23b-224"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ba23b-225"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="ba23b-225"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ba23b-226"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ba23b-226"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ba23b-227"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ba23b-227"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ba23b-228"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="ba23b-228"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ba23b-229"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ba23b-229"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ba23b-230"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="ba23b-230"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-231">Serie A</span><span class="sxs-lookup"><span data-stu-id="ba23b-231">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ba23b-232"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="ba23b-232"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-233">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="ba23b-233">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ba23b-234"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="ba23b-234"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-235">NT tandem</span><span class="sxs-lookup"><span data-stu-id="ba23b-235">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ba23b-236"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ba23b-236"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-237">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ba23b-237">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ba23b-238"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ba23b-238"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ba23b-239"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ba23b-239"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ba23b-240"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="ba23b-240"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ba23b-241"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="ba23b-241"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ba23b-242"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="ba23b-242"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ba23b-243"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="ba23b-243"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-244">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="ba23b-244">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ba23b-245"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ba23b-245"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ba23b-246"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ba23b-246"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ba23b-247"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ba23b-247"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ba23b-248"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ba23b-248"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-249">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ba23b-249">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ba23b-250"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="ba23b-250"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ba23b-251"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ba23b-251"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ba23b-252"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ba23b-252"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ba23b-253"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ba23b-253"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ba23b-254"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="ba23b-254"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ba23b-255"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ba23b-255"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ba23b-256"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="ba23b-256"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ba23b-257"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ba23b-257"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-258">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ba23b-258">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ba23b-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="ba23b-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ba23b-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="ba23b-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ba23b-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ba23b-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ba23b-262">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="ba23b-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ba23b-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ba23b-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ba23b-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ba23b-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ba23b-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="ba23b-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ba23b-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ba23b-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ba23b-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ba23b-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ba23b-268">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ba23b-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba23b-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba23b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba23b-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba23b-271">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="ba23b-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ba23b-272">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ba23b-272">Version of the operation.</span></span>

<span data-ttu-id="ba23b-273">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="ba23b-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ba23b-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="ba23b-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="ba23b-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="ba23b-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="ba23b-276">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ba23b-276">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba23b-277">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba23b-277">Remarks</span></span>

<span data-ttu-id="ba23b-278">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ba23b-278">WMI does not implement this class.</span></span>

<span data-ttu-id="ba23b-279">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ba23b-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ba23b-280">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ba23b-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba23b-281">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba23b-281">Requirements</span></span>



| <span data-ttu-id="ba23b-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba23b-282">Requirement</span></span> | <span data-ttu-id="ba23b-283">Valore</span><span class="sxs-lookup"><span data-stu-id="ba23b-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba23b-284">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba23b-284">Minimum supported client</span></span><br/> | <span data-ttu-id="ba23b-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba23b-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba23b-286">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba23b-286">Minimum supported server</span></span><br/> | <span data-ttu-id="ba23b-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba23b-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba23b-288">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba23b-288">Namespace</span></span><br/>                | <span data-ttu-id="ba23b-289">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ba23b-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba23b-290">MOF</span><span class="sxs-lookup"><span data-stu-id="ba23b-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba23b-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba23b-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba23b-292">DLL</span><span class="sxs-lookup"><span data-stu-id="ba23b-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba23b-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba23b-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba23b-294">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba23b-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba23b-295">**\_Azione CIM**</span><span class="sxs-lookup"><span data-stu-id="ba23b-295">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

