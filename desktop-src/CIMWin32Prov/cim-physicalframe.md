---
description: La \_ classe CIM PhysicalFrame è una classe padre di rack, chassis e altre enclosure di frame così come sono definiti nelle classi di estensione.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: Classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127382"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="6d70e-103">CIM \_ PhysicalFrame (classe)</span><span class="sxs-lookup"><span data-stu-id="6d70e-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="6d70e-104">La classe **CIM \_ PhysicalFrame** è una classe padre di rack, chassis e altre enclosure di frame così come sono definiti nelle classi di estensione.</span><span class="sxs-lookup"><span data-stu-id="6d70e-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="6d70e-105">In questa classe padre sono incluse proprietà quali **VisibleAlarm** e **AudibleAlarm** e i dati relativi alle violazioni della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6d70e-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d70e-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6d70e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6d70e-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6d70e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6d70e-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6d70e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6d70e-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6d70e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d70e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d70e-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
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
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="6d70e-111">Members</span><span class="sxs-lookup"><span data-stu-id="6d70e-111">Members</span></span>

<span data-ttu-id="6d70e-112">La classe **CIM \_ PhysicalFrame** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6d70e-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="6d70e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="6d70e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="6d70e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d70e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6d70e-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="6d70e-115">Methods</span></span>

<span data-ttu-id="6d70e-116">La classe **CIM \_ PhysicalFrame** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6d70e-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="6d70e-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="6d70e-117">Method</span></span>                                                                 | <span data-ttu-id="6d70e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d70e-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d70e-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="6d70e-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="6d70e-120">Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="6d70e-121">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="6d70e-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6d70e-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d70e-122">Properties</span></span>

<span data-ttu-id="6d70e-123">La classe **CIM \_ PhysicalFrame** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d70e-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d70e-124">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="6d70e-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-125">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-127">Se **true**, il frame è dotato di un allarme acustico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="6d70e-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="6d70e-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-132">Stringa in formato libero che fornisce ulteriori informazioni se la proprietà **SecurityBreach** indica che si è verificata una violazione o un altro evento correlato alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6d70e-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-133">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="6d70e-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-136">Stringa in formato libero che contiene informazioni sul modo in cui i vari cavi sono connessi e in bundle per il frame.</span><span class="sxs-lookup"><span data-stu-id="6d70e-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="6d70e-137">Con molti cavi di rete, correlati all'archiviazione e di alimentazione, la gestione dei cavi può essere un'attività complessa e impegnativa.</span><span class="sxs-lookup"><span data-stu-id="6d70e-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="6d70e-138">Questa proprietà di stringa contiene informazioni per facilitare l'assembly e il servizio del frame.</span><span class="sxs-lookup"><span data-stu-id="6d70e-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6d70e-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-142">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6d70e-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-143">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d70e-143">Short textual description of the object.</span></span>

<span data-ttu-id="6d70e-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6d70e-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-148">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6d70e-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-149">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="6d70e-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6d70e-150">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="6d70e-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6d70e-151">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-152">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="6d70e-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-153">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="6d70e-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-155">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="6d70e-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-156">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="6d70e-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="6d70e-157">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-158">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6d70e-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-161">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6d70e-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-162">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d70e-162">Textual description of the object.</span></span>

