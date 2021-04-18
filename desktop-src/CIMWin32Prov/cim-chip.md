---
description: La \_ classe CIM chip rappresenta il tipo di hardware del circuito integrato, tra cui ASICS, processori, chip di memoria e così via.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: Classe CIM_Chip
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483549"
---
# <a name="cim_chip-class"></a><span data-ttu-id="f5e3a-103">\_Classe di chip CIM</span><span class="sxs-lookup"><span data-stu-id="f5e3a-103">CIM\_Chip class</span></span>

<span data-ttu-id="f5e3a-104">La classe **CIM \_ chip** rappresenta il tipo di hardware del circuito integrato, tra cui ASICS, processori, chip di memoria e così via.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5e3a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5e3a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5e3a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f5e3a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e3a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5e3a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="f5e3a-110">Members</span><span class="sxs-lookup"><span data-stu-id="f5e3a-110">Members</span></span>

<span data-ttu-id="f5e3a-111">La classe **CIM \_ chip** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f5e3a-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="f5e3a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5e3a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5e3a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5e3a-113">Properties</span></span>

<span data-ttu-id="f5e3a-114">La classe **CIM \_ chip** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5e3a-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-119">A short textual description of the object.</span></span>

<span data-ttu-id="f5e3a-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-124">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-125">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f5e3a-126">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f5e3a-127">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-131">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-132">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-132">A textual description of the object.</span></span>

<span data-ttu-id="f5e3a-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-134">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-137">Fattore di forma dell'implementazione per il chip.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="f5e3a-138">È possibile specificare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5e3a-139">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f5e3a-140">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="f5e3a-141">**SIP** (2)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="f5e3a-142">**DIP** (3)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="f5e3a-143">**Zip** (4)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="f5e3a-144">**SOJ** (5)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="f5e3a-145">**Proprietario** (6)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="f5e3a-146">**SIMM** (7)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="f5e3a-147">**DIMM** (8)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="f5e3a-148">**TSOP** (9)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="f5e3a-149">**PGA** (10)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="f5e3a-150">**Rimming** (11)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="f5e3a-151">**SODIMM** (12)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="f5e3a-152">**SRIMM** (13)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="f5e3a-153">**SMD** (14)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="f5e3a-154">**SSMP** (15)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="f5e3a-155">**QFP** (16)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="f5e3a-156">**TQFP** (17)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="f5e3a-157">**SOIC** (18)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="f5e3a-158">**LCC** (19)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="f5e3a-159">**PLCC** (20)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="f5e3a-160">**BGA** (21)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="f5e3a-161">**FPBGA** (22)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="f5e3a-162">**LGA** (23)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="f5e3a-163">**FB-DIMM** (24)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5e3a-164">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-165">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-167">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f5e3a-168">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f5e3a-169">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f5e3a-170">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f5e3a-171">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-173">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-175">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-176">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-176">Indicates when the object was installed.</span></span> <span data-ttu-id="f5e3a-177">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f5e3a-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-179">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-182">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-183">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="f5e3a-184">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f5e3a-185">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-186">**Modello**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-189">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-190">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f5e3a-191">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-192">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-195">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-196">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-196">Label by which the object is known.</span></span> <span data-ttu-id="f5e3a-197">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f5e3a-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-202">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="f5e3a-203">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="f5e3a-204">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="f5e3a-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="f5e3a-205">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-206">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-209">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-210">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="f5e3a-211">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-212">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-213">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-215">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="f5e3a-216">In caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="f5e3a-217">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-218">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-221">Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f5e3a-222">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="f5e3a-223">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f5e3a-224">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="f5e3a-225">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-226">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-227">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-229">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f5e3a-230">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f5e3a-231">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f5e3a-232">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f5e3a-233">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-234">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-237">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-238">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="f5e3a-239">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-240">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-243">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-244">Numero di unità di conservazione per questo elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="f5e3a-245">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-246">**Status**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-249">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-250">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="f5e3a-251">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f5e3a-252">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="f5e3a-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f5e3a-253">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f5e3a-254">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f5e3a-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f5e3a-255">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f5e3a-256">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f5e3a-257">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f5e3a-258">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5e3a-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f5e3a-259">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f5e3a-260">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f5e3a-261">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="f5e3a-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5e3a-262">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f5e3a-263">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f5e3a-264">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f5e3a-265">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f5e3a-266">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f5e3a-267">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f5e3a-268">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f5e3a-269">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f5e3a-270">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="f5e3a-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5e3a-271">**Tag**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-274">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-275">Identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f5e3a-276">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f5e3a-277">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f5e3a-278">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f5e3a-279">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f5e3a-280">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f5e3a-281">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e3a-282">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5e3a-283">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5e3a-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5e3a-285">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f5e3a-286">Indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="f5e3a-287">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5e3a-288">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5e3a-288">Remarks</span></span>

<span data-ttu-id="f5e3a-289">La classe **CIM \_ chip** è derivata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="f5e3a-290">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-290">WMI does not implement this class.</span></span> <span data-ttu-id="f5e3a-291">Per ulteriori informazioni sulle classi derivate dal **\_ chip CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5e3a-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f5e3a-292">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5e3a-293">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e3a-294">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5e3a-294">Requirements</span></span>



| <span data-ttu-id="f5e3a-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e3a-295">Requirement</span></span> | <span data-ttu-id="f5e3a-296">Valore</span><span class="sxs-lookup"><span data-stu-id="f5e3a-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e3a-297">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5e3a-297">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e3a-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5e3a-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5e3a-299">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5e3a-299">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e3a-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5e3a-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5e3a-301">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5e3a-301">Namespace</span></span><br/>                | <span data-ttu-id="f5e3a-302">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f5e3a-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5e3a-303">MOF</span><span class="sxs-lookup"><span data-stu-id="f5e3a-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5e3a-304"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5e3a-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5e3a-305">DLL</span><span class="sxs-lookup"><span data-stu-id="f5e3a-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5e3a-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5e3a-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5e3a-307">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5e3a-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e3a-308">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f5e3a-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

