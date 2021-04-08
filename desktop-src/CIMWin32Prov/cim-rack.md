---
description: La \_ classe CIM rack rappresenta un rack (un frame fisico o un'enclosure) in cui vengono archiviati gli chassis. In genere, un rack rappresenta l'enclosure; tutti i componenti funzionanti sono inclusi nello chassis.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: Classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748234"
---
# <a name="cim_rack-class"></a><span data-ttu-id="8f3da-104">\_Classe CIM rack</span><span class="sxs-lookup"><span data-stu-id="8f3da-104">CIM\_Rack class</span></span>

<span data-ttu-id="8f3da-105">La classe **CIM \_ rack** rappresenta un rack (un frame fisico o un'enclosure) in cui vengono archiviati gli chassis.</span><span class="sxs-lookup"><span data-stu-id="8f3da-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="8f3da-106">In genere, un rack rappresenta l'enclosure; tutti i componenti funzionanti sono inclusi nello chassis.</span><span class="sxs-lookup"><span data-stu-id="8f3da-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f3da-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8f3da-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f3da-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f3da-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f3da-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8f3da-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8f3da-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8f3da-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3da-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f3da-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="8f3da-112">Members</span><span class="sxs-lookup"><span data-stu-id="8f3da-112">Members</span></span>

<span data-ttu-id="8f3da-113">La classe **CIM \_ rack** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8f3da-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="8f3da-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="8f3da-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f3da-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f3da-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f3da-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="8f3da-116">Methods</span></span>

<span data-ttu-id="8f3da-117">La classe **CIM \_ rack** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8f3da-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="8f3da-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="8f3da-118">Method</span></span>                                                        | <span data-ttu-id="8f3da-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f3da-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f3da-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="8f3da-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="8f3da-121">Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="8f3da-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="8f3da-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8f3da-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8f3da-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f3da-123">Properties</span></span>

<span data-ttu-id="8f3da-124">La classe **CIM \_ rack** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8f3da-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f3da-125">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="8f3da-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-128">Se **true**, il frame è dotato di un allarme acustico.</span><span class="sxs-lookup"><span data-stu-id="8f3da-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="8f3da-129">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-130">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="8f3da-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-133">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="8f3da-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-134">Stringa in formato libero che fornisce informazioni se la proprietà **SecurityBreach** indica che si è verificata una violazione o un altro evento correlato alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8f3da-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="8f3da-135">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-136">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="8f3da-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-139">Stringa in formato libero che contiene informazioni sul modo in cui i vari cavi sono connessi e in bundle per il frame.</span><span class="sxs-lookup"><span data-stu-id="8f3da-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="8f3da-140">Con molti cavi di rete, correlati all'archiviazione e di alimentazione, la gestione dei cavi può essere un'attività complessa e impegnativa.</span><span class="sxs-lookup"><span data-stu-id="8f3da-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="8f3da-141">Questa proprietà di stringa contiene informazioni per facilitare l'assembly e il servizio del frame.</span><span class="sxs-lookup"><span data-stu-id="8f3da-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="8f3da-142">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-143">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8f3da-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-146">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8f3da-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-147">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-147">Short textual description of the object.</span></span>

<span data-ttu-id="8f3da-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-149">**CountryDesignation**</span><span class="sxs-lookup"><span data-stu-id="8f3da-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-152">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ rack**.**TypeOfRack**")</span><span class="sxs-lookup"><span data-stu-id="8f3da-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-153">Paese o area geografica per cui è progettato il rack.</span><span class="sxs-lookup"><span data-stu-id="8f3da-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="8f3da-154">Le stringhe di codice paese o area geografica sono definite da ISO/IEC 3166.</span><span class="sxs-lookup"><span data-stu-id="8f3da-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="8f3da-155">Il tipo di rack è specificato nella proprietà **TypeOfRack** .</span><span class="sxs-lookup"><span data-stu-id="8f3da-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f3da-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-159">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f3da-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-160">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="8f3da-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8f3da-161">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="8f3da-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8f3da-162">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-163">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="8f3da-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-164">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="8f3da-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-166">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="8f3da-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-167">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="8f3da-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="8f3da-168">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-169">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8f3da-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-172">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8f3da-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-173">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-173">Textual description of the object.</span></span>

<span data-ttu-id="8f3da-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-175">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="8f3da-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-176">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="8f3da-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-178">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("height"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="8f3da-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-179">Altezza del pacchetto fisico, usando l'unità di misura "U".</span><span class="sxs-lookup"><span data-stu-id="8f3da-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="8f3da-180">Un "U" è un'unità di misura standard per l'altezza di un rack o un componente montabile su rack ed è uguale a 1,75 centimetri o 4,445 centimetri.</span><span class="sxs-lookup"><span data-stu-id="8f3da-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="8f3da-181">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-182">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="8f3da-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-183">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-185">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="8f3da-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="8f3da-186">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="8f3da-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="8f3da-187">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="8f3da-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="8f3da-188">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="8f3da-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="8f3da-189">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f3da-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-191">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f3da-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-193">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="8f3da-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-194">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-194">Date and time the object was installed.</span></span> <span data-ttu-id="8f3da-195">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="8f3da-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8f3da-196">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-197">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="8f3da-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-198">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-200">Se **true**, il frame è protetto con un blocco.</span><span class="sxs-lookup"><span data-stu-id="8f3da-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="8f3da-201">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-202">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="8f3da-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-205">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f3da-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-206">Nome dell'organizzazione che ha prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="8f3da-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="8f3da-207">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="8f3da-208">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-209">**Modello**</span><span class="sxs-lookup"><span data-stu-id="8f3da-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-212">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f3da-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-213">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="8f3da-214">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-215">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8f3da-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-218">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8f3da-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-219">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-219">Label by which the object is known.</span></span> <span data-ttu-id="8f3da-220">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="8f3da-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8f3da-221">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8f3da-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-225">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="8f3da-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="8f3da-226">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="8f3da-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="8f3da-227">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f3da-228">Se sono disponibili solo dati del codice a barre e è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="8f3da-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="8f3da-229">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="8f3da-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-232">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f3da-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-233">Numero di parte assegnato dall'organizzazione che ha prodotto o prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="8f3da-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="8f3da-234">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-235">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="8f3da-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-236">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-238">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="8f3da-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="8f3da-239">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-240">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="8f3da-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-241">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-243">Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8f3da-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="8f3da-244">Un pacchetto viene considerato rimovibile anche se la potenza deve essere "off" per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="8f3da-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="8f3da-245">Se la potenza può essere "on" e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="8f3da-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="8f3da-246">Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando i connettori SCA; Tuttavia, quest'ultimo può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="8f3da-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="8f3da-247">Il display di un portatile non è rimovibile, né è un alimentatore non ridondante.</span><span class="sxs-lookup"><span data-stu-id="8f3da-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="8f3da-248">La rimozione di questi componenti influisca sulla funzione della creazione complessiva dei pacchetti oppure è impossibile grazie alla stretta integrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="8f3da-249">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-250">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="8f3da-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-251">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-253">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="8f3da-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="8f3da-254">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="8f3da-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="8f3da-255">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="8f3da-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="8f3da-256">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="8f3da-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="8f3da-257">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-258">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="8f3da-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-259">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f3da-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-261">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="8f3da-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-262">Indica se una violazione fisica del frame è stata tentata, ma non è stata completata, oppure se è stata tentata e riuscita.</span><span class="sxs-lookup"><span data-stu-id="8f3da-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="8f3da-263">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f3da-264">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8f3da-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f3da-265">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="8f3da-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="8f3da-266">**Nessuna violazione** (3)</span><span class="sxs-lookup"><span data-stu-id="8f3da-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="8f3da-267">**Tentativo di violazione** (4)</span><span class="sxs-lookup"><span data-stu-id="8f3da-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="8f3da-268">**Violazione riuscita** (5)</span><span class="sxs-lookup"><span data-stu-id="8f3da-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f3da-269">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8f3da-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-272">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f3da-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-273">Numero allocato dal produttore utilizzato per identificare il rack.</span><span class="sxs-lookup"><span data-stu-id="8f3da-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="8f3da-274">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-275">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8f3da-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-276">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8f3da-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-278">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="8f3da-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-279">Stringhe in formato libero che forniscono spiegazioni dettagliate per le voci nella matrice **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="8f3da-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="8f3da-280">Si noti che ogni voce della matrice è correlata alla voce in **ServicePhilosophy** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="8f3da-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="8f3da-281">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-282">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="8f3da-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-283">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f3da-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-285">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8f3da-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-286">Indica se il frame viene servito dalla parte superiore, anteriore, posteriore o laterale; e se sono presenti vassoi scorrevoli o lati rimovibili e se il frame è mobile (ad esempio, con i Roller).</span><span class="sxs-lookup"><span data-stu-id="8f3da-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="8f3da-287">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f3da-288">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8f3da-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f3da-289">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8f3da-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="8f3da-290">**Servizio dall'inizio** (2)</span><span class="sxs-lookup"><span data-stu-id="8f3da-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="8f3da-291">**Servizio dall'inizio** (3)</span><span class="sxs-lookup"><span data-stu-id="8f3da-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="8f3da-292">**Servizio da indietro** (4)</span><span class="sxs-lookup"><span data-stu-id="8f3da-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="8f3da-293">**Servizio dal lato** (5)</span><span class="sxs-lookup"><span data-stu-id="8f3da-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="8f3da-294">**Vassoi scorrevoli** (6)</span><span class="sxs-lookup"><span data-stu-id="8f3da-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="8f3da-295">**Lati rimovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="8f3da-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="8f3da-296">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="8f3da-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f3da-297">**SKU**</span><span class="sxs-lookup"><span data-stu-id="8f3da-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-300">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f3da-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-301">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="8f3da-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="8f3da-302">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-303">**Status**</span><span class="sxs-lookup"><span data-stu-id="8f3da-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-306">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8f3da-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-307">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f3da-307">Current status of the object.</span></span> <span data-ttu-id="8f3da-308">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8f3da-309">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f3da-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8f3da-310">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8f3da-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8f3da-311">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="8f3da-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8f3da-312">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="8f3da-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f3da-313">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="8f3da-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8f3da-314">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="8f3da-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8f3da-315">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="8f3da-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8f3da-316">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="8f3da-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8f3da-317">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="8f3da-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8f3da-318">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="8f3da-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8f3da-319">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="8f3da-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8f3da-320">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="8f3da-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8f3da-321">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="8f3da-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f3da-322">**Tag**</span><span class="sxs-lookup"><span data-stu-id="8f3da-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-325">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f3da-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-326">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f3da-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="8f3da-327">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="8f3da-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="8f3da-328">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="8f3da-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="8f3da-329">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="8f3da-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="8f3da-330">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="8f3da-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="8f3da-331">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8f3da-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="8f3da-332">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-333">**TypeOfRack**</span><span class="sxs-lookup"><span data-stu-id="8f3da-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-334">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f3da-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-336">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ rack**.**CountryDesignation**")</span><span class="sxs-lookup"><span data-stu-id="8f3da-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-337">Tipo di rack.</span><span class="sxs-lookup"><span data-stu-id="8f3da-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f3da-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8f3da-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="8f3da-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**19 pollici standard** (1)</span><span class="sxs-lookup"><span data-stu-id="8f3da-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f3da-340">Standard da 19 pollici</span><span class="sxs-lookup"><span data-stu-id="8f3da-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="8f3da-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span><span class="sxs-lookup"><span data-stu-id="8f3da-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="8f3da-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Scaffale attrezzature** (3)</span><span class="sxs-lookup"><span data-stu-id="8f3da-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="8f3da-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non standard** (4)</span><span class="sxs-lookup"><span data-stu-id="8f3da-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f3da-344">**Versione**</span><span class="sxs-lookup"><span data-stu-id="8f3da-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f3da-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-347">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f3da-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-348">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="8f3da-348">Version of the physical element.</span></span>

<span data-ttu-id="8f3da-349">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-350">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="8f3da-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-351">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f3da-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-353">Se **true**, l'apparecchiatura include un allarme visibile.</span><span class="sxs-lookup"><span data-stu-id="8f3da-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="8f3da-354">Questa proprietà viene ereditata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-355">**Weight**</span><span class="sxs-lookup"><span data-stu-id="8f3da-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-356">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="8f3da-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-358">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="8f3da-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-359">Peso del pacchetto fisico, in sterline.</span><span class="sxs-lookup"><span data-stu-id="8f3da-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="8f3da-360">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f3da-361">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="8f3da-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3da-362">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="8f3da-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f3da-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3da-364">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="8f3da-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="8f3da-365">Larghezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="8f3da-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="8f3da-366">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f3da-367">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f3da-367">Remarks</span></span>

<span data-ttu-id="8f3da-368">La classe **CIM \_ rack** è derivata da [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8f3da-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="8f3da-369">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="8f3da-369">WMI does not implement this class.</span></span>

<span data-ttu-id="8f3da-370">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f3da-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f3da-371">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8f3da-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3da-372">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f3da-372">Requirements</span></span>



| <span data-ttu-id="8f3da-373">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3da-373">Requirement</span></span> | <span data-ttu-id="8f3da-374">Valore</span><span class="sxs-lookup"><span data-stu-id="8f3da-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3da-375">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f3da-375">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3da-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f3da-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f3da-377">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f3da-377">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3da-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f3da-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f3da-379">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f3da-379">Namespace</span></span><br/>                | <span data-ttu-id="8f3da-380">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8f3da-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f3da-381">MOF</span><span class="sxs-lookup"><span data-stu-id="8f3da-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f3da-382"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f3da-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f3da-383">DLL</span><span class="sxs-lookup"><span data-stu-id="8f3da-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f3da-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f3da-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f3da-385">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f3da-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3da-386">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="8f3da-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