<span data-ttu-id="6d70e-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-164">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="6d70e-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-165">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="6d70e-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-167">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="6d70e-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-168">Altezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="6d70e-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="6d70e-169">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-170">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="6d70e-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-171">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-173">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="6d70e-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="6d70e-174">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="6d70e-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="6d70e-175">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="6d70e-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="6d70e-176">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="6d70e-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="6d70e-177">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6d70e-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-179">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6d70e-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-181">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="6d70e-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-182">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d70e-182">Date and time the object was installed.</span></span> <span data-ttu-id="6d70e-183">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="6d70e-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6d70e-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-185">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="6d70e-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-186">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-188">Se **true**, il frame è protetto con un blocco.</span><span class="sxs-lookup"><span data-stu-id="6d70e-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-189">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="6d70e-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-192">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6d70e-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-193">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="6d70e-194">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="6d70e-195">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-196">**Modello**</span><span class="sxs-lookup"><span data-stu-id="6d70e-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-199">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6d70e-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-200">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="6d70e-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="6d70e-201">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-202">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6d70e-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-205">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6d70e-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-206">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="6d70e-206">Label by which the object is known.</span></span> <span data-ttu-id="6d70e-207">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="6d70e-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6d70e-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6d70e-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-212">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="6d70e-213">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="6d70e-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="6d70e-214">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="6d70e-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="6d70e-215">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-216">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="6d70e-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-219">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6d70e-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-220">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="6d70e-221">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-222">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="6d70e-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-223">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-225">Se **true**, l'elemento fisico è acceso; in caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="6d70e-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="6d70e-226">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-227">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="6d70e-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-228">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-230">Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6d70e-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="6d70e-231">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="6d70e-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="6d70e-232">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="6d70e-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="6d70e-233">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="6d70e-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="6d70e-234">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-235">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="6d70e-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-236">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-238">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="6d70e-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="6d70e-239">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="6d70e-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="6d70e-240">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="6d70e-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="6d70e-241">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="6d70e-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="6d70e-242">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-243">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="6d70e-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6d70e-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-246">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="6d70e-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-247">Indica se una violazione fisica del frame è stata tentata, ma non è stata completata, oppure se è stata tentata e riuscita.</span><span class="sxs-lookup"><span data-stu-id="6d70e-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6d70e-248">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6d70e-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6d70e-249">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="6d70e-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="6d70e-250">**Nessuna violazione** (3)</span><span class="sxs-lookup"><span data-stu-id="6d70e-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="6d70e-251">**Tentativo di violazione** (4)</span><span class="sxs-lookup"><span data-stu-id="6d70e-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="6d70e-252">**Violazione riuscita** (5)</span><span class="sxs-lookup"><span data-stu-id="6d70e-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d70e-253">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="6d70e-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-256">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6d70e-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-257">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="6d70e-258">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-259">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6d70e-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-260">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6d70e-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-262">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="6d70e-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-263">Stringhe in formato libero che forniscono spiegazioni dettagliate per le voci nella matrice **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="6d70e-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="6d70e-264">Ogni voce di questa matrice è correlata alla voce nella matrice **ServicePhilosophy** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="6d70e-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="6d70e-265">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="6d70e-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-266">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6d70e-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-268">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="6d70e-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-269">Indica se il frame viene servito dalla parte superiore, anteriore, posteriore o laterale; e se sono presenti vassoi scorrevoli o lati rimovibili e se il frame è mobile (ad esempio, con i Roller).</span><span class="sxs-lookup"><span data-stu-id="6d70e-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6d70e-270">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6d70e-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6d70e-271">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6d70e-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="6d70e-272">**Servizio dall'inizio** (2)</span><span class="sxs-lookup"><span data-stu-id="6d70e-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="6d70e-273">**Servizio dall'inizio** (3)</span><span class="sxs-lookup"><span data-stu-id="6d70e-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="6d70e-274">**Servizio da indietro** (4)</span><span class="sxs-lookup"><span data-stu-id="6d70e-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="6d70e-275">**Servizio dal lato** (5)</span><span class="sxs-lookup"><span data-stu-id="6d70e-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="6d70e-276">**Vassoi scorrevoli** (6)</span><span class="sxs-lookup"><span data-stu-id="6d70e-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="6d70e-277">**Lati rimovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="6d70e-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="6d70e-278">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="6d70e-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d70e-279">**SKU**</span><span class="sxs-lookup"><span data-stu-id="6d70e-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-282">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6d70e-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-283">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="6d70e-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="6d70e-284">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-285">**Status**</span><span class="sxs-lookup"><span data-stu-id="6d70e-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-288">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6d70e-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-289">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d70e-289">Current status of the object.</span></span>

<span data-ttu-id="6d70e-290">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6d70e-291">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d70e-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6d70e-292">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6d70e-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6d70e-293">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="6d70e-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6d70e-294">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="6d70e-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6d70e-295">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="6d70e-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6d70e-296">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="6d70e-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6d70e-297">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="6d70e-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6d70e-298">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="6d70e-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6d70e-299">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="6d70e-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6d70e-300">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="6d70e-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6d70e-301">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="6d70e-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6d70e-302">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="6d70e-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6d70e-303">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="6d70e-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d70e-304">**Tag**</span><span class="sxs-lookup"><span data-stu-id="6d70e-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-307">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6d70e-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-308">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6d70e-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="6d70e-309">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="6d70e-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="6d70e-310">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="6d70e-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="6d70e-311">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="6d70e-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="6d70e-312">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="6d70e-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="6d70e-313">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="6d70e-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="6d70e-314">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-315">**Versione**</span><span class="sxs-lookup"><span data-stu-id="6d70e-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d70e-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-318">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6d70e-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-319">Stringa che indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="6d70e-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="6d70e-320">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-321">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="6d70e-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-322">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d70e-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-324">Se **true**, l'apparecchiatura include un allarme visibile.</span><span class="sxs-lookup"><span data-stu-id="6d70e-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-325">**Weight**</span><span class="sxs-lookup"><span data-stu-id="6d70e-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-326">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="6d70e-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-328">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="6d70e-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-329">Peso del pacchetto fisico, in sterline.</span><span class="sxs-lookup"><span data-stu-id="6d70e-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="6d70e-330">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d70e-331">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="6d70e-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d70e-332">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="6d70e-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d70e-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d70e-334">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="6d70e-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="6d70e-335">Larghezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="6d70e-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="6d70e-336">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d70e-337">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d70e-337">Remarks</span></span>

<span data-ttu-id="6d70e-338">La classe **CIM \_ PhysicalFrame** è derivata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="6d70e-339">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6d70e-339">WMI does not implement this class.</span></span> <span data-ttu-id="6d70e-340">Per le classi WMI derivate da **CIM \_ PhysicalFrame**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6d70e-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6d70e-341">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6d70e-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6d70e-342">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6d70e-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d70e-343">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d70e-343">Requirements</span></span>



| <span data-ttu-id="6d70e-344">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d70e-344">Requirement</span></span> | <span data-ttu-id="6d70e-345">Valore</span><span class="sxs-lookup"><span data-stu-id="6d70e-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d70e-346">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d70e-346">Minimum supported client</span></span><br/> | <span data-ttu-id="6d70e-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d70e-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d70e-348">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d70e-348">Minimum supported server</span></span><br/> | <span data-ttu-id="6d70e-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d70e-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d70e-350">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d70e-350">Namespace</span></span><br/>                | <span data-ttu-id="6d70e-351">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6d70e-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d70e-352">MOF</span><span class="sxs-lookup"><span data-stu-id="6d70e-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d70e-353"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d70e-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d70e-354">DLL</span><span class="sxs-lookup"><span data-stu-id="6d70e-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d70e-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d70e-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d70e-356">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d70e-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d70e-357">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="6d70e-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

