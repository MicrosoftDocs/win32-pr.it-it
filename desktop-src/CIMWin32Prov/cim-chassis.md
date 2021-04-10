---
description: La \_ classe chassis CIM rappresenta gli elementi fisici che racchiudono altri elementi e fornisce funzionalità definibili, ad esempio un desktop, un nodo di elaborazione, un UPS, un'archiviazione su disco o su nastro o una combinazione di questi.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: Classe CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127115"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="5a11a-103">\_Classe chassis CIM</span><span class="sxs-lookup"><span data-stu-id="5a11a-103">CIM\_Chassis class</span></span>

<span data-ttu-id="5a11a-104">La **classe \_ chassis CIM** rappresenta gli elementi fisici che racchiudono altri elementi e fornisce funzionalità definibili, ad esempio un desktop, un nodo di elaborazione, un UPS, un'archiviazione su disco o su nastro o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="5a11a-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a11a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5a11a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5a11a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5a11a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5a11a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5a11a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5a11a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5a11a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a11a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a11a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="5a11a-110">Members</span><span class="sxs-lookup"><span data-stu-id="5a11a-110">Members</span></span>

<span data-ttu-id="5a11a-111">La **classe \_ chassis CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5a11a-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="5a11a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5a11a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a11a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a11a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a11a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="5a11a-114">Methods</span></span>

<span data-ttu-id="5a11a-115">La **classe \_ chassis CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5a11a-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="5a11a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="5a11a-116">Method</span></span>                                                           | <span data-ttu-id="5a11a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a11a-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a11a-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="5a11a-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="5a11a-119">Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="5a11a-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="5a11a-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5a11a-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a11a-121">Properties</span></span>

<span data-ttu-id="5a11a-122">La **classe \_ chassis CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a11a-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a11a-123">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="5a11a-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-126">Se **true**, il frame è dotato di un allarme acustico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="5a11a-127">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="5a11a-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="5a11a-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-132">Stringa in formato libero che fornisce ulteriori informazioni se la proprietà **SecurityBreach** indica che si è verificata una violazione o un altro evento correlato alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5a11a-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="5a11a-133">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-134">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="5a11a-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-137">Stringa in formato libero che contiene informazioni sul modo in cui i vari cavi sono connessi e in bundle per il frame.</span><span class="sxs-lookup"><span data-stu-id="5a11a-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="5a11a-138">Con molti cavi di rete, correlati all'archiviazione e di alimentazione, la gestione dei cavi può essere un'attività complessa e impegnativa.</span><span class="sxs-lookup"><span data-stu-id="5a11a-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="5a11a-139">Questa proprietà di stringa contiene informazioni per facilitare l'assembly e il servizio del frame.</span><span class="sxs-lookup"><span data-stu-id="5a11a-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="5a11a-140">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-141">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5a11a-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-144">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5a11a-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-145">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a11a-145">A short textual description of the object.</span></span>

