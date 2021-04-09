---
description: La \_ classe CIM RemoveDirectoryAction rimuove le directory per gli elementi software.
ms.assetid: e403baa8-3704-42a6-970a-8159e7cd72a7
ms.tgt_platform: multiple
title: Classe CIM_RemoveDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveDirectoryAction
- CIM_RemoveDirectoryAction.ActionID
- CIM_RemoveDirectoryAction.Caption
- CIM_RemoveDirectoryAction.Description
- CIM_RemoveDirectoryAction.Direction
- CIM_RemoveDirectoryAction.Name
- CIM_RemoveDirectoryAction.SoftwareElementID
- CIM_RemoveDirectoryAction.SoftwareElementState
- CIM_RemoveDirectoryAction.TargetOperatingSystem
- CIM_RemoveDirectoryAction.Version
- CIM_RemoveDirectoryAction.DirectoryName
- CIM_RemoveDirectoryAction.MustBeEmpty
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5960c0f72bdea28bd431c11d23ccffa0ea19ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965997"
---
# <a name="cim_removedirectoryaction-class"></a><span data-ttu-id="990a8-103">CIM \_ RemoveDirectoryAction (classe)</span><span class="sxs-lookup"><span data-stu-id="990a8-103">CIM\_RemoveDirectoryAction class</span></span>

