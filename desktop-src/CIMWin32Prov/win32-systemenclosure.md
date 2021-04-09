---
description: Rappresenta le proprietà associate a un'enclosure di sistema fisica.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Classe Win32_SystemEnclosure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966326"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="ae430-103">Win32 \_ SystemEnclosure (classe)</span><span class="sxs-lookup"><span data-stu-id="ae430-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="ae430-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemEnclosure Win32** rappresenta le proprietà associate a un'enclosure di sistema fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="ae430-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ae430-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ae430-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ae430-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae430-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae430-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="ae430-108">Members</span><span class="sxs-lookup"><span data-stu-id="ae430-108">Members</span></span>

<span data-ttu-id="ae430-109">La classe **Win32 \_ SystemEnclosure** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ae430-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="ae430-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ae430-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae430-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ae430-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae430-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ae430-112">Methods</span></span>

<span data-ttu-id="ae430-113">La classe **Win32 \_ SystemEnclosure** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ae430-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="ae430-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="ae430-114">Method</span></span>           | <span data-ttu-id="ae430-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae430-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="ae430-116">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="ae430-116">**IsCompatible**</span></span> | <span data-ttu-id="ae430-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="ae430-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae430-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ae430-118">Properties</span></span>

<span data-ttu-id="ae430-119">La classe **Win32 \_ SystemEnclosure** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ae430-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae430-120">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="ae430-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-121">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-123">Se **true**, il frame è dotato di un allarme acustico.</span><span class="sxs-lookup"><span data-stu-id="ae430-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="ae430-124">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-125">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="ae430-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-128">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="ae430-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-129">Stringa in formato libero che fornisce ulteriori informazioni se la proprietà **SecurityBreach** indica che si è verificato un evento correlato alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ae430-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="ae430-130">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-131">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="ae430-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-134">Stringa in formato libero che contiene informazioni sul modo in cui i vari cavi sono connessi e in bundle per il frame.</span><span class="sxs-lookup"><span data-stu-id="ae430-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="ae430-135">Con molti cavi di rete, correlati all'archiviazione e di alimentazione, la gestione dei cavi può essere un'attività complessa e impegnativa.</span><span class="sxs-lookup"><span data-stu-id="ae430-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="ae430-136">Questa proprietà contiene informazioni per facilitare l'assembly e il servizio del frame.</span><span class="sxs-lookup"><span data-stu-id="ae430-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="ae430-137">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ae430-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-141">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ae430-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-142">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="ae430-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="ae430-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-144">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="ae430-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-145">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae430-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae430-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-147">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,1 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chassis CIM**](cim-chassis.md).**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="ae430-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-148">Matrice di tipi di chassis.</span><span class="sxs-lookup"><span data-stu-id="ae430-148">Array of chassis types.</span></span>

<span data-ttu-id="ae430-149">Questo valore deriva dal membro del **tipo** dell' **enclosure di sistema o** della struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae430-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ae430-150">Questa proprietà viene ereditata [**dallo \_ chassis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae430-151">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae430-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae430-152">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ae430-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="ae430-153">**Desktop** (3)</span><span class="sxs-lookup"><span data-stu-id="ae430-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="ae430-154">**Desktop con profili bassi** (4)</span><span class="sxs-lookup"><span data-stu-id="ae430-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="ae430-155">**Casella pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="ae430-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="ae430-156">**Mini-Tower** (6)</span><span class="sxs-lookup"><span data-stu-id="ae430-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="ae430-157">**Tower** (7)</span><span class="sxs-lookup"><span data-stu-id="ae430-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="ae430-158">**Portatile** (8)</span><span class="sxs-lookup"><span data-stu-id="ae430-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="ae430-159">**Portatile** (9)</span><span class="sxs-lookup"><span data-stu-id="ae430-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="ae430-160">**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="ae430-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="ae430-161">**Hand mantenuti** (11)</span><span class="sxs-lookup"><span data-stu-id="ae430-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="ae430-162">**Docking station** (12)</span><span class="sxs-lookup"><span data-stu-id="ae430-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="ae430-163">**Tutto in uno** (13)</span><span class="sxs-lookup"><span data-stu-id="ae430-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="ae430-164">**Notebook secondario** (14)</span><span class="sxs-lookup"><span data-stu-id="ae430-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="ae430-165">**Risparmio di spazio** (15)</span><span class="sxs-lookup"><span data-stu-id="ae430-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="ae430-166">**Lunch box** (16)</span><span class="sxs-lookup"><span data-stu-id="ae430-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="ae430-167">**Chassis del sistema principale** (17)</span><span class="sxs-lookup"><span data-stu-id="ae430-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="ae430-168">**Chassis di espansione** (18)</span><span class="sxs-lookup"><span data-stu-id="ae430-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="ae430-169">**Sottochassis** (19)</span><span class="sxs-lookup"><span data-stu-id="ae430-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="ae430-170">**Chassis di espansione del bus** (20)</span><span class="sxs-lookup"><span data-stu-id="ae430-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="ae430-171">**Chassis periferico** (21)</span><span class="sxs-lookup"><span data-stu-id="ae430-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="ae430-172">**Chassis di archiviazione** (22)</span><span class="sxs-lookup"><span data-stu-id="ae430-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="ae430-173">**Chassis montaggio rack** (23)</span><span class="sxs-lookup"><span data-stu-id="ae430-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="ae430-174">**Computer con case sealed** (24)</span><span class="sxs-lookup"><span data-stu-id="ae430-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="ae430-175">**Tablet** (30)</span><span class="sxs-lookup"><span data-stu-id="ae430-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="ae430-176">**Convertibile** (31)</span><span class="sxs-lookup"><span data-stu-id="ae430-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="ae430-177">**Scollegabile** (32)</span><span class="sxs-lookup"><span data-stu-id="ae430-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae430-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ae430-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-181">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="ae430-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-182">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ae430-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="ae430-183">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ae430-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="ae430-184">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-185">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="ae430-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-186">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="ae430-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-188">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("amps a 120 volt")</span><span class="sxs-lookup"><span data-stu-id="ae430-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-189">Corrente richiesta dallo chassis a 120V.</span><span class="sxs-lookup"><span data-stu-id="ae430-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="ae430-190">Se il potere viene fornito dallo chassis, come nel caso di un gruppo di continuità (UPS), questa proprietà può indicare l'amperaggio prodotto (come numero negativo).</span><span class="sxs-lookup"><span data-stu-id="ae430-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="ae430-191">Questa proprietà viene ereditata [**dallo \_ chassis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-192">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="ae430-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-193">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="ae430-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-195">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="ae430-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-196">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="ae430-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="ae430-197">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-198">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ae430-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-201">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ae430-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-202">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ae430-202">Description of the object.</span></span>

