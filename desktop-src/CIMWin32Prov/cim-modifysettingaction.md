---
description: La \_ classe CIM ModifySettingAction rappresenta le informazioni per la modifica di un file di impostazioni specifico, per una voce specifica, con un valore specifico.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: Classe CIM_ModifySettingAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748690"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="ca9ce-103">CIM \_ ModifySettingAction (classe)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="ca9ce-104">La classe **CIM \_ ModifySettingAction** rappresenta le informazioni per la modifica di un file di impostazioni specifico, per una voce specifica, con un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca9ce-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ca9ce-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ca9ce-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ca9ce-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca9ce-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca9ce-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
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
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="ca9ce-110">Members</span><span class="sxs-lookup"><span data-stu-id="ca9ce-110">Members</span></span>

<span data-ttu-id="ca9ce-111">La classe **CIM \_ ModifySettingAction** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca9ce-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="ca9ce-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ca9ce-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca9ce-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca9ce-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca9ce-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="ca9ce-114">Methods</span></span>

<span data-ttu-id="ca9ce-115">La classe **CIM \_ ModifySettingAction** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="ca9ce-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="ca9ce-116">Method</span></span>                                                           | <span data-ttu-id="ca9ce-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca9ce-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="ca9ce-118">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="ca9ce-119">Esegue un'azione specifica.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-119">Takes a specific action.</span></span> <span data-ttu-id="ca9ce-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ca9ce-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca9ce-121">Properties</span></span>

<span data-ttu-id="ca9ce-122">La classe **CIM \_ ModifySettingAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca9ce-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-126">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-127">Identificatore univoco assegnato a una determinata azione per un elemento software.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="ca9ce-128">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-129">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-132">Tipo di azione da eseguire sulla voce di impostazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="ca9ce-133">Si presuppone che le aggiunte siano sensibili alla distinzione tra maiuscole e minuscole. Tuttavia, si presuppone che non venga fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="ca9ce-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Creazione** (0)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-135">Crea la voce specificata.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="ca9ce-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Elimina** (1)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-137">Elimina la voce specificata.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="ca9ce-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Accoda** (2)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-139">Aggiunge alla fine della voce specificata.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="ca9ce-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Rimuovi** (3)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-141">Rimuove il valore dalla voce specificata.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca9ce-142">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-145">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-146">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-146">Short textual description of the object.</span></span>

<span data-ttu-id="ca9ce-147">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-148">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-151">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-151">Description of the object.</span></span>

<span data-ttu-id="ca9ce-152">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-153">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-156">Indica se un particolare [**oggetto \_ azione CIM**](cim-action.md) fa parte di una sequenza di azioni per la transizione dell'elemento software corrente allo stato successivo, ad esempio "Install", o per rimuovere l'elemento software corrente, ad esempio "uninstall".</span><span class="sxs-lookup"><span data-stu-id="ca9ce-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="ca9ce-157">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="ca9ce-158">**Installazione** (0)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="ca9ce-159">**Disinstalla** (1)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca9ce-160">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-163">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-164">Nome della voce da modificare.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-165">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-168">Valore da aggiungere, aggiungere o per sostituire l'impostazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-172">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-173">Nome file della voce del file di impostazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-174">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-177">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-178">Identifica l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-178">Identifies the software element.</span></span>

<span data-ttu-id="ca9ce-179">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-180">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-183">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-184">Chiave della sezione della voce di impostazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-185">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-188">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-189">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-189">Identifier for the software element.</span></span>

<span data-ttu-id="ca9ce-190">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca9ce-191">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-192">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-194">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-195">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-195">State of a software element.</span></span>

<span data-ttu-id="ca9ce-196">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ca9ce-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-198">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ca9ce-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-200">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ca9ce-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-202">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ca9ce-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-204">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca9ce-205">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-206">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-208">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="ca9ce-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-209">Sistema operativo di destinazione dell'elemento software proprietario.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="ca9ce-210">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca9ce-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca9ce-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ca9ce-213"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-214">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ca9ce-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ca9ce-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ca9ce-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ca9ce-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ca9ce-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ca9ce-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-220">Apri VM</span><span class="sxs-lookup"><span data-stu-id="ca9ce-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ca9ce-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ca9ce-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ca9ce-223"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ca9ce-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ca9ce-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ca9ce-226"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ca9ce-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-228">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="ca9ce-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ca9ce-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ca9ce-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-231">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ca9ce-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ca9ce-232"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ca9ce-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ca9ce-234"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ca9ce-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ca9ce-236"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ca9ce-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ca9ce-238"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ca9ce-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ca9ce-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-241">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ca9ce-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ca9ce-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ca9ce-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ca9ce-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ca9ce-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ca9ce-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ca9ce-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ca9ce-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ca9ce-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ca9ce-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ca9ce-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ca9ce-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ca9ce-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-254">Serie A</span><span class="sxs-lookup"><span data-stu-id="ca9ce-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ca9ce-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-256">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="ca9ce-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ca9ce-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-258">NT tandem</span><span class="sxs-lookup"><span data-stu-id="ca9ce-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ca9ce-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ca9ce-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ca9ce-261"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ca9ce-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ca9ce-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ca9ce-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ca9ce-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ca9ce-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-267">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="ca9ce-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ca9ce-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ca9ce-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ca9ce-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ca9ce-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ca9ce-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ca9ce-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ca9ce-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ca9ce-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ca9ce-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ca9ce-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ca9ce-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ca9ce-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ca9ce-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-281">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ca9ce-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ca9ce-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ca9ce-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ca9ce-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ca9ce-285">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="ca9ce-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ca9ce-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ca9ce-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ca9ce-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ca9ce-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ca9ce-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ca9ce-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca9ce-291">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca9ce-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca9ce-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca9ce-294">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="ca9ce-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ca9ce-295">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-295">Version of the operation.</span></span>

<span data-ttu-id="ca9ce-296">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="ca9ce-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ca9ce-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="ca9ce-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="ca9ce-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="ca9ce-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="ca9ce-299">Questa proprietà viene ereditata [**dall' \_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca9ce-300">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca9ce-300">Remarks</span></span>

<span data-ttu-id="ca9ce-301">La classe **CIM \_ ModifySettingAction** è derivata dall' [**\_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca9ce-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="ca9ce-302">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-302">WMI does not implement this class.</span></span>

<span data-ttu-id="ca9ce-303">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ca9ce-304">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ca9ce-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca9ce-305">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca9ce-305">Requirements</span></span>



| <span data-ttu-id="ca9ce-306">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca9ce-306">Requirement</span></span> | <span data-ttu-id="ca9ce-307">Valore</span><span class="sxs-lookup"><span data-stu-id="ca9ce-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca9ce-308">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca9ce-308">Minimum supported client</span></span><br/> | <span data-ttu-id="ca9ce-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca9ce-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca9ce-310">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca9ce-310">Minimum supported server</span></span><br/> | <span data-ttu-id="ca9ce-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca9ce-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca9ce-312">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca9ce-312">Namespace</span></span><br/>                | <span data-ttu-id="ca9ce-313">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ca9ce-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca9ce-314">MOF</span><span class="sxs-lookup"><span data-stu-id="ca9ce-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca9ce-315"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca9ce-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca9ce-316">DLL</span><span class="sxs-lookup"><span data-stu-id="ca9ce-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca9ce-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca9ce-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca9ce-318">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca9ce-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca9ce-319">**\_Azione CIM**</span><span class="sxs-lookup"><span data-stu-id="ca9ce-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

