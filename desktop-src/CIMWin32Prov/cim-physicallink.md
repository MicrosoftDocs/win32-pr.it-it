---
description: La \_ classe CIM PhysicalLink rappresenta il cablaggio di elementi fisici.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: Classe CIM_PhysicalLink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524010"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="20e9c-103">CIM \_ PhysicalLink (classe)</span><span class="sxs-lookup"><span data-stu-id="20e9c-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="20e9c-104">La classe **CIM \_ PhysicalLink** rappresenta il cablaggio di elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="20e9c-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="20e9c-105">Ad esempio, i cavi seriale o Ethernet e i collegamenti infrarossi sarebbero sottoclassi (se sono definite proprietà o associazioni aggiuntive) o istanze di **CIM \_ PhysicalLink**.</span><span class="sxs-lookup"><span data-stu-id="20e9c-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="20e9c-106">In genere, i numerosi cavi fisici in un pacchetto fisico o in una rete non sono modellati.</span><span class="sxs-lookup"><span data-stu-id="20e9c-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="20e9c-107">Tuttavia, quando i cavi o i collegamenti sono componenti critici o asset con tag della società, è possibile creare un'istanza degli oggetti utilizzando questa classe o una delle relative classi discendenti.</span><span class="sxs-lookup"><span data-stu-id="20e9c-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20e9c-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="20e9c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="20e9c-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="20e9c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="20e9c-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="20e9c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="20e9c-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="20e9c-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e9c-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20e9c-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="20e9c-113">Members</span><span class="sxs-lookup"><span data-stu-id="20e9c-113">Members</span></span>

<span data-ttu-id="20e9c-114">La classe **CIM \_ PhysicalLink** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="20e9c-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="20e9c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20e9c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20e9c-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20e9c-116">Properties</span></span>

<span data-ttu-id="20e9c-117">La classe **CIM \_ PhysicalLink** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="20e9c-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20e9c-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="20e9c-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="20e9c-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20e9c-122">Short textual description of the object.</span></span>

<span data-ttu-id="20e9c-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20e9c-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-127">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="20e9c-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-128">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="20e9c-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="20e9c-129">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="20e9c-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="20e9c-130">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="20e9c-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-134">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="20e9c-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20e9c-135">Textual description of the object.</span></span>

<span data-ttu-id="20e9c-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20e9c-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20e9c-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="20e9c-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-141">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20e9c-141">Date and time the object was installed.</span></span> <span data-ttu-id="20e9c-142">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="20e9c-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="20e9c-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-144">**Length**</span><span class="sxs-lookup"><span data-stu-id="20e9c-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-145">Tipo di dati: **real64**</span><span class="sxs-lookup"><span data-stu-id="20e9c-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-147">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("piedi")</span><span class="sxs-lookup"><span data-stu-id="20e9c-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-148">Lunghezza corrente del collegamento fisico, in metri.</span><span class="sxs-lookup"><span data-stu-id="20e9c-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="20e9c-149">Per alcune connessioni, soprattutto per le tecnologie wireless, questa proprietà potrebbe non essere applicabile e deve essere lasciata non inizializzata.</span><span class="sxs-lookup"><span data-stu-id="20e9c-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-150">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="20e9c-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-153">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="20e9c-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-154">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="20e9c-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="20e9c-155">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="20e9c-156">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="20e9c-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-158">Tipo di dati: **real64**</span><span class="sxs-lookup"><span data-stu-id="20e9c-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-160">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("piedi")</span><span class="sxs-lookup"><span data-stu-id="20e9c-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-161">Lunghezza massima del collegamento fisico in piedi.</span><span class="sxs-lookup"><span data-stu-id="20e9c-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-162">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="20e9c-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20e9c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-165">Tipo di supporti attraverso i quali passano i segnali di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="20e9c-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="20e9c-166">I supporti di rete comuni includono cavi bidirezionali, coassiali e a fibra ottica.</span><span class="sxs-lookup"><span data-stu-id="20e9c-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20e9c-167">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="20e9c-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20e9c-168">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="20e9c-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="20e9c-169">**CAT1** (2)</span><span class="sxs-lookup"><span data-stu-id="20e9c-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="20e9c-170">**CAT2** (3)</span><span class="sxs-lookup"><span data-stu-id="20e9c-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="20e9c-171">**Cat3** (4)</span><span class="sxs-lookup"><span data-stu-id="20e9c-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="20e9c-172">**Cat4** (5)</span><span class="sxs-lookup"><span data-stu-id="20e9c-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="20e9c-173">**CAT5** (6)</span><span class="sxs-lookup"><span data-stu-id="20e9c-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="20e9c-174">**50-ohm coassiale** (7)</span><span class="sxs-lookup"><span data-stu-id="20e9c-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="20e9c-175">**75-ohm coassiale** (8)</span><span class="sxs-lookup"><span data-stu-id="20e9c-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="20e9c-176">**100-ohm coassiale** (9)</span><span class="sxs-lookup"><span data-stu-id="20e9c-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="20e9c-177">**Fibra ottica** (10)</span><span class="sxs-lookup"><span data-stu-id="20e9c-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="20e9c-178">**UTP** (11)</span><span class="sxs-lookup"><span data-stu-id="20e9c-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="20e9c-179">**STP** (12)</span><span class="sxs-lookup"><span data-stu-id="20e9c-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="20e9c-180">**Cavo barra multifunzione** (13)</span><span class="sxs-lookup"><span data-stu-id="20e9c-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="20e9c-181">**Twinaxial** (14)</span><span class="sxs-lookup"><span data-stu-id="20e9c-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="20e9c-182">**9Um ottico** (15)</span><span class="sxs-lookup"><span data-stu-id="20e9c-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="20e9c-183">**50um ottico** (16)</span><span class="sxs-lookup"><span data-stu-id="20e9c-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="20e9c-184">**62,5 ottico um** (17)</span><span class="sxs-lookup"><span data-stu-id="20e9c-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20e9c-185">**Modello**</span><span class="sxs-lookup"><span data-stu-id="20e9c-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-188">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20e9c-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-189">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="20e9c-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="20e9c-190">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-191">**Nome**</span><span class="sxs-lookup"><span data-stu-id="20e9c-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-194">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="20e9c-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-195">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="20e9c-195">Label by which the object is known.</span></span> <span data-ttu-id="20e9c-196">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="20e9c-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="20e9c-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="20e9c-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-201">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="20e9c-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="20e9c-202">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="20e9c-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="20e9c-203">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="20e9c-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="20e9c-204">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-205">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="20e9c-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-208">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="20e9c-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-209">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="20e9c-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="20e9c-210">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-211">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="20e9c-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-212">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20e9c-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-214">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="20e9c-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="20e9c-215">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-216">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="20e9c-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-219">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20e9c-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-220">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="20e9c-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="20e9c-221">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-222">**SKU**</span><span class="sxs-lookup"><span data-stu-id="20e9c-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-225">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20e9c-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-226">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="20e9c-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="20e9c-227">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-228">**Status**</span><span class="sxs-lookup"><span data-stu-id="20e9c-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-231">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="20e9c-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-232">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20e9c-232">Current status of the object.</span></span>