<span data-ttu-id="ae430-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-204">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="ae430-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-205">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae430-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-207">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("BTU per ora")</span><span class="sxs-lookup"><span data-stu-id="ae430-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-208">Quantità di calore generata dallo chassis in BTU/ora.</span><span class="sxs-lookup"><span data-stu-id="ae430-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="ae430-209">Questa proprietà viene ereditata [**dallo \_ chassis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-210">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="ae430-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-211">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="ae430-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-213">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="ae430-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-214">Altezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="ae430-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="ae430-215">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-216">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="ae430-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-217">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-219">Se **true**, un pacchetto fisico può essere scambiato a caldo (se è possibile sostituire l'elemento con un oggetto fisicamente diverso ma equivalente mentre al pacchetto che lo contiene è stata applicata una potenza).</span><span class="sxs-lookup"><span data-stu-id="ae430-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="ae430-220">Ad esempio, un pacchetto di unità disco inserito utilizzando connettori SCA è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="ae430-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="ae430-221">Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="ae430-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="ae430-222">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae430-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-224">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae430-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-226">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ae430-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-227">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ae430-227">Date and time the object was installed.</span></span> <span data-ttu-id="ae430-228">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="ae430-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ae430-229">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-230">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="ae430-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-233">Se **true**, il frame è protetto con un blocco.</span><span class="sxs-lookup"><span data-stu-id="ae430-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="ae430-234">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-235">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="ae430-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-238">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="ae430-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-239">Nome dell'organizzazione che produce l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="ae430-240">Questo valore deriva dal membro del **produttore** dell' **enclosure di sistema o** della struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae430-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ae430-241">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-242">**Modello**</span><span class="sxs-lookup"><span data-stu-id="ae430-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-245">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ae430-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-246">Nome con cui l'elemento fisico è noto.</span><span class="sxs-lookup"><span data-stu-id="ae430-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="ae430-247">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-248">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ae430-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-251">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ae430-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-252">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="ae430-252">Label by which the object is known.</span></span> <span data-ttu-id="ae430-253">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="ae430-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="ae430-254">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-255">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="ae430-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-256">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae430-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-258">Numero di cavi di alimentazione che devono essere connessi allo chassis per il funzionamento di tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="ae430-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="ae430-259">Questa proprietà viene ereditata [**dallo \_ chassis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ae430-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-263">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="ae430-264">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="ae430-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="ae430-265">Tenere presente che, se sono disponibili solo i dati del codice a barre ed è univoco o in grado di essere utilizzati come chiave di elemento, questa proprietà sarà **null** e i dati di codice a barre utilizzati come chiave della classe nella proprietà Tag.</span><span class="sxs-lookup"><span data-stu-id="ae430-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="ae430-266">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-267">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="ae430-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-270">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="ae430-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-271">Numero di parte assegnato dall'organizzazione che produce o produce l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="ae430-272">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-273">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="ae430-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-274">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-276">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="ae430-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="ae430-277">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-278">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="ae430-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-279">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-281">Se il valore è **true**, un pacchetto fisico è rimovibile (se è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti).</span><span class="sxs-lookup"><span data-stu-id="ae430-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="ae430-282">Un pacchetto può comunque essere rimovibile se la potenza deve essere "OFF" per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="ae430-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="ae430-283">Se il pacchetto può essere rimosso mentre l'alimentazione è attiva, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="ae430-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="ae430-284">Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco che viene inserito usando i connettori SCA (Server Configuration Application).</span><span class="sxs-lookup"><span data-stu-id="ae430-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="ae430-285">Tuttavia, quest'ultimo può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="ae430-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="ae430-286">Uno schermo portatile non è rimovibile, né un alimentatore non ridondante.</span><span class="sxs-lookup"><span data-stu-id="ae430-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="ae430-287">La rimozione di questi componenti influisce sulla funzione della creazione complessiva dei pacchetti oppure è impossibile a causa della stretta integrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ae430-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="ae430-288">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-289">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="ae430-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-290">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-292">Se **true**, questo componente multimediale fisico può essere sostituito con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="ae430-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="ae430-293">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="ae430-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="ae430-294">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="ae430-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="ae430-295">Un altro esempio è un pacchetto di alimentazione montato sulle guide scorrevoli.</span><span class="sxs-lookup"><span data-stu-id="ae430-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="ae430-296">Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="ae430-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="ae430-297">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-298">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="ae430-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-299">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae430-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-301">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,12 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="ae430-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-302">Stato di una violazione fisica del frame.</span><span class="sxs-lookup"><span data-stu-id="ae430-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="ae430-303">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae430-304">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae430-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae430-305">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ae430-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="ae430-306">**Nessuna violazione** (3)</span><span class="sxs-lookup"><span data-stu-id="ae430-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="ae430-307">**Tentativo di violazione** (4)</span><span class="sxs-lookup"><span data-stu-id="ae430-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="ae430-308">**Violazione riuscita** (5)</span><span class="sxs-lookup"><span data-stu-id="ae430-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae430-309">**SecurityStatus**</span><span class="sxs-lookup"><span data-stu-id="ae430-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-310">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae430-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-312">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 3 \| Security Status")</span><span class="sxs-lookup"><span data-stu-id="ae430-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-313">Impostazione di sicurezza per input esterno, ad esempio una tastiera, in un computer.</span><span class="sxs-lookup"><span data-stu-id="ae430-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="ae430-314">Questo valore deriva dal membro dello **stato di sicurezza** dell' **enclosure di sistema o** dalla struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae430-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae430-315">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae430-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae430-316">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ae430-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ae430-317">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="ae430-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="ae430-318">**Interfaccia esterna bloccata** (4)</span><span class="sxs-lookup"><span data-stu-id="ae430-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="ae430-319">**Interfaccia esterna abilitata** (5)</span><span class="sxs-lookup"><span data-stu-id="ae430-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae430-320">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ae430-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-323">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ae430-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-324">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="ae430-325">Questo valore deriva dal membro del **numero di serie** dell' **enclosure di sistema o** della struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae430-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ae430-326">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-327">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ae430-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-328">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ae430-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae430-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-330">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="ae430-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-331">Matrice di spiegazioni più dettagliate per tutte le voci della matrice **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="ae430-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="ae430-332">Tenere presente che ogni voce di questa matrice è correlata alla voce in **ServicePhilosophy** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="ae430-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="ae430-333">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-334">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="ae430-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-335">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae430-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae430-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-337">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="ae430-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-338">Matrice che indica se il frame viene servito dalla parte superiore, anteriore, posteriore o laterale, se il frame dispone di barra di scorrimento o di lati rimovibili e se il frame è mobile, ad esempio se è presente un rullo.</span><span class="sxs-lookup"><span data-stu-id="ae430-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="ae430-339">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae430-340">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ae430-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae430-341">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae430-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="ae430-342">**Servizio dall'inizio** (2)</span><span class="sxs-lookup"><span data-stu-id="ae430-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="ae430-343">**Servizio dall'inizio** (3)</span><span class="sxs-lookup"><span data-stu-id="ae430-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="ae430-344">**Servizio da indietro** (4)</span><span class="sxs-lookup"><span data-stu-id="ae430-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="ae430-345">**Servizio dal lato** (5)</span><span class="sxs-lookup"><span data-stu-id="ae430-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="ae430-346">**Vassoi scorrevoli** (6)</span><span class="sxs-lookup"><span data-stu-id="ae430-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="ae430-347">**Lati rimovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="ae430-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="ae430-348">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="ae430-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae430-349">**SKU**</span><span class="sxs-lookup"><span data-stu-id="ae430-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-352">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ae430-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-353">Numero di unità di conservazione per l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="ae430-354">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="ae430-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-358">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 3 \| asset tag")</span><span class="sxs-lookup"><span data-stu-id="ae430-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-359">Numero di tag asset dell'enclosure di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae430-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="ae430-360">Questo valore deriva dal membro del **numero di tag asset** dell' **enclosure di sistema o** della struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae430-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="ae430-361">**Status**</span><span class="sxs-lookup"><span data-stu-id="ae430-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-362">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-364">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="ae430-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-365">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ae430-365">Current status of the object.</span></span> <span data-ttu-id="ae430-366">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="ae430-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ae430-367">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="ae430-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ae430-368">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="ae430-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ae430-369">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="ae430-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ae430-370">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="ae430-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ae430-371">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ae430-372">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae430-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ae430-373">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ae430-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ae430-374">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ae430-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ae430-375">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ae430-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae430-376">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ae430-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ae430-377">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ae430-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ae430-378">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ae430-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ae430-379">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ae430-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ae430-380">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ae430-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ae430-381">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ae430-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ae430-382">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ae430-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ae430-383">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ae430-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ae430-384">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ae430-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae430-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="ae430-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-386">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-388">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="ae430-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-389">Identificatore univoco dell'enclosure di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae430-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="ae430-390">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="ae430-391">Esempio: "System Enclosure 1"</span><span class="sxs-lookup"><span data-stu-id="ae430-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="ae430-392">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ae430-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-393">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ae430-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae430-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-395">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ chassis**](cim-chassis.md).**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="ae430-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-396">Matrice di ulteriori informazioni sulle voci della matrice **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="ae430-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="ae430-397">Tenere presente che ogni voce di questa matrice è correlata alla voce in **ChassisTypes** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="ae430-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="ae430-398">Questa proprietà viene ereditata [**dallo \_ chassis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-399">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ae430-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ae430-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-402">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ae430-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ae430-403">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="ae430-403">Version of the physical element.</span></span>

<span data-ttu-id="ae430-404">Questo valore deriva dal membro della **versione** dell' **enclosure di sistema o** della struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae430-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ae430-405">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-406">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="ae430-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-407">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae430-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae430-409">Se **true**, l'apparecchiatura include un allarme visibile.</span><span class="sxs-lookup"><span data-stu-id="ae430-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="ae430-410">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-411">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ae430-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-412">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="ae430-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-414">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="ae430-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-415">Peso del pacchetto fisico in sterline.</span><span class="sxs-lookup"><span data-stu-id="ae430-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="ae430-416">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae430-417">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="ae430-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae430-418">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="ae430-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ae430-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ae430-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae430-420">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="ae430-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ae430-421">Larghezza del pacchetto fisico in pollici.</span><span class="sxs-lookup"><span data-stu-id="ae430-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="ae430-422">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae430-423">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae430-423">Remarks</span></span>

<span data-ttu-id="ae430-424">La classe **Win32 \_ SystemEnclosure** è derivata dallo [**\_ chassis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="ae430-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ae430-425">Esempio</span><span class="sxs-lookup"><span data-stu-id="ae430-425">Examples</span></span>

<span data-ttu-id="ae430-426">L'esempio di [raccolta di asset di sistema multithreading con](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell PowerShell nella raccolta TechNet usa diverse classi, tra cui **Win32 \_ SystemEnclosure**, per recuperare i dati da un sistema.</span><span class="sxs-lookup"><span data-stu-id="ae430-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae430-427">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae430-427">Requirements</span></span>



| <span data-ttu-id="ae430-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae430-428">Requirement</span></span> | <span data-ttu-id="ae430-429">Valore</span><span class="sxs-lookup"><span data-stu-id="ae430-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae430-430">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae430-430">Minimum supported client</span></span><br/> | <span data-ttu-id="ae430-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae430-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae430-432">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae430-432">Minimum supported server</span></span><br/> | <span data-ttu-id="ae430-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae430-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae430-434">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae430-434">Namespace</span></span><br/>                | <span data-ttu-id="ae430-435">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ae430-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae430-436">MOF</span><span class="sxs-lookup"><span data-stu-id="ae430-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae430-437"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae430-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae430-438">DLL</span><span class="sxs-lookup"><span data-stu-id="ae430-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae430-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae430-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae430-440">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae430-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae430-441">**\_Chassis CIM**</span><span class="sxs-lookup"><span data-stu-id="ae430-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="ae430-442">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ae430-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ae430-443">Attività WMI: hardware del computer</span><span class="sxs-lookup"><span data-stu-id="ae430-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
