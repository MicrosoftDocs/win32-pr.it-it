---
description: La \_ classe CIM CopyFileAction rappresenta lo spostamento o la copia di file da un sistema di computer in una nuova posizione.
ms.assetid: c80b5002-d489-4b7e-b9a2-4460c3596958
ms.tgt_platform: multiple
title: Classe CIM_CopyFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction
- CIM_CopyFileAction.ActionID
- CIM_CopyFileAction.Caption
- CIM_CopyFileAction.Description
- CIM_CopyFileAction.Direction
- CIM_CopyFileAction.Name
- CIM_CopyFileAction.SoftwareElementID
- CIM_CopyFileAction.SoftwareElementState
- CIM_CopyFileAction.TargetOperatingSystem
- CIM_CopyFileAction.Version
- CIM_CopyFileAction.DeleteAfterCopy
- CIM_CopyFileAction.Destination
- CIM_CopyFileAction.Source
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0303f4696d1baa5129d93cd2e6a7703be611ed9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304924"
---
# <a name="cim_copyfileaction-class"></a><span data-ttu-id="065de-103">CIM \_ CopyFileAction (classe)</span><span class="sxs-lookup"><span data-stu-id="065de-103">CIM\_CopyFileAction class</span></span>

<span data-ttu-id="065de-104">La classe **CIM \_ CopyFileAction** rappresenta lo spostamento o la copia di file da un sistema di computer in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="065de-104">The **CIM\_CopyFileAction** class represents moving or copying files from a computer system to a new location.</span></span>