<span data-ttu-id="5a11a-146">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-147">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="5a11a-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a11a-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-150">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,1 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chassis CIM**.**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="5a11a-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-151">Matrice con valori integer enumerata che indica il tipo di chassis.</span><span class="sxs-lookup"><span data-stu-id="5a11a-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a11a-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5a11a-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-153">Altro.</span><span class="sxs-lookup"><span data-stu-id="5a11a-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a11a-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5a11a-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-155">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5a11a-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="5a11a-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span><span class="sxs-lookup"><span data-stu-id="5a11a-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-157">Desktop.</span><span class="sxs-lookup"><span data-stu-id="5a11a-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="5a11a-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Desktop con profili bassi** (4)</span><span class="sxs-lookup"><span data-stu-id="5a11a-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-159">Desktop con basso profilo.</span><span class="sxs-lookup"><span data-stu-id="5a11a-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="5a11a-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Casella pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="5a11a-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-161">Casella di pizza.</span><span class="sxs-lookup"><span data-stu-id="5a11a-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="5a11a-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini-Tower** (6)</span><span class="sxs-lookup"><span data-stu-id="5a11a-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-163">Mini-Tower.</span><span class="sxs-lookup"><span data-stu-id="5a11a-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="5a11a-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span><span class="sxs-lookup"><span data-stu-id="5a11a-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-165">Tower.</span><span class="sxs-lookup"><span data-stu-id="5a11a-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="5a11a-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portatile** (8)</span><span class="sxs-lookup"><span data-stu-id="5a11a-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-167">Portabile.</span><span class="sxs-lookup"><span data-stu-id="5a11a-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="5a11a-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Portatile** (9)</span><span class="sxs-lookup"><span data-stu-id="5a11a-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-169">Portatile.</span><span class="sxs-lookup"><span data-stu-id="5a11a-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="5a11a-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="5a11a-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-171">Notebook.</span><span class="sxs-lookup"><span data-stu-id="5a11a-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="5a11a-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand mantenuti** (11)</span><span class="sxs-lookup"><span data-stu-id="5a11a-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-173">Gestito manualmente.</span><span class="sxs-lookup"><span data-stu-id="5a11a-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="5a11a-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking station** (12)</span><span class="sxs-lookup"><span data-stu-id="5a11a-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-175">Docking station.</span><span class="sxs-lookup"><span data-stu-id="5a11a-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="5a11a-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Tutto in uno** (13)</span><span class="sxs-lookup"><span data-stu-id="5a11a-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-177">All-in-One.</span><span class="sxs-lookup"><span data-stu-id="5a11a-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="5a11a-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Notebook secondario** (14)</span><span class="sxs-lookup"><span data-stu-id="5a11a-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-179">Subnotebook.</span><span class="sxs-lookup"><span data-stu-id="5a11a-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="5a11a-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Risparmio di spazio** (15)</span><span class="sxs-lookup"><span data-stu-id="5a11a-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-181">Risparmio di spazio.</span><span class="sxs-lookup"><span data-stu-id="5a11a-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="5a11a-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch box** (16)</span><span class="sxs-lookup"><span data-stu-id="5a11a-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-183">Lunch box.</span><span class="sxs-lookup"><span data-stu-id="5a11a-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="5a11a-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Chassis del sistema principale** (17)</span><span class="sxs-lookup"><span data-stu-id="5a11a-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-185">Chassis principale del sistema.</span><span class="sxs-lookup"><span data-stu-id="5a11a-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="5a11a-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Chassis di espansione** (18)</span><span class="sxs-lookup"><span data-stu-id="5a11a-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-187">Chassis di espansione.</span><span class="sxs-lookup"><span data-stu-id="5a11a-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="5a11a-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**Sottochassis** (19)</span><span class="sxs-lookup"><span data-stu-id="5a11a-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-189">Sottochassis.</span><span class="sxs-lookup"><span data-stu-id="5a11a-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="5a11a-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Chassis di espansione del bus** (20)</span><span class="sxs-lookup"><span data-stu-id="5a11a-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-191">Chassis di espansione del bus.</span><span class="sxs-lookup"><span data-stu-id="5a11a-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="5a11a-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Chassis periferico** (21)</span><span class="sxs-lookup"><span data-stu-id="5a11a-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-193">Chassis periferico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="5a11a-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Chassis di archiviazione** (22)</span><span class="sxs-lookup"><span data-stu-id="5a11a-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-195">Chassis di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5a11a-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="5a11a-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Chassis montaggio rack** (23)</span><span class="sxs-lookup"><span data-stu-id="5a11a-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-197">Chassis montaggio rack.</span><span class="sxs-lookup"><span data-stu-id="5a11a-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="5a11a-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Computer con case sealed** (24)</span><span class="sxs-lookup"><span data-stu-id="5a11a-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="5a11a-199">Computer con case sealed.</span><span class="sxs-lookup"><span data-stu-id="5a11a-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a11a-200">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a11a-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-203">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a11a-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-204">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="5a11a-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5a11a-205">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="5a11a-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5a11a-206">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-207">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="5a11a-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-208">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="5a11a-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-210">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps a 120 volt")</span><span class="sxs-lookup"><span data-stu-id="5a11a-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-211">Attualmente richiesto dallo chassis a 120 volt.</span><span class="sxs-lookup"><span data-stu-id="5a11a-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="5a11a-212">Se la potenza viene fornita dallo chassis (come nel caso di un UPS), questa proprietà può indicare l'amperaggio prodotto, come un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="5a11a-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-213">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="5a11a-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-214">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5a11a-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-216">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="5a11a-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-217">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="5a11a-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="5a11a-218">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-219">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5a11a-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-222">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5a11a-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-223">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a11a-223">A textual description of the object.</span></span>

