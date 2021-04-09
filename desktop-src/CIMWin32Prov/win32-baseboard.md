---
description: Rappresenta un battiscopa, noto anche come scheda madre o scheda di sistema.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Classe Win32_BaseBoard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049272"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="5ecca-103">\_Classe battiscopa Win32</span><span class="sxs-lookup"><span data-stu-id="5ecca-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="5ecca-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ battiscopa Win32** rappresenta una scheda di rete, nota anche come scheda madre o scheda di sistema.</span><span class="sxs-lookup"><span data-stu-id="5ecca-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="5ecca-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ecca-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecca-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ecca-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="5ecca-107">Members</span><span class="sxs-lookup"><span data-stu-id="5ecca-107">Members</span></span>

<span data-ttu-id="5ecca-108">La **classe \_ battiscopa Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ecca-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="5ecca-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5ecca-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5ecca-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ecca-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5ecca-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="5ecca-111">Methods</span></span>

<span data-ttu-id="5ecca-112">La **classe \_ battiscopa Win32** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5ecca-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="5ecca-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="5ecca-113">Method</span></span>           | <span data-ttu-id="5ecca-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ecca-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="5ecca-115">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="5ecca-115">**IsCompatible**</span></span> | <span data-ttu-id="5ecca-116">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="5ecca-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5ecca-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ecca-117">Properties</span></span>

<span data-ttu-id="5ecca-118">La **classe \_ battiscopa Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ecca-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ecca-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5ecca-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5ecca-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-123">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="5ecca-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="5ecca-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-125">**ConfigOptions**</span><span class="sxs-lookup"><span data-stu-id="5ecca-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-126">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5ecca-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 12 \| stringhe opzioni di configurazione")</span><span class="sxs-lookup"><span data-stu-id="5ecca-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-129">Matrice che rappresenta la configurazione dei saltatori e degli interruttori posizionati sulla scheda di battiscopa.</span><span class="sxs-lookup"><span data-stu-id="5ecca-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="5ecca-130">Esempio: "JP2:1-2 la dimensione della cache è 256K, 2-3 la dimensione della cache è 512K, SW1-1: Close to Disable on board video"</span><span class="sxs-lookup"><span data-stu-id="5ecca-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ecca-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-134">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5ecca-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-135">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="5ecca-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5ecca-136">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="5ecca-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="5ecca-137">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-138">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="5ecca-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-139">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5ecca-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-141">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="5ecca-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-142">Profondità del pacchetto fisico in pollici.</span><span class="sxs-lookup"><span data-stu-id="5ecca-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="5ecca-143">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-144">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5ecca-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-147">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5ecca-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-148">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ecca-148">Description of the object.</span></span>