<span data-ttu-id="065de-105">Le informazioni sulla posizione per la copia vengono specificate tramite le associazioni CIM [**\_ ToDirectorySpecification**](cim-todirectoryspecification.md) e [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) oppure le associazioni CIM [**\_ ToDirectoryAction**](cim-todirectoryaction.md) e [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="065de-105">Location information for copying is specified by using either the [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) and [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) associations, or the [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) and [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) associations.</span></span> <span data-ttu-id="065de-106">Il primo set viene usato quando l'origine o la destinazione devono esistere prima di intraprendere qualsiasi azione.</span><span class="sxs-lookup"><span data-stu-id="065de-106">The first set is used when the source or target are to exist before any actions are taken.</span></span> <span data-ttu-id="065de-107">Il secondo set viene usato quando l'origine o la destinazione vengono create come parte di un'azione precedente.</span><span class="sxs-lookup"><span data-stu-id="065de-107">The second set is used when the source or target are created as a part of a previous action.</span></span> <span data-ttu-id="065de-108">Nel secondo caso, l'azione per creare la directory deve essere eseguita prima dell'oggetto **CIM \_ CopyFileAction** .</span><span class="sxs-lookup"><span data-stu-id="065de-108">In the latter case, the action to create the directory must occur prior to the **CIM\_CopyFileAction** object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="065de-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="065de-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="065de-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="065de-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="065de-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="065de-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="065de-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="065de-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="065de-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="065de-113">Syntax</span></span>

``` syntax
[UUID("{73553260-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CopyFileAction : CIM_FileAction
{
  string  ActionID;
  string  Caption;
  string  Description;
  uint16  Direction;
  string  Name;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
  boolean DeleteAfterCopy;
  string  Destination;
  string  Source;
};
```

## <a name="members"></a><span data-ttu-id="065de-114">Members</span><span class="sxs-lookup"><span data-stu-id="065de-114">Members</span></span>

<span data-ttu-id="065de-115">La classe **CIM \_ CopyFileAction** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="065de-115">The **CIM\_CopyFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="065de-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="065de-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="065de-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="065de-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="065de-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="065de-118">Methods</span></span>

<span data-ttu-id="065de-119">La classe **CIM \_ CopyFileAction** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="065de-119">The **CIM\_CopyFileAction** class has these methods.</span></span>



| <span data-ttu-id="065de-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="065de-120">Method</span></span>                                                      | <span data-ttu-id="065de-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="065de-121">Description</span></span>                                                                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065de-122">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="065de-122">**Invoke**</span></span>](invoke-method-in-class-cim-copyfileaction.md) | <span data-ttu-id="065de-123">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="065de-123">Takes a particular action.</span></span> <span data-ttu-id="065de-124">I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="065de-124">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="065de-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="065de-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="065de-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="065de-126">Properties</span></span>

<span data-ttu-id="065de-127">La classe **CIM \_ CopyFileAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="065de-127">The **CIM\_CopyFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="065de-128">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="065de-128">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-131">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="065de-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="065de-132">Identificatore univoco assegnato a una determinata azione per un elemento software.</span><span class="sxs-lookup"><span data-stu-id="065de-132">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="065de-133">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-133">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="065de-134">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="065de-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-137">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="065de-137">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="065de-138">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="065de-138">Short textual description of the object.</span></span>

<span data-ttu-id="065de-139">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="065de-140">**DeleteAfterCopy**</span><span class="sxs-lookup"><span data-stu-id="065de-140">**DeleteAfterCopy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-141">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="065de-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="065de-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065de-143">Se **true**, il file di origine viene eliminato dopo l'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="065de-143">If **TRUE**, the source file is deleted after the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="065de-144">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="065de-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065de-147">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="065de-147">Description of the object.</span></span>

<span data-ttu-id="065de-148">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="065de-149">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="065de-149">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-152">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="065de-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="065de-153">Nome completo del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="065de-153">Fully qualified destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="065de-154">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="065de-154">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="065de-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="065de-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065de-157">Indica se un particolare [**oggetto \_ azione CIM**](cim-action.md) fa parte di una sequenza di azioni per la transizione dell'elemento software corrente allo stato successivo, ad esempio "Install", o per rimuovere l'elemento software corrente, ad esempio "uninstall".</span><span class="sxs-lookup"><span data-stu-id="065de-157">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="065de-158">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-158">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="065de-159">**Installazione** (0)</span><span class="sxs-lookup"><span data-stu-id="065de-159">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="065de-160">**Disinstalla** (1)</span><span class="sxs-lookup"><span data-stu-id="065de-160">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="065de-161">**Nome**</span><span class="sxs-lookup"><span data-stu-id="065de-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-164">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="065de-164">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="065de-165">Identifica l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="065de-165">Identifies the software element.</span></span>

<span data-ttu-id="065de-166">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-166">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="065de-167">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="065de-167">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-170">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="065de-170">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="065de-171">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="065de-171">Identifier for the software element.</span></span>

<span data-ttu-id="065de-172">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-172">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="065de-173">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="065de-173">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-174">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="065de-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="065de-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-176">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="065de-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="065de-177">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="065de-177">State of a software element.</span></span>

<span data-ttu-id="065de-178">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-178">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="065de-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="065de-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="065de-180">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="065de-180">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="065de-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="065de-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="065de-182">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="065de-182">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="065de-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="065de-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="065de-184">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="065de-184">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="065de-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="065de-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="065de-186">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="065de-186">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="065de-187">**Origine**</span><span class="sxs-lookup"><span data-stu-id="065de-187">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-190">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="065de-190">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="065de-191">Nome completo del file di origine.</span><span class="sxs-lookup"><span data-stu-id="065de-191">Fully qualified source file name.</span></span>

</dd> <dt>

<span data-ttu-id="065de-192">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="065de-192">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="065de-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="065de-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-195">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="065de-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="065de-196">Sistema operativo di destinazione dell'elemento software proprietario.</span><span class="sxs-lookup"><span data-stu-id="065de-196">Target operating system of the owning software element.</span></span>

<span data-ttu-id="065de-197">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-197">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="065de-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="065de-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="065de-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="065de-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="065de-200"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="065de-200"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="065de-201">Mac OS</span><span class="sxs-lookup"><span data-stu-id="065de-201">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="065de-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="065de-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="065de-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="065de-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="065de-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="065de-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="065de-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="065de-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="065de-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="065de-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="065de-207">Apri VM</span><span class="sxs-lookup"><span data-stu-id="065de-207">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="065de-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="065de-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="065de-209">HP-UX</span><span class="sxs-lookup"><span data-stu-id="065de-209">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="065de-210"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="065de-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="065de-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="065de-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="065de-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="065de-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="065de-213"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="065de-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="065de-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="065de-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="065de-215">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="065de-215">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="065de-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="065de-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="065de-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="065de-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="065de-218">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="065de-218">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="065de-219"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="065de-219"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="065de-220">Windows 95</span><span class="sxs-lookup"><span data-stu-id="065de-220">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="065de-221"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="065de-221"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="065de-222">Windows 98</span><span class="sxs-lookup"><span data-stu-id="065de-222">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="065de-223"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="065de-223"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="065de-224">Windows NT</span><span class="sxs-lookup"><span data-stu-id="065de-224">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="065de-225"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="065de-225"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="065de-226">Windows CE</span><span class="sxs-lookup"><span data-stu-id="065de-226">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="065de-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="065de-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="065de-228">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="065de-228">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="065de-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="065de-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="065de-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="065de-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="065de-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="065de-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="065de-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="065de-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="065de-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="065de-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="065de-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="065de-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="065de-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="065de-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="065de-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="065de-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="065de-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="065de-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="065de-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="065de-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="065de-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="065de-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="065de-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="065de-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="065de-241">Serie A</span><span class="sxs-lookup"><span data-stu-id="065de-241">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="065de-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="065de-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="065de-243">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="065de-243">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="065de-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="065de-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="065de-245">NT tandem</span><span class="sxs-lookup"><span data-stu-id="065de-245">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="065de-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="065de-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="065de-247">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="065de-247">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="065de-248"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="065de-248"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="065de-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="065de-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="065de-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="065de-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="065de-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="065de-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="065de-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="065de-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="065de-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="065de-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="065de-254">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="065de-254">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="065de-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="065de-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="065de-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="065de-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="065de-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="065de-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="065de-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="065de-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="065de-259">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="065de-259">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="065de-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="065de-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="065de-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="065de-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="065de-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="065de-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="065de-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="065de-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="065de-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="065de-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="065de-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="065de-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="065de-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="065de-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="065de-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="065de-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="065de-268">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="065de-268">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="065de-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="065de-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="065de-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="065de-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="065de-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="065de-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="065de-272">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="065de-272">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="065de-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="065de-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="065de-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="065de-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="065de-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="065de-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="065de-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="065de-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="065de-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="065de-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="065de-278">**Versione**</span><span class="sxs-lookup"><span data-stu-id="065de-278">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065de-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="065de-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065de-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="065de-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="065de-281">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="065de-281">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="065de-282">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="065de-282">Version of the operation.</span></span>

<span data-ttu-id="065de-283">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="065de-283">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="065de-284"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="065de-284"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="065de-285"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="065de-285"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="065de-286">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="065de-286">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="065de-287">Commenti</span><span class="sxs-lookup"><span data-stu-id="065de-287">Remarks</span></span>

<span data-ttu-id="065de-288">La classe **CIM \_ CopyFileAction** è derivata da [**\_ fileaction CIM**](cim-fileaction.md).</span><span class="sxs-lookup"><span data-stu-id="065de-288">The **CIM\_CopyFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="065de-289">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="065de-289">WMI does not implement this class.</span></span> <span data-ttu-id="065de-290">Per ulteriori informazioni sulle classi derivate da **CIM \_ CopyFileAction**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="065de-290">For more information about classes derived from **CIM\_CopyFileAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="065de-291">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="065de-291">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="065de-292">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="065de-292">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="065de-293">Requisiti</span><span class="sxs-lookup"><span data-stu-id="065de-293">Requirements</span></span>



| <span data-ttu-id="065de-294">Requisito</span><span class="sxs-lookup"><span data-stu-id="065de-294">Requirement</span></span> | <span data-ttu-id="065de-295">Valore</span><span class="sxs-lookup"><span data-stu-id="065de-295">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="065de-296">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="065de-296">Minimum supported client</span></span><br/> | <span data-ttu-id="065de-297">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="065de-297">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="065de-298">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="065de-298">Minimum supported server</span></span><br/> | <span data-ttu-id="065de-299">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="065de-299">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="065de-300">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="065de-300">Namespace</span></span><br/>                | <span data-ttu-id="065de-301">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="065de-301">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="065de-302">MOF</span><span class="sxs-lookup"><span data-stu-id="065de-302">MOF</span></span><br/>                      | <dl> <span data-ttu-id="065de-303"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="065de-303"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="065de-304">DLL</span><span class="sxs-lookup"><span data-stu-id="065de-304">DLL</span></span><br/>                      | <dl> <span data-ttu-id="065de-305"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="065de-305"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065de-306">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="065de-306">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065de-307">**Azione filecim \_**</span><span class="sxs-lookup"><span data-stu-id="065de-307">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