<span data-ttu-id="5a11a-224">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-225">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="5a11a-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-226">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a11a-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-228">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per ora")</span><span class="sxs-lookup"><span data-stu-id="5a11a-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-229">Quantità di calore generata dallo chassis in BTU/ora.</span><span class="sxs-lookup"><span data-stu-id="5a11a-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-230">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="5a11a-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-231">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5a11a-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-233">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="5a11a-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-234">Altezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="5a11a-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="5a11a-235">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-236">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="5a11a-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-237">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-239">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5a11a-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="5a11a-240">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="5a11a-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="5a11a-241">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5a11a-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="5a11a-242">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="5a11a-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="5a11a-243">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5a11a-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-245">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a11a-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-247">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="5a11a-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-248">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="5a11a-248">Indicates when the object was installed.</span></span> <span data-ttu-id="5a11a-249">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="5a11a-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5a11a-250">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-251">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="5a11a-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-252">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-254">Se **true**, il frame è protetto con un blocco.</span><span class="sxs-lookup"><span data-stu-id="5a11a-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="5a11a-255">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-256">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="5a11a-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-259">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a11a-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-260">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="5a11a-261">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="5a11a-262">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-263">**Modello**</span><span class="sxs-lookup"><span data-stu-id="5a11a-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-266">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5a11a-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-267">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="5a11a-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="5a11a-268">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-269">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5a11a-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-272">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5a11a-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-273">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5a11a-273">Label by which the object is known.</span></span> <span data-ttu-id="5a11a-274">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5a11a-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5a11a-275">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-276">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="5a11a-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-277">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a11a-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-279">Numero di cavi di alimentazione che devono essere connessi allo chassis in modo che tutti i componenti possano funzionare.</span><span class="sxs-lookup"><span data-stu-id="5a11a-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5a11a-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-283">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5a11a-284">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="5a11a-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="5a11a-285">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="5a11a-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="5a11a-286">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-287">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="5a11a-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-290">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a11a-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-291">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="5a11a-292">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-293">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="5a11a-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-294">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-296">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="5a11a-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="5a11a-297">In caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="5a11a-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="5a11a-298">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-299">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="5a11a-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-300">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-302">Se **true**, il pacchetto è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5a11a-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="5a11a-303">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="5a11a-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="5a11a-304">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5a11a-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="5a11a-305">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="5a11a-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="5a11a-306">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-307">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="5a11a-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-308">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-310">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="5a11a-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="5a11a-311">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="5a11a-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="5a11a-312">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="5a11a-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="5a11a-313">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="5a11a-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="5a11a-314">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-315">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="5a11a-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-316">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a11a-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-318">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="5a11a-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-319">Indica se una violazione fisica del frame è stata tentata, ma non è stata completata, oppure se è stata tentata e riuscita.</span><span class="sxs-lookup"><span data-stu-id="5a11a-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="5a11a-320">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a11a-321">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5a11a-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a11a-322">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="5a11a-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="5a11a-323">**Nessuna violazione** (3)</span><span class="sxs-lookup"><span data-stu-id="5a11a-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="5a11a-324">**Tentativo di violazione** (4)</span><span class="sxs-lookup"><span data-stu-id="5a11a-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="5a11a-325">**Violazione riuscita** (5)</span><span class="sxs-lookup"><span data-stu-id="5a11a-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a11a-326">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5a11a-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-329">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5a11a-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-330">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5a11a-331">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-332">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a11a-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-333">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5a11a-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-335">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="5a11a-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-336">Stringhe in formato libero che forniscono spiegazioni dettagliate per le voci nella matrice **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="5a11a-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="5a11a-337">Ogni voce di questa matrice è correlata alla voce nella matrice **ServicePhilosophy** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="5a11a-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="5a11a-338">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-339">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="5a11a-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-340">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a11a-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-342">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="5a11a-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-343">Indica se il frame viene servito dalla parte superiore, anteriore, posteriore o laterale; e se sono presenti vassoi scorrevoli o lati rimovibili e se il frame è mobile (ad esempio, con i Roller).</span><span class="sxs-lookup"><span data-stu-id="5a11a-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="5a11a-344">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a11a-345">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5a11a-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a11a-346">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5a11a-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="5a11a-347">**Servizio dall'inizio** (2)</span><span class="sxs-lookup"><span data-stu-id="5a11a-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="5a11a-348">**Servizio dall'inizio** (3)</span><span class="sxs-lookup"><span data-stu-id="5a11a-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="5a11a-349">**Servizio da indietro** (4)</span><span class="sxs-lookup"><span data-stu-id="5a11a-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="5a11a-350">**Servizio dal lato** (5)</span><span class="sxs-lookup"><span data-stu-id="5a11a-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="5a11a-351">**Vassoi scorrevoli** (6)</span><span class="sxs-lookup"><span data-stu-id="5a11a-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="5a11a-352">**Lati rimovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="5a11a-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="5a11a-353">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="5a11a-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a11a-354">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5a11a-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-357">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5a11a-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-358">Numero di unità di conservazione per questo elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="5a11a-359">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-360">**Status**</span><span class="sxs-lookup"><span data-stu-id="5a11a-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-363">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5a11a-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-364">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a11a-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="5a11a-365">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="5a11a-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5a11a-366">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="5a11a-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5a11a-367">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="5a11a-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5a11a-368">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5a11a-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5a11a-369">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5a11a-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5a11a-370">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5a11a-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5a11a-371">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5a11a-372">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a11a-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5a11a-373">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5a11a-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5a11a-374">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="5a11a-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5a11a-375">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="5a11a-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a11a-376">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5a11a-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5a11a-377">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="5a11a-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5a11a-378">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="5a11a-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5a11a-379">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="5a11a-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5a11a-380">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="5a11a-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5a11a-381">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="5a11a-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5a11a-382">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="5a11a-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5a11a-383">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="5a11a-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5a11a-384">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="5a11a-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a11a-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5a11a-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-386">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-388">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a11a-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-389">Identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5a11a-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="5a11a-390">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="5a11a-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="5a11a-391">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="5a11a-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="5a11a-392">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="5a11a-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="5a11a-393">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="5a11a-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="5a11a-394">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="5a11a-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="5a11a-395">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-396">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a11a-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-397">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5a11a-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-399">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ chassis**.**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="5a11a-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-400">Matrice di stringhe in formato libero che fornisce informazioni sulle voci della matrice **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="5a11a-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="5a11a-401">Ogni voce della matrice è correlata alla voce nella proprietà **ChassisTypes** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="5a11a-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a11a-402">**Versione**</span><span class="sxs-lookup"><span data-stu-id="5a11a-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a11a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-405">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5a11a-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-406">Indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5a11a-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="5a11a-407">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-408">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="5a11a-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-409">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5a11a-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-411">Se **true**, l'apparecchiatura include un allarme visibile.</span><span class="sxs-lookup"><span data-stu-id="5a11a-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="5a11a-412">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-413">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5a11a-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-414">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5a11a-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-416">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="5a11a-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-417">Peso del pacchetto fisico, in sterline.</span><span class="sxs-lookup"><span data-stu-id="5a11a-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="5a11a-418">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a11a-419">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="5a11a-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a11a-420">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5a11a-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a11a-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a11a-422">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="5a11a-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5a11a-423">Larghezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="5a11a-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="5a11a-424">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a11a-425">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a11a-425">Remarks</span></span>

