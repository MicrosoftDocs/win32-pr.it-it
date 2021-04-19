---
description: La \_ classe CIM SettingCheck specifica le informazioni necessarie per controllare un determinato file di impostazioni per una voce specifica che contiene un valore uguale al valore specificato. Si presuppone che non venga fatta distinzione tra maiuscole e minuscole.
ms.assetid: 0e40276c-e794-4ea1-8937-c6d7f110f97d
ms.tgt_platform: multiple
title: Classe CIM_SettingCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck
- CIM_SettingCheck.Caption
- CIM_SettingCheck.CheckID
- CIM_SettingCheck.CheckMode
- CIM_SettingCheck.CheckType
- CIM_SettingCheck.Description
- CIM_SettingCheck.EntryName
- CIM_SettingCheck.EntryValue
- CIM_SettingCheck.FileName
- CIM_SettingCheck.Name
- CIM_SettingCheck.SectionKey
- CIM_SettingCheck.SoftwareElementID
- CIM_SettingCheck.SoftwareElementState
- CIM_SettingCheck.TargetOperatingSystem
- CIM_SettingCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4b360833f216d9feb839a4ed84a0e1ba4cd61ebf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304763"
---
# <a name="cim_settingcheck-class"></a><span data-ttu-id="b6b8a-104">CIM \_ SettingCheck (classe)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-104">CIM\_SettingCheck class</span></span>

<span data-ttu-id="b6b8a-105">La classe **CIM \_ SettingCheck** specifica le informazioni necessarie per controllare un determinato file di impostazioni per una voce specifica che contiene un valore uguale al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-105">The **CIM\_SettingCheck** class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="b6b8a-106">Si presuppone che non venga fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-106">All comparisons are assumed to be case insensitive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6b8a-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b6b8a-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b6b8a-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b6b8a-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b8a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6b8a-111">Syntax</span></span>