<span data-ttu-id="5ecca-149">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-150">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="5ecca-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-151">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5ecca-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-153">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="5ecca-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-154">Altezza del pacchetto fisico in pollici.</span><span class="sxs-lookup"><span data-stu-id="5ecca-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="5ecca-155">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-156">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="5ecca-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-157">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-159">Se **true**, la scheda è una scheda madre o un battiscopa in uno chassis.</span><span class="sxs-lookup"><span data-stu-id="5ecca-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="5ecca-160">Questa proprietà viene ereditata [**dalla \_ scheda CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-161">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="5ecca-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-162">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-164">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5ecca-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="5ecca-165">Un pacchetto fisico può essere scambiato a caldo se è possibile sostituire l'elemento con un elemento fisicamente diverso ma equivalente mentre al pacchetto che lo contiene è applicata una potenza che è, mentre è acceso.</span><span class="sxs-lookup"><span data-stu-id="5ecca-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="5ecca-166">Ad esempio, un pacchetto di unità disco inserito usando i connettori SCA è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5ecca-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="5ecca-167">Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="5ecca-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="5ecca-168">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5ecca-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-170">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5ecca-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-172">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="5ecca-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-173">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ecca-173">Date and time the object was installed.</span></span> <span data-ttu-id="5ecca-174">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="5ecca-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5ecca-175">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-176">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="5ecca-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-179">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5ecca-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-180">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5ecca-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="5ecca-181">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-182">**Modello**</span><span class="sxs-lookup"><span data-stu-id="5ecca-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-185">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5ecca-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-186">Nome con cui l'elemento fisico è noto.</span><span class="sxs-lookup"><span data-stu-id="5ecca-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="5ecca-187">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-188">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5ecca-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-191">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5ecca-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-192">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5ecca-192">Label by which the object is known.</span></span> <span data-ttu-id="5ecca-193">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5ecca-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5ecca-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5ecca-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-198">Acquisisce dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5ecca-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5ecca-199">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="5ecca-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="5ecca-200">Si noti che se solo i dati del codice a barre sono disponibili e sono univoci oppure possono essere utilizzati come chiave dell'elemento, il valore della proprietà sarà **null** e i dati del codice a barre verranno utilizzati come chiave della classe nella proprietà Tag.</span><span class="sxs-lookup"><span data-stu-id="5ecca-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="5ecca-201">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-202">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="5ecca-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-205">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5ecca-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-206">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5ecca-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="5ecca-207">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-208">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="5ecca-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-209">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-211">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="5ecca-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="5ecca-212">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-213">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="5ecca-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-216">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 2 \| Product")</span><span class="sxs-lookup"><span data-stu-id="5ecca-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-217">Numero di parte della linea di base definito dal produttore.</span><span class="sxs-lookup"><span data-stu-id="5ecca-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-218">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="5ecca-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-221">Se **true**, un pacchetto è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="5ecca-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="5ecca-222">Un pacchetto fisico è rimovibile se è progettato per essere utilizzato e esterno al contenitore fisico in cui si trova normalmente senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5ecca-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="5ecca-223">Un pacchetto può comunque essere rimovibile se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="5ecca-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="5ecca-224">Se la potenza può essere ACCESa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5ecca-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="5ecca-225">Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando i connettori SCA.</span><span class="sxs-lookup"><span data-stu-id="5ecca-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="5ecca-226">Tuttavia, anche quest'ultimo può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="5ecca-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="5ecca-227">La visualizzazione di un computer portatile non è rimovibile, né è un alimentatore non ridondante.</span><span class="sxs-lookup"><span data-stu-id="5ecca-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="5ecca-228">La rimozione di questi componenti influirà sulla funzione della creazione complessiva dei pacchetti oppure non è possibile grazie alla stretta integrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ecca-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="5ecca-229">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-230">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="5ecca-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-233">Se **true**, un pacchetto è sostituibile.</span><span class="sxs-lookup"><span data-stu-id="5ecca-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="5ecca-234">Un pacchetto fisico è sostituibile se è possibile sostituire (FRU o upgrade) l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="5ecca-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="5ecca-235">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="5ecca-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="5ecca-236">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="5ecca-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="5ecca-237">Un altro esempio è un pacchetto di alimentazione montato sulle guide scorrevoli.</span><span class="sxs-lookup"><span data-stu-id="5ecca-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="5ecca-238">Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="5ecca-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="5ecca-239">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-240">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="5ecca-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-243">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Card**](cim-card.md).**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="5ecca-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-244">Stringa in formato libero che descrive il modo in cui questa scheda è fisicamente univoca rispetto ad altre schede.</span><span class="sxs-lookup"><span data-stu-id="5ecca-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="5ecca-245">La proprietà ha un significato solo quando la proprietà booleana corrispondente **SpecialRequirements** è impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="5ecca-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="5ecca-246">Questa proprietà viene ereditata [**dalla \_ scheda CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-247">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="5ecca-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-248">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-250">Se **true**, per il corretto funzionamento è necessario almeno un daughterboard o una scheda ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="5ecca-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="5ecca-251">Questa proprietà viene ereditata [**dalla \_ scheda CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-252">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5ecca-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-255">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5ecca-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-256">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5ecca-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5ecca-257">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-258">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5ecca-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-259">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-261">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5ecca-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-262">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="5ecca-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="5ecca-263">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-264">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="5ecca-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-265">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-267">Stringa in formato libero che descrive la posizione degli slot, l'utilizzo tipico, le restrizioni, la spaziatura dei singoli slot o qualsiasi altra informazione pertinente per gli slot in una scheda.</span><span class="sxs-lookup"><span data-stu-id="5ecca-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="5ecca-268">Questa proprietà viene ereditata [**dalla \_ scheda CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-269">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="5ecca-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-270">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ecca-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-272">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Card**](cim-card.md).**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="5ecca-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-273">Se **true**, questa scheda è fisicamente univoca rispetto ad altre schede dello stesso tipo e pertanto richiede uno slot speciale.</span><span class="sxs-lookup"><span data-stu-id="5ecca-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="5ecca-274">Una scheda a doppia larghezza, ad esempio, richiede due slot.</span><span class="sxs-lookup"><span data-stu-id="5ecca-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="5ecca-275">Un altro esempio è la posizione in cui una determinata scheda può essere usata per la stessa funzione generale di altre schede, ma richiede uno slot speciale (ad esempio, molto lungo), mentre le altre schede possono essere inserite in qualsiasi slot disponibile.</span><span class="sxs-lookup"><span data-stu-id="5ecca-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="5ecca-276">Se impostato su **true**, la proprietà corrispondente, **RequirementsDescription**, deve specificare la natura dell'unicità o lo scopo della scheda.</span><span class="sxs-lookup"><span data-stu-id="5ecca-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="5ecca-277">Questa proprietà viene ereditata [**dalla \_ scheda CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-278">**Status**</span><span class="sxs-lookup"><span data-stu-id="5ecca-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-281">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5ecca-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-282">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ecca-282">Current status of the object.</span></span> <span data-ttu-id="5ecca-283">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="5ecca-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5ecca-284">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="5ecca-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5ecca-285">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5ecca-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5ecca-286">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5ecca-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5ecca-287">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5ecca-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5ecca-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5ecca-289">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ecca-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5ecca-290">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5ecca-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5ecca-291">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="5ecca-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5ecca-292">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="5ecca-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ecca-293">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5ecca-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5ecca-294">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="5ecca-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5ecca-295">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="5ecca-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5ecca-296">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="5ecca-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5ecca-297">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="5ecca-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5ecca-298">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="5ecca-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5ecca-299">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="5ecca-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5ecca-300">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="5ecca-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5ecca-301">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="5ecca-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ecca-302">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5ecca-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-305">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="5ecca-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-306">Identificatore univoco del battiscopa del sistema.</span><span class="sxs-lookup"><span data-stu-id="5ecca-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="5ecca-307">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="5ecca-308">Esempio: "lavagna di base"</span><span class="sxs-lookup"><span data-stu-id="5ecca-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-309">**Versione**</span><span class="sxs-lookup"><span data-stu-id="5ecca-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecca-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-312">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5ecca-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-313">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="5ecca-313">Version of the physical element.</span></span>

<span data-ttu-id="5ecca-314">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-315">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5ecca-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-316">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5ecca-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-318">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="5ecca-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-319">Peso del pacchetto fisico in sterline.</span><span class="sxs-lookup"><span data-stu-id="5ecca-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="5ecca-320">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecca-321">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="5ecca-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecca-322">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="5ecca-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ecca-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecca-324">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="5ecca-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5ecca-325">Larghezza del pacchetto fisico in pollici.</span><span class="sxs-lookup"><span data-stu-id="5ecca-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="5ecca-326">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ecca-327">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ecca-327">Remarks</span></span>

<span data-ttu-id="5ecca-328">La **classe \_ battiscopa Win32** è derivata dalla [**\_ scheda CIM**](cim-card.md) che deriva da [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ecca-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5ecca-329">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ecca-329">Examples</span></span>

<span data-ttu-id="5ecca-330">L'esempio di elenco delle proprietà della scheda di [battiscopa del computer](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) viene restituito le informazioni sul battiscopa del computer.</span><span class="sxs-lookup"><span data-stu-id="5ecca-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="5ecca-331">L'esempio di [elenco delle proprietà](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) della scheda di stato del computer di PowerShell restituisce informazioni sul computer.</span><span class="sxs-lookup"><span data-stu-id="5ecca-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="5ecca-332">Nell'esempio VBScript riportato di seguito vengono inoltre restituite informazioni sulla scheda di stato del computer.</span><span class="sxs-lookup"><span data-stu-id="5ecca-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="5ecca-333">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ecca-333">Requirements</span></span>



| <span data-ttu-id="5ecca-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ecca-334">Requirement</span></span> | <span data-ttu-id="5ecca-335">Valore</span><span class="sxs-lookup"><span data-stu-id="5ecca-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecca-336">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ecca-336">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecca-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ecca-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ecca-338">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ecca-338">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecca-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ecca-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ecca-340">MOF</span><span class="sxs-lookup"><span data-stu-id="5ecca-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ecca-341"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ecca-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ecca-342">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecca-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecca-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecca-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ecca-344">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ecca-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecca-345">**\_Scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="5ecca-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="5ecca-346">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="5ecca-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

