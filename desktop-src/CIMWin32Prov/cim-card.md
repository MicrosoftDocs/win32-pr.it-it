---
description: La \_ classe CIM rappresenta un tipo di contenitore fisico che può essere inserito in un'altra scheda o lavagna host oppure è una lavagna di hosting/scheda madre in uno chassis.
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: Classe CIM_Card
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304983"
---
# <a name="cim_card-class"></a><span data-ttu-id="f8267-103">\_Classe CIM card</span><span class="sxs-lookup"><span data-stu-id="f8267-103">CIM\_Card class</span></span>

<span data-ttu-id="f8267-104">La **classe \_ CIM** rappresenta un tipo di contenitore fisico che può essere inserito in un'altra scheda o lavagna host oppure è una lavagna di hosting/scheda madre in uno chassis.</span><span class="sxs-lookup"><span data-stu-id="f8267-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="f8267-105">Questa classe include tutti i pacchetti in grado di trasportare segnali e fornire un punto di montaggio per i componenti fisici, ad esempio chip o altri pacchetti fisici, ad esempio altre schede.</span><span class="sxs-lookup"><span data-stu-id="f8267-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8267-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f8267-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8267-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8267-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f8267-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f8267-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f8267-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f8267-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8267-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8267-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
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
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="f8267-111">Members</span><span class="sxs-lookup"><span data-stu-id="f8267-111">Members</span></span>

<span data-ttu-id="f8267-112">La classe **CIM \_ Card** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8267-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="f8267-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f8267-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f8267-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8267-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f8267-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="f8267-115">Methods</span></span>

<span data-ttu-id="f8267-116">La classe **CIM \_ Card** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f8267-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="f8267-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="f8267-117">Method</span></span>                                                        | <span data-ttu-id="f8267-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8267-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8267-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="f8267-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="f8267-120">Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="f8267-121">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f8267-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f8267-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8267-122">Properties</span></span>

<span data-ttu-id="f8267-123">La classe **CIM \_ Card** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8267-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8267-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f8267-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f8267-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-128">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8267-128">A short textual description of the object.</span></span>

<span data-ttu-id="f8267-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f8267-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-133">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f8267-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-134">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f8267-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f8267-135">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f8267-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f8267-136">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-137">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="f8267-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-138">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="f8267-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-140">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="f8267-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-141">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="f8267-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="f8267-142">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-143">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f8267-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-146">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f8267-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-147">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8267-147">A textual description of the object.</span></span>

