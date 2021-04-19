---
description: La \_ classe CIM PhysicalPackage rappresenta elementi fisici che contengono o ospitano altri componenti. Gli esempi sono un'enclosure rack o una scheda scheda.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: Classe CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305108"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="630c0-104">CIM \_ PhysicalPackage (classe)</span><span class="sxs-lookup"><span data-stu-id="630c0-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="630c0-105">La classe **CIM \_ PhysicalPackage** rappresenta elementi fisici che contengono o ospitano altri componenti.</span><span class="sxs-lookup"><span data-stu-id="630c0-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="630c0-106">Gli esempi sono un'enclosure rack o una scheda scheda.</span><span class="sxs-lookup"><span data-stu-id="630c0-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="630c0-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="630c0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="630c0-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="630c0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="630c0-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="630c0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="630c0-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="630c0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="630c0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="630c0-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="630c0-112">Members</span><span class="sxs-lookup"><span data-stu-id="630c0-112">Members</span></span>

<span data-ttu-id="630c0-113">La classe **CIM \_ PhysicalPackage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="630c0-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="630c0-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="630c0-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="630c0-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="630c0-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="630c0-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="630c0-116">Methods</span></span>

<span data-ttu-id="630c0-117">La classe **CIM \_ PhysicalPackage** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="630c0-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="630c0-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="630c0-118">Method</span></span>                                                                   | <span data-ttu-id="630c0-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="630c0-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="630c0-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="630c0-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="630c0-121">Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="630c0-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="630c0-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="630c0-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="630c0-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="630c0-123">Properties</span></span>

<span data-ttu-id="630c0-124">La classe **CIM \_ PhysicalPackage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="630c0-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="630c0-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="630c0-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-128">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="630c0-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-129">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="630c0-129">Short textual description of the object.</span></span>

<span data-ttu-id="630c0-130">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="630c0-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-134">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="630c0-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-135">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="630c0-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="630c0-136">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="630c0-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="630c0-137">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-138">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="630c0-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-139">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="630c0-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-141">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="630c0-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-142">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="630c0-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="630c0-143">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="630c0-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-146">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="630c0-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-147">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="630c0-147">Textual description of the object.</span></span>

<span data-ttu-id="630c0-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-149">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="630c0-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-150">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="630c0-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-152">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="630c0-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-153">Altezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="630c0-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="630c0-154">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="630c0-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-155">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="630c0-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="630c0-157">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="630c0-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="630c0-158">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="630c0-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="630c0-159">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="630c0-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="630c0-160">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="630c0-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="630c0-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="630c0-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-162">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="630c0-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-164">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="630c0-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-165">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="630c0-165">Date and time the object was installed.</span></span> <span data-ttu-id="630c0-166">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="630c0-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="630c0-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-168">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="630c0-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-171">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="630c0-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-172">Nome dell'organizzazione che ha prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="630c0-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="630c0-173">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="630c0-174">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-175">**Modello**</span><span class="sxs-lookup"><span data-stu-id="630c0-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-178">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="630c0-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-179">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="630c0-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="630c0-180">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-181">**Nome**</span><span class="sxs-lookup"><span data-stu-id="630c0-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-184">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="630c0-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-185">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="630c0-185">Label by which the object is known.</span></span> <span data-ttu-id="630c0-186">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="630c0-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="630c0-187">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="630c0-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="630c0-191">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="630c0-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="630c0-192">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="630c0-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="630c0-193">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="630c0-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="630c0-194">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-195">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="630c0-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-198">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="630c0-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-199">Numero di parte assegnato dall'organizzazione che ha prodotto o prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="630c0-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="630c0-200">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-201">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="630c0-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-202">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="630c0-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="630c0-204">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="630c0-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="630c0-205">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-206">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="630c0-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-207">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="630c0-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="630c0-209">Se **true**, il pacchetto è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="630c0-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="630c0-210">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="630c0-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="630c0-211">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="630c0-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="630c0-212">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="630c0-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="630c0-213">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="630c0-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-214">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="630c0-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="630c0-216">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="630c0-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="630c0-217">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="630c0-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="630c0-218">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="630c0-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="630c0-219">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="630c0-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="630c0-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="630c0-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-223">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="630c0-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-224">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="630c0-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="630c0-225">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="630c0-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-229">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="630c0-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-230">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="630c0-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="630c0-231">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-232">**Status**</span><span class="sxs-lookup"><span data-stu-id="630c0-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-235">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="630c0-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-236">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="630c0-236">Current status of the object.</span></span>

<span data-ttu-id="630c0-237">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="630c0-238">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="630c0-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="630c0-239">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="630c0-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="630c0-240">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="630c0-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="630c0-241">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="630c0-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="630c0-242">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="630c0-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="630c0-243">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="630c0-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="630c0-244">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="630c0-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="630c0-245">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="630c0-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="630c0-246">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="630c0-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="630c0-247">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="630c0-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="630c0-248">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="630c0-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="630c0-249">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="630c0-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="630c0-250">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="630c0-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="630c0-251">**Tag**</span><span class="sxs-lookup"><span data-stu-id="630c0-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-254">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="630c0-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-255">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="630c0-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="630c0-256">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="630c0-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="630c0-257">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="630c0-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="630c0-258">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="630c0-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="630c0-259">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="630c0-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="630c0-260">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="630c0-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="630c0-261">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-262">**Versione**</span><span class="sxs-lookup"><span data-stu-id="630c0-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="630c0-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-265">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="630c0-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="630c0-266">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="630c0-266">Version of the physical element.</span></span>

<span data-ttu-id="630c0-267">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="630c0-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="630c0-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-269">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="630c0-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-271">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="630c0-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-272">Peso del pacchetto fisico, in sterline.</span><span class="sxs-lookup"><span data-stu-id="630c0-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="630c0-273">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="630c0-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630c0-274">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="630c0-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="630c0-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630c0-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630c0-276">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="630c0-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="630c0-277">Larghezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="630c0-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="630c0-278">Commenti</span><span class="sxs-lookup"><span data-stu-id="630c0-278">Remarks</span></span>

<span data-ttu-id="630c0-279">La classe **CIM \_ PhysicalPackage** è derivata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="630c0-280">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="630c0-280">WMI does not implement this class.</span></span> <span data-ttu-id="630c0-281">Per le classi WMI derivate da **CIM \_ PhysicalPackage**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="630c0-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="630c0-282">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="630c0-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="630c0-283">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="630c0-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="630c0-284">Requisiti</span><span class="sxs-lookup"><span data-stu-id="630c0-284">Requirements</span></span>



| <span data-ttu-id="630c0-285">Requisito</span><span class="sxs-lookup"><span data-stu-id="630c0-285">Requirement</span></span> | <span data-ttu-id="630c0-286">Valore</span><span class="sxs-lookup"><span data-stu-id="630c0-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="630c0-287">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="630c0-287">Minimum supported client</span></span><br/> | <span data-ttu-id="630c0-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="630c0-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="630c0-289">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="630c0-289">Minimum supported server</span></span><br/> | <span data-ttu-id="630c0-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="630c0-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="630c0-291">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="630c0-291">Namespace</span></span><br/>                | <span data-ttu-id="630c0-292">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="630c0-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="630c0-293">MOF</span><span class="sxs-lookup"><span data-stu-id="630c0-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="630c0-294"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="630c0-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="630c0-295">DLL</span><span class="sxs-lookup"><span data-stu-id="630c0-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630c0-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="630c0-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="630c0-297">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="630c0-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="630c0-298">**\_PhysicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="630c0-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