``` syntax
[UUID("{DC1D8140-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SettingCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  uint16  CheckType;
  string  Description;
  string  EntryName;
  string  EntryValue;
  string  FileName;
  string  Name;
  string  SectionKey;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="b6b8a-112">Members</span><span class="sxs-lookup"><span data-stu-id="b6b8a-112">Members</span></span>

<span data-ttu-id="b6b8a-113">La classe **CIM \_ SettingCheck** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b6b8a-113">The **CIM\_SettingCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="b6b8a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b6b8a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b6b8a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6b8a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b6b8a-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="b6b8a-116">Methods</span></span>

<span data-ttu-id="b6b8a-117">La classe **CIM \_ SettingCheck** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-117">The **CIM\_SettingCheck** class has these methods.</span></span>



| <span data-ttu-id="b6b8a-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="b6b8a-118">Method</span></span>                                                    | <span data-ttu-id="b6b8a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6b8a-119">Description</span></span>                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="b6b8a-120">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-120">**Invoke**</span></span>](invoke-method-in-class-cim-settingcheck.md) | <span data-ttu-id="b6b8a-121">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-121">Takes a particular action.</span></span> <span data-ttu-id="b6b8a-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b6b8a-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6b8a-123">Properties</span></span>

<span data-ttu-id="b6b8a-124">La classe **CIM \_ SettingCheck** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-124">The **CIM\_SettingCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6b8a-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-128">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-129">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-129">Short textual description of the object.</span></span>

<span data-ttu-id="b6b8a-130">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-134">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-135">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span> <span data-ttu-id="b6b8a-136">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-140">Se **true**, la condizione dovrebbe esistere nell'ambiente (ad esempio, se un file si trova in un sistema, il metodo [**Invoke**](invoke-method-in-class-cim-settingcheck.md) deve restituire **true**).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-140">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-settingcheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="b6b8a-141">Se **false**, la condizione non deve esistere, ad esempio se un file non si trova in un sistema, il metodo **Invoke** deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-141">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="b6b8a-142">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-143">**CheckType**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-143">**CheckType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-146">Modalità di confronto del valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-146">Way in which the setting value should be compared.</span></span>

<dt>

<span id="Matches"></span><span id="matches"></span><span id="MATCHES"></span>

<span data-ttu-id="b6b8a-147">**Corrisponde** a (0)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-147">**Matches** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Contains"></span><span id="contains"></span><span id="CONTAINS"></span>

<span data-ttu-id="b6b8a-148">**Contains** (1)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-148">**Contains** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6b8a-149">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-152">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-152">Description of the object.</span></span>

<span data-ttu-id="b6b8a-153">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-153">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-154">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-154">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-157">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-157">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-158">Nome della voce da controllare</span><span class="sxs-lookup"><span data-stu-id="b6b8a-158">Name of the entry to be checked</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-159">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-159">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-162">Valore associato alla voce denominata da verificare.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-162">Value that is associated with the named entry to check.</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-163">**FileName**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-163">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-166">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-166">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-167">Nome file del file di impostazioni da controllare.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-167">File name of the setting file to check.</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-168">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-171">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-172">Nome utilizzato per identificare l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-172">Name used to identify the software element.</span></span> <span data-ttu-id="b6b8a-173">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-174">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-174">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-177">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-177">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-178">Chiave della sezione che contiene le impostazioni da controllare.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-178">Key of section that contains the settings to check.</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-179">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-179">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-182">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-183">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-183">Identifier for the software element.</span></span>

<span data-ttu-id="b6b8a-184">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-184">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6b8a-185">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-185">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-186">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-188">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-189">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-189">State of a software element.</span></span>

<span data-ttu-id="b6b8a-190">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-190">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="b6b8a-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-192">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-192">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="b6b8a-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-194">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-194">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="b6b8a-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-196">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-196">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="b6b8a-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-198">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-198">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6b8a-199">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-199">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-200">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-202">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="b6b8a-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-203">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-203">Target operating system of the software element.</span></span>

<span data-ttu-id="b6b8a-204">Questa proprietà viene ereditata [**dal \_ controllo CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="b6b8a-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6b8a-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b6b8a-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="b6b8a-207"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-208">Mac OS</span><span class="sxs-lookup"><span data-stu-id="b6b8a-208">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="b6b8a-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-210">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="b6b8a-210">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="b6b8a-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="b6b8a-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="b6b8a-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="b6b8a-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-215">Apri VM</span><span class="sxs-lookup"><span data-stu-id="b6b8a-215">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="b6b8a-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-217">HP-UX</span><span class="sxs-lookup"><span data-stu-id="b6b8a-217">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="b6b8a-218"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="b6b8a-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="b6b8a-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="b6b8a-221"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="b6b8a-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-223">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="b6b8a-223">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="b6b8a-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="b6b8a-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-226">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="b6b8a-226">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="b6b8a-227"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-228">Windows 95</span><span class="sxs-lookup"><span data-stu-id="b6b8a-228">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="b6b8a-229"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-230">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b6b8a-230">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="b6b8a-231"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-232">Windows NT</span><span class="sxs-lookup"><span data-stu-id="b6b8a-232">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="b6b8a-233"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-234">Windows CE</span><span class="sxs-lookup"><span data-stu-id="b6b8a-234">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="b6b8a-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-236">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="b6b8a-236">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="b6b8a-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="b6b8a-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="b6b8a-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="b6b8a-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="b6b8a-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="b6b8a-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="b6b8a-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="b6b8a-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="b6b8a-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="b6b8a-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="b6b8a-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="b6b8a-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-249">Serie A</span><span class="sxs-lookup"><span data-stu-id="b6b8a-249">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="b6b8a-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-251">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="b6b8a-251">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="b6b8a-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-253">NT tandem</span><span class="sxs-lookup"><span data-stu-id="b6b8a-253">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="b6b8a-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-255">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="b6b8a-255">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="b6b8a-256"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="b6b8a-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="b6b8a-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="b6b8a-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="b6b8a-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="b6b8a-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-262">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="b6b8a-262">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="b6b8a-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="b6b8a-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="b6b8a-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="b6b8a-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-267">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="b6b8a-267">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="b6b8a-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="b6b8a-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="b6b8a-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="b6b8a-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="b6b8a-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="b6b8a-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="b6b8a-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="b6b8a-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="b6b8a-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="b6b8a-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="b6b8a-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="b6b8a-279">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="b6b8a-279">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="b6b8a-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="b6b8a-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="b6b8a-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="b6b8a-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="b6b8a-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="b6b8a-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6b8a-285">**Versione**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-285">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6b8a-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6b8a-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6b8a-288">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="b6b8a-288">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b6b8a-289">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-289">Version of the operation.</span></span>

<span data-ttu-id="b6b8a-290">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="b6b8a-290">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="b6b8a-291"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="b6b8a-291"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="b6b8a-292"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="b6b8a-292"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="b6b8a-293">Questa proprietà viene ereditata dalla classe di [**\_ controllo CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b8a-293">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6b8a-294">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6b8a-294">Remarks</span></span>

<span data-ttu-id="b6b8a-295">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-295">WMI does not implement this class.</span></span>

<span data-ttu-id="b6b8a-296">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-296">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b6b8a-297">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b6b8a-297">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b8a-298">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6b8a-298">Requirements</span></span>



| <span data-ttu-id="b6b8a-299">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b8a-299">Requirement</span></span> | <span data-ttu-id="b6b8a-300">Valore</span><span class="sxs-lookup"><span data-stu-id="b6b8a-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b8a-301">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6b8a-301">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b8a-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6b8a-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6b8a-303">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6b8a-303">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b8a-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6b8a-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6b8a-305">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6b8a-305">Namespace</span></span><br/>                | <span data-ttu-id="b6b8a-306">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b6b8a-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6b8a-307">MOF</span><span class="sxs-lookup"><span data-stu-id="b6b8a-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6b8a-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6b8a-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6b8a-309">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b8a-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b8a-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b8a-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b8a-311">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6b8a-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b8a-312">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="b6b8a-312">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