<span data-ttu-id="5a11a-426">La classe **CIM \_ chassis** è derivata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="5a11a-427">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5a11a-427">WMI does not implement this class.</span></span> <span data-ttu-id="5a11a-428">Per ulteriori informazioni sulle classi derivate dallo **\_ chassis CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5a11a-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5a11a-429">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5a11a-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5a11a-430">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5a11a-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a11a-431">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a11a-431">Requirements</span></span>



| <span data-ttu-id="5a11a-432">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a11a-432">Requirement</span></span> | <span data-ttu-id="5a11a-433">Valore</span><span class="sxs-lookup"><span data-stu-id="5a11a-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a11a-434">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a11a-434">Minimum supported client</span></span><br/> | <span data-ttu-id="5a11a-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a11a-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a11a-436">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a11a-436">Minimum supported server</span></span><br/> | <span data-ttu-id="5a11a-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a11a-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a11a-438">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a11a-438">Namespace</span></span><br/>                | <span data-ttu-id="5a11a-439">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5a11a-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5a11a-440">MOF</span><span class="sxs-lookup"><span data-stu-id="5a11a-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a11a-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a11a-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a11a-442">DLL</span><span class="sxs-lookup"><span data-stu-id="5a11a-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a11a-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a11a-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a11a-444">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a11a-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a11a-445">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="5a11a-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