<span data-ttu-id="20e9c-233">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="20e9c-234">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="20e9c-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="20e9c-235">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="20e9c-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="20e9c-236">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="20e9c-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20e9c-237">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="20e9c-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20e9c-238">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="20e9c-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="20e9c-239">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="20e9c-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="20e9c-240">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="20e9c-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="20e9c-241">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="20e9c-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="20e9c-242">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="20e9c-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="20e9c-243">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="20e9c-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="20e9c-244">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="20e9c-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="20e9c-245">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="20e9c-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="20e9c-246">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="20e9c-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20e9c-247">**Tag**</span><span class="sxs-lookup"><span data-stu-id="20e9c-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-250">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="20e9c-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-251">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="20e9c-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="20e9c-252">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="20e9c-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="20e9c-253">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="20e9c-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="20e9c-254">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="20e9c-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="20e9c-255">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="20e9c-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="20e9c-256">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="20e9c-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="20e9c-257">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-258">**Versione**</span><span class="sxs-lookup"><span data-stu-id="20e9c-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-259">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20e9c-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-261">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20e9c-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-262">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="20e9c-262">Version of the physical element.</span></span>

<span data-ttu-id="20e9c-263">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20e9c-264">**Cablate**</span><span class="sxs-lookup"><span data-stu-id="20e9c-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20e9c-265">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20e9c-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20e9c-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20e9c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20e9c-267">Se **true**, il collegamento fisico è un cavo.</span><span class="sxs-lookup"><span data-stu-id="20e9c-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="20e9c-268">In caso contrario, si tratta di una connessione wireless.</span><span class="sxs-lookup"><span data-stu-id="20e9c-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20e9c-269">Commenti</span><span class="sxs-lookup"><span data-stu-id="20e9c-269">Remarks</span></span>

<span data-ttu-id="20e9c-270">La classe **CIM \_ PhysicalLink** è derivata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="20e9c-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="20e9c-271">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="20e9c-271">WMI does not implement this class.</span></span>

<span data-ttu-id="20e9c-272">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="20e9c-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="20e9c-273">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="20e9c-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="20e9c-274">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20e9c-274">Requirements</span></span>



| <span data-ttu-id="20e9c-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="20e9c-275">Requirement</span></span> | <span data-ttu-id="20e9c-276">Valore</span><span class="sxs-lookup"><span data-stu-id="20e9c-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20e9c-277">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20e9c-277">Minimum supported client</span></span><br/> | <span data-ttu-id="20e9c-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20e9c-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20e9c-279">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20e9c-279">Minimum supported server</span></span><br/> | <span data-ttu-id="20e9c-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20e9c-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20e9c-281">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="20e9c-281">Namespace</span></span><br/>                | <span data-ttu-id="20e9c-282">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="20e9c-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20e9c-283">MOF</span><span class="sxs-lookup"><span data-stu-id="20e9c-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20e9c-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20e9c-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20e9c-285">DLL</span><span class="sxs-lookup"><span data-stu-id="20e9c-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20e9c-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20e9c-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20e9c-287">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20e9c-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e9c-288">**\_PhysicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="20e9c-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