<span data-ttu-id="990a8-104">La classe **CIM \_ RemoveDirectoryAction** rimuove le directory per gli elementi software.</span><span class="sxs-lookup"><span data-stu-id="990a8-104">The **CIM\_RemoveDirectoryAction** class removes directories for software elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="990a8-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="990a8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="990a8-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="990a8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="990a8-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="990a8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="990a8-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="990a8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="990a8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="990a8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B272D2EA-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RemoveDirectoryAction : CIM_DirectoryAction
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
  string  DirectoryName;
  boolean MustBeEmpty;
};
```

## <a name="members"></a><span data-ttu-id="990a8-110">Members</span><span class="sxs-lookup"><span data-stu-id="990a8-110">Members</span></span>

<span data-ttu-id="990a8-111">La classe **CIM \_ RemoveDirectoryAction** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="990a8-111">The **CIM\_RemoveDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="990a8-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="990a8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="990a8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="990a8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="990a8-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="990a8-114">Methods</span></span>

<span data-ttu-id="990a8-115">La classe **CIM \_ RemoveDirectoryAction** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="990a8-115">The **CIM\_RemoveDirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="990a8-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="990a8-116">Method</span></span>                                                             | <span data-ttu-id="990a8-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="990a8-117">Description</span></span>                                                   |
|:-------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="990a8-118">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="990a8-118">**Invoke**</span></span>](invoke-method-in-class-cim-removedirectoryaction.md) | <span data-ttu-id="990a8-119">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="990a8-119">Takes a particular action.</span></span> <span data-ttu-id="990a8-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="990a8-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="990a8-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="990a8-121">Properties</span></span>

<span data-ttu-id="990a8-122">La classe **CIM \_ RemoveDirectoryAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="990a8-122">The **CIM\_RemoveDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="990a8-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="990a8-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-126">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="990a8-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="990a8-127">Identificatore univoco assegnato a una determinata azione per un elemento software.</span><span class="sxs-lookup"><span data-stu-id="990a8-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="990a8-128">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="990a8-129">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="990a8-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-132">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="990a8-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="990a8-133">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="990a8-133">Short textual description of the object.</span></span>

<span data-ttu-id="990a8-134">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="990a8-135">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="990a8-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="990a8-138">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="990a8-138">Description of the object.</span></span>

<span data-ttu-id="990a8-139">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="990a8-140">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="990a8-140">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="990a8-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="990a8-143">Indica se un particolare [**oggetto \_ azione CIM**](cim-action.md) fa parte di una sequenza di azioni per la transizione dell'elemento software corrente allo stato successivo, ad esempio "Install", o per rimuovere l'elemento software corrente, ad esempio "uninstall".</span><span class="sxs-lookup"><span data-stu-id="990a8-143">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="990a8-144">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-144">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="990a8-145">**Installazione** (0)</span><span class="sxs-lookup"><span data-stu-id="990a8-145">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="990a8-146">**Disinstalla** (1)</span><span class="sxs-lookup"><span data-stu-id="990a8-146">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="990a8-147">**DirectoryName**</span><span class="sxs-lookup"><span data-stu-id="990a8-147">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-150">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="990a8-150">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="990a8-151">Nome della directory a cui si applica l'azione.</span><span class="sxs-lookup"><span data-stu-id="990a8-151">Name of the directory to which the action applies.</span></span>

<span data-ttu-id="990a8-152">Questa proprietà viene ereditata da [**CIM \_ DirectoryAction**](cim-directoryaction.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-152">This property is inherited from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

</dd> <dt>

<span data-ttu-id="990a8-153">**MustBeEmpty**</span><span class="sxs-lookup"><span data-stu-id="990a8-153">**MustBeEmpty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-154">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="990a8-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="990a8-156">Se **true**, la directory deve essere vuota per essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="990a8-156">If **TRUE**, the directory must be empty to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="990a8-157">**Nome**</span><span class="sxs-lookup"><span data-stu-id="990a8-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-160">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="990a8-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="990a8-161">Identifica l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="990a8-161">Identifies the software element.</span></span>

<span data-ttu-id="990a8-162">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-162">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="990a8-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="990a8-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-166">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="990a8-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="990a8-167">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="990a8-167">Identifier for the software element.</span></span>

<span data-ttu-id="990a8-168">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-168">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="990a8-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="990a8-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-170">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="990a8-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-172">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="990a8-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="990a8-173">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="990a8-173">State of a software element.</span></span>

<span data-ttu-id="990a8-174">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-174">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="990a8-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="990a8-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-176">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="990a8-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="990a8-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="990a8-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-178">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="990a8-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="990a8-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="990a8-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-180">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="990a8-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="990a8-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="990a8-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-182">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="990a8-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="990a8-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="990a8-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="990a8-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-186">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="990a8-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="990a8-187">Sistema operativo di destinazione dell'elemento software proprietario.</span><span class="sxs-lookup"><span data-stu-id="990a8-187">Target operating system of the owning software element.</span></span>

<span data-ttu-id="990a8-188">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-188">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="990a8-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="990a8-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="990a8-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="990a8-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="990a8-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="990a8-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="990a8-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="990a8-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="990a8-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="990a8-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="990a8-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="990a8-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="990a8-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="990a8-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="990a8-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="990a8-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="990a8-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-198">Apri VM</span><span class="sxs-lookup"><span data-stu-id="990a8-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="990a8-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="990a8-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="990a8-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="990a8-201"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="990a8-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="990a8-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="990a8-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="990a8-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="990a8-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="990a8-204"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="990a8-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="990a8-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="990a8-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-206">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="990a8-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="990a8-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="990a8-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="990a8-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="990a8-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="990a8-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="990a8-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="990a8-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="990a8-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="990a8-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="990a8-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="990a8-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="990a8-214"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="990a8-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="990a8-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="990a8-216"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="990a8-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="990a8-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="990a8-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="990a8-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="990a8-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="990a8-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="990a8-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="990a8-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="990a8-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="990a8-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="990a8-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="990a8-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="990a8-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="990a8-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="990a8-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="990a8-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="990a8-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="990a8-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="990a8-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="990a8-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="990a8-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="990a8-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="990a8-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="990a8-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="990a8-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="990a8-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="990a8-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="990a8-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="990a8-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-232">Serie A</span><span class="sxs-lookup"><span data-stu-id="990a8-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="990a8-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="990a8-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-234">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="990a8-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="990a8-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="990a8-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-236">NT tandem</span><span class="sxs-lookup"><span data-stu-id="990a8-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="990a8-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="990a8-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="990a8-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="990a8-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="990a8-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="990a8-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="990a8-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="990a8-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="990a8-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="990a8-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="990a8-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="990a8-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="990a8-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="990a8-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="990a8-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-245">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="990a8-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="990a8-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="990a8-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="990a8-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="990a8-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="990a8-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="990a8-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="990a8-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="990a8-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="990a8-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="990a8-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="990a8-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="990a8-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="990a8-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="990a8-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="990a8-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="990a8-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="990a8-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="990a8-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="990a8-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="990a8-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="990a8-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="990a8-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="990a8-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="990a8-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="990a8-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-259">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="990a8-259">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="990a8-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="990a8-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="990a8-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="990a8-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="990a8-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="990a8-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="990a8-263">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="990a8-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="990a8-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="990a8-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="990a8-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="990a8-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="990a8-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="990a8-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="990a8-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="990a8-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="990a8-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="990a8-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="990a8-269">**Versione**</span><span class="sxs-lookup"><span data-stu-id="990a8-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="990a8-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="990a8-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="990a8-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="990a8-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="990a8-272">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="990a8-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="990a8-273">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="990a8-273">Version of the operation.</span></span>

<span data-ttu-id="990a8-274">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="990a8-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="990a8-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="990a8-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="990a8-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="990a8-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="990a8-277">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-277">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="990a8-278">Commenti</span><span class="sxs-lookup"><span data-stu-id="990a8-278">Remarks</span></span>

<span data-ttu-id="990a8-279">La classe **CIM \_ RemoveDirectoryAction** è derivata da [**CIM \_ DirectoryAction**](cim-directoryaction.md).</span><span class="sxs-lookup"><span data-stu-id="990a8-279">The **CIM\_RemoveDirectoryAction** class is derived from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

<span data-ttu-id="990a8-280">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="990a8-280">WMI does not implement this class.</span></span>

<span data-ttu-id="990a8-281">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="990a8-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="990a8-282">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="990a8-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="990a8-283">Requisiti</span><span class="sxs-lookup"><span data-stu-id="990a8-283">Requirements</span></span>



| <span data-ttu-id="990a8-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="990a8-284">Requirement</span></span> | <span data-ttu-id="990a8-285">Valore</span><span class="sxs-lookup"><span data-stu-id="990a8-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="990a8-286">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="990a8-286">Minimum supported client</span></span><br/> | <span data-ttu-id="990a8-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="990a8-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="990a8-288">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="990a8-288">Minimum supported server</span></span><br/> | <span data-ttu-id="990a8-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="990a8-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="990a8-290">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="990a8-290">Namespace</span></span><br/>                | <span data-ttu-id="990a8-291">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="990a8-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="990a8-292">MOF</span><span class="sxs-lookup"><span data-stu-id="990a8-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="990a8-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="990a8-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="990a8-294">DLL</span><span class="sxs-lookup"><span data-stu-id="990a8-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="990a8-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="990a8-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="990a8-296">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="990a8-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="990a8-297">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="990a8-297">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