<span data-ttu-id="f8267-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-149">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="f8267-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-150">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="f8267-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-152">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="f8267-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-153">Altezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="f8267-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="f8267-154">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-155">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="f8267-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-156">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-158">Se **true**, questa scheda è una scheda madre o, in modo più generico, un battiscopa in uno chassis.</span><span class="sxs-lookup"><span data-stu-id="f8267-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="f8267-159">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="f8267-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-160">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-162">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="f8267-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f8267-163">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="f8267-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f8267-164">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="f8267-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f8267-165">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="f8267-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f8267-166">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8267-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-168">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8267-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-170">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="f8267-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-171">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="f8267-171">Indicates when the object was installed.</span></span> <span data-ttu-id="f8267-172">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="f8267-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f8267-173">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-174">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="f8267-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-177">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f8267-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-178">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="f8267-179">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f8267-180">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-181">**Modello**</span><span class="sxs-lookup"><span data-stu-id="f8267-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-184">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f8267-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-185">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="f8267-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f8267-186">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-187">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f8267-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-190">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f8267-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-191">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f8267-191">Label by which the object is known.</span></span> <span data-ttu-id="f8267-192">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f8267-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f8267-193">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f8267-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-197">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="f8267-198">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="f8267-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="f8267-199">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="f8267-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="f8267-200">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-201">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="f8267-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-204">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f8267-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-205">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="f8267-206">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-207">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="f8267-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-208">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-210">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="f8267-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="f8267-211">In caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="f8267-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="f8267-212">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-213">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="f8267-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-214">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-216">Se **true**, il pacchetto è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f8267-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f8267-217">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="f8267-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="f8267-218">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="f8267-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f8267-219">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="f8267-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="f8267-220">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-221">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="f8267-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-222">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-224">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="f8267-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f8267-225">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="f8267-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f8267-226">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="f8267-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f8267-227">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="f8267-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f8267-228">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-229">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="f8267-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-232">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Card**.**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="f8267-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-233">Stringa in formato libero che descrive il modo in cui la scheda è fisicamente univoca da altre schede.</span><span class="sxs-lookup"><span data-stu-id="f8267-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="f8267-234">Questa proprietà ha un significato solo quando la proprietà booleana corrispondente, **SpecialRequirements**, è impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="f8267-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="f8267-235">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="f8267-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-236">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-238">Se **true**, per il corretto funzionamento è necessario almeno un daughterboard o una scheda ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="f8267-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="f8267-239">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f8267-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-242">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f8267-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-243">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="f8267-244">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-245">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f8267-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-248">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f8267-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-249">Numero di unità di conservazione per questo elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="f8267-250">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-251">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="f8267-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8267-254">Stringa in formato libero che descrive il posizionamento degli slot, l'utilizzo tipico, le restrizioni, le spaziatura dei singoli slot o altre informazioni pertinenti per gli slot in una scheda.</span><span class="sxs-lookup"><span data-stu-id="f8267-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="f8267-255">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="f8267-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-256">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8267-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-258">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Card**.**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="f8267-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-259">Se **true**, la scheda è fisicamente univoca rispetto ad altre schede dello stesso tipo e, pertanto, richiede uno slot speciale.</span><span class="sxs-lookup"><span data-stu-id="f8267-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="f8267-260">Una scheda a doppia larghezza, ad esempio, richiede due slot.</span><span class="sxs-lookup"><span data-stu-id="f8267-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="f8267-261">Un altro esempio è quando una determinata scheda può essere usata per la stessa funzione generale di altre schede, ma richiede uno slot speciale (ad esempio, molto lungo); mentre altre schede possono essere inserite in qualsiasi slot disponibile.</span><span class="sxs-lookup"><span data-stu-id="f8267-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="f8267-262">Se **true**, la proprietà **RequirementsDescription** corrispondente deve specificare la natura dell'unicità o lo scopo della scheda.</span><span class="sxs-lookup"><span data-stu-id="f8267-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="f8267-263">**Status**</span><span class="sxs-lookup"><span data-stu-id="f8267-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-266">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f8267-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-267">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8267-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="f8267-268">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="f8267-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f8267-269">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="f8267-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f8267-270">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="f8267-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f8267-271">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f8267-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f8267-272">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f8267-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f8267-273">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f8267-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f8267-274">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f8267-275">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8267-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f8267-276">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f8267-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f8267-277">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="f8267-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f8267-278">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="f8267-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f8267-279">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f8267-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f8267-280">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="f8267-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f8267-281">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="f8267-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f8267-282">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="f8267-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f8267-283">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="f8267-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f8267-284">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="f8267-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f8267-285">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="f8267-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f8267-286">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="f8267-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f8267-287">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="f8267-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f8267-288">**Tag**</span><span class="sxs-lookup"><span data-stu-id="f8267-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-291">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f8267-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-292">Identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f8267-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f8267-293">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="f8267-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f8267-294">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="f8267-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f8267-295">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="f8267-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f8267-296">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="f8267-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f8267-297">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="f8267-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f8267-298">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-299">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f8267-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8267-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-302">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f8267-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8267-303">Indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f8267-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="f8267-304">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-305">**Weight**</span><span class="sxs-lookup"><span data-stu-id="f8267-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-306">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="f8267-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-308">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="f8267-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-309">Peso del pacchetto fisico, in sterline.</span><span class="sxs-lookup"><span data-stu-id="f8267-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="f8267-310">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8267-311">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="f8267-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8267-312">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="f8267-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f8267-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8267-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8267-314">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="f8267-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f8267-315">Larghezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="f8267-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="f8267-316">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8267-317">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8267-317">Remarks</span></span>

<span data-ttu-id="f8267-318">La classe **CIM \_ Card** è derivata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="f8267-319">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f8267-319">WMI does not implement this class.</span></span> <span data-ttu-id="f8267-320">Per ulteriori informazioni sulle classi derivate dalla **\_ scheda CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f8267-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f8267-321">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8267-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8267-322">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f8267-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8267-323">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8267-323">Requirements</span></span>



| <span data-ttu-id="f8267-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8267-324">Requirement</span></span> | <span data-ttu-id="f8267-325">Valore</span><span class="sxs-lookup"><span data-stu-id="f8267-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8267-326">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8267-326">Minimum supported client</span></span><br/> | <span data-ttu-id="f8267-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8267-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8267-328">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8267-328">Minimum supported server</span></span><br/> | <span data-ttu-id="f8267-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8267-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8267-330">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8267-330">Namespace</span></span><br/>                | <span data-ttu-id="f8267-331">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f8267-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8267-332">MOF</span><span class="sxs-lookup"><span data-stu-id="f8267-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8267-333"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8267-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8267-334">DLL</span><span class="sxs-lookup"><span data-stu-id="f8267-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8267-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8267-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8267-336">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8267-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8267-337">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="f8267-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

