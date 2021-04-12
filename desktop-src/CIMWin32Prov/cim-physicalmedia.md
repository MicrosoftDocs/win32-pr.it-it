---
description: La \_ classe CIM PhysicalMedia rappresenta i tipi di documentazione e supporti di archiviazione, ad esempio nastri, CD ROM e così via.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234524"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="97545-103">CIM \_ PhysicalMedia (classe)</span><span class="sxs-lookup"><span data-stu-id="97545-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="97545-104">La classe **CIM \_ PhysicalMedia** rappresenta i tipi di documentazione e supporti di archiviazione, ad esempio nastri, CD ROM e così via.</span><span class="sxs-lookup"><span data-stu-id="97545-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="97545-105">Questa classe viene in genere usata per individuare e gestire supporti rimovibili (rispetto ai supporti bloccati con il dispositivo di accesso multimediale come singolo pacchetto, ad esempio dischi rigidi).</span><span class="sxs-lookup"><span data-stu-id="97545-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="97545-106">I supporti sealed, tuttavia, possono essere modellati anche usando questa classe quando il supporto è associato al pacchetto fisico usando la relazione [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="97545-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97545-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="97545-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="97545-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="97545-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="97545-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="97545-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="97545-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="97545-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97545-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97545-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
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
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="97545-112">Members</span><span class="sxs-lookup"><span data-stu-id="97545-112">Members</span></span>

<span data-ttu-id="97545-113">La classe **CIM \_ PhysicalMedia** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="97545-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="97545-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97545-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97545-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97545-115">Properties</span></span>

<span data-ttu-id="97545-116">La classe **CIM \_ PhysicalMedia** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="97545-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97545-117">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="97545-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-118">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="97545-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="97545-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-120">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="97545-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="97545-121">Numero di byte che possono essere letti o scritti in un supporto.</span><span class="sxs-lookup"><span data-stu-id="97545-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="97545-122">Questa proprietà non è applicabile a una copia (documentazione) o a un supporto più pulito.</span><span class="sxs-lookup"><span data-stu-id="97545-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="97545-123">La compressione dei dati non deve essere presupposta, in quanto aumenterebbe il valore in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="97545-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="97545-124">Per i nastri, è preferibile che non vengano registrate tracce di file o spazi vuoti sul supporto.</span><span class="sxs-lookup"><span data-stu-id="97545-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="97545-125">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="97545-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="97545-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="97545-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="97545-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="97545-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="97545-130">Short textual description of the object.</span></span>

<span data-ttu-id="97545-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-132">**CleanerMedia**</span><span class="sxs-lookup"><span data-stu-id="97545-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="97545-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97545-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-135">Se **true**, il supporto fisico viene usato per scopi di pulizia e non per l'archiviazione di dati.</span><span class="sxs-lookup"><span data-stu-id="97545-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="97545-136">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="97545-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-139">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97545-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97545-140">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="97545-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="97545-141">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="97545-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="97545-142">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-143">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="97545-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-146">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="97545-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="97545-147">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="97545-147">Textual description of the object.</span></span>

<span data-ttu-id="97545-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="97545-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-150">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="97545-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97545-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-152">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="97545-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="97545-153">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="97545-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="97545-154">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="97545-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="97545-155">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="97545-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="97545-156">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="97545-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="97545-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-158">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="97545-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="97545-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-160">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="97545-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="97545-161">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="97545-161">Date and time the object was installed.</span></span> <span data-ttu-id="97545-162">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="97545-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="97545-163">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-164">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="97545-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-167">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97545-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97545-168">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="97545-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="97545-169">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="97545-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="97545-170">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="97545-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-174">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="97545-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="97545-175">Dettagli aggiuntivi relativi all'enumerazione **mediaType** .</span><span class="sxs-lookup"><span data-stu-id="97545-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="97545-176">Se, ad esempio, viene specificato il valore 3 ("QIC cartuccia"), questa proprietà indicherà se il nastro è in larghezza o 1/4 pollice, preformattato, compatibile con Travan e così via.</span><span class="sxs-lookup"><span data-stu-id="97545-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="97545-177">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="97545-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="97545-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="97545-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-180">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaDescription**")</span><span class="sxs-lookup"><span data-stu-id="97545-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="97545-181">Tipo di supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="97545-181">Type of physical media.</span></span> <span data-ttu-id="97545-182">La proprietà **MEDIADESCRIPTION** fornisce una definizione più esplicita del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="97545-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="97545-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="97545-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="97545-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="97545-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="97545-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Cartuccia nastro** (2)</span><span class="sxs-lookup"><span data-stu-id="97545-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="97545-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**Cartuccia QIC** (3)</span><span class="sxs-lookup"><span data-stu-id="97545-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="97545-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**Cartuccia AIT** (4)</span><span class="sxs-lookup"><span data-stu-id="97545-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="97545-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**Cartuccia DTF** (5)</span><span class="sxs-lookup"><span data-stu-id="97545-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="97545-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**Cartuccia dat** (6)</span><span class="sxs-lookup"><span data-stu-id="97545-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="97545-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**cartuccia nastro 8mm** (7)</span><span class="sxs-lookup"><span data-stu-id="97545-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="97545-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19 mm cartuccia nastro** (8)</span><span class="sxs-lookup"><span data-stu-id="97545-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="97545-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**Cartuccia DLT** (9)</span><span class="sxs-lookup"><span data-stu-id="97545-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="97545-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Cartuccia nastro magnetico da metà pollice** (10)</span><span class="sxs-lookup"><span data-stu-id="97545-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="97545-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Disco cartuccia** (11)</span><span class="sxs-lookup"><span data-stu-id="97545-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="97545-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Disco Jaz** (12)</span><span class="sxs-lookup"><span data-stu-id="97545-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="97545-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**Disco zip** (13)</span><span class="sxs-lookup"><span data-stu-id="97545-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="97545-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Disco SyQuest** (14)</span><span class="sxs-lookup"><span data-stu-id="97545-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="97545-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Disco rimovibile Winchester** (15)</span><span class="sxs-lookup"><span data-stu-id="97545-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="97545-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="97545-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="97545-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="97545-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="97545-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="97545-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="97545-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD registrabile** (19)</span><span class="sxs-lookup"><span data-stu-id="97545-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="97545-203"><span id="WORM"></span><span id="worm"></span>**Worm** (20)</span><span class="sxs-lookup"><span data-stu-id="97545-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="97545-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-ottico** (21)</span><span class="sxs-lookup"><span data-stu-id="97545-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="97545-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="97545-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="97545-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)</span><span class="sxs-lookup"><span data-stu-id="97545-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="97545-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="97545-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="97545-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="97545-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="97545-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-video** (26)</span><span class="sxs-lookup"><span data-stu-id="97545-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="97545-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="97545-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="97545-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/dischetto** (28)</span><span class="sxs-lookup"><span data-stu-id="97545-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="97545-212">Disco floppy</span><span class="sxs-lookup"><span data-stu-id="97545-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="97545-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Disco rigido** (29)</span><span class="sxs-lookup"><span data-stu-id="97545-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="97545-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Scheda memoria** (30)</span><span class="sxs-lookup"><span data-stu-id="97545-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="97545-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Copia disco rigido** (31)</span><span class="sxs-lookup"><span data-stu-id="97545-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="97545-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Disco clik** (32)</span><span class="sxs-lookup"><span data-stu-id="97545-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="97545-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="97545-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="97545-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="97545-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="97545-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="97545-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="97545-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD registrabile** (36)</span><span class="sxs-lookup"><span data-stu-id="97545-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="97545-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="97545-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="97545-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="97545-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="97545-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="97545-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="97545-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="97545-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="97545-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="97545-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="97545-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="97545-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="97545-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-ottico riscrivibile** (43)</span><span class="sxs-lookup"><span data-stu-id="97545-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="97545-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Scrittura magneto-ottico una volta** (44)</span><span class="sxs-lookup"><span data-stu-id="97545-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="97545-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical riscrivibile (LIMDOW)** (45)</span><span class="sxs-lookup"><span data-stu-id="97545-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="97545-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Modifica della fase scrittura una volta** (46)</span><span class="sxs-lookup"><span data-stu-id="97545-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="97545-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Modifica della fase riscrivibile** (47)</span><span class="sxs-lookup"><span data-stu-id="97545-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="97545-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Modifica della fase doppio riscrivibile** (48)</span><span class="sxs-lookup"><span data-stu-id="97545-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="97545-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Scrittura ablativo** (49)</span><span class="sxs-lookup"><span data-stu-id="97545-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="97545-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Registrazione Near Field** (50)</span><span class="sxs-lookup"><span data-stu-id="97545-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="97545-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQIC** (51)</span><span class="sxs-lookup"><span data-stu-id="97545-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="97545-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span><span class="sxs-lookup"><span data-stu-id="97545-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="97545-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**particella 8mm Metal** (53)</span><span class="sxs-lookup"><span data-stu-id="97545-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="97545-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**evaporazione metallo avanzata 8mm** (54)</span><span class="sxs-lookup"><span data-stu-id="97545-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="97545-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span><span class="sxs-lookup"><span data-stu-id="97545-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="97545-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span><span class="sxs-lookup"><span data-stu-id="97545-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="97545-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**Accelis LTO** (57)</span><span class="sxs-lookup"><span data-stu-id="97545-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="97545-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 track tape** (58)</span><span class="sxs-lookup"><span data-stu-id="97545-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="97545-243">9-tenere traccia del nastro</span><span class="sxs-lookup"><span data-stu-id="97545-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="97545-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 track tape** (59)</span><span class="sxs-lookup"><span data-stu-id="97545-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="97545-245">18-track tape</span><span class="sxs-lookup"><span data-stu-id="97545-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="97545-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 track tape** (60)</span><span class="sxs-lookup"><span data-stu-id="97545-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="97545-247">36-track tape</span><span class="sxs-lookup"><span data-stu-id="97545-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="97545-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span><span class="sxs-lookup"><span data-stu-id="97545-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="97545-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**MP Magstar** (62)</span><span class="sxs-lookup"><span data-stu-id="97545-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="97545-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**Nastro D2** (63)</span><span class="sxs-lookup"><span data-stu-id="97545-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="97545-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape-DST Small** (64)</span><span class="sxs-lookup"><span data-stu-id="97545-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="97545-252">Tape DST Small</span><span class="sxs-lookup"><span data-stu-id="97545-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="97545-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Nastro-DST medio** (65)</span><span class="sxs-lookup"><span data-stu-id="97545-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="97545-254">Media DST nastro</span><span class="sxs-lookup"><span data-stu-id="97545-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="97545-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape-DST grande** (66)</span><span class="sxs-lookup"><span data-stu-id="97545-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="97545-256">DST nastro grande</span><span class="sxs-lookup"><span data-stu-id="97545-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="97545-257">**Modello**</span><span class="sxs-lookup"><span data-stu-id="97545-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-260">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97545-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97545-261">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="97545-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="97545-262">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-263">**Nome**</span><span class="sxs-lookup"><span data-stu-id="97545-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-266">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="97545-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="97545-267">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="97545-267">Label by which the object is known.</span></span> <span data-ttu-id="97545-268">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="97545-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="97545-269">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="97545-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-273">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="97545-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="97545-274">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="97545-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="97545-275">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="97545-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="97545-276">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-277">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="97545-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-280">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97545-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97545-281">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="97545-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="97545-282">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-283">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="97545-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-284">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="97545-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97545-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-286">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="97545-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="97545-287">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-288">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="97545-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-289">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="97545-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97545-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-291">Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="97545-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="97545-292">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="97545-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="97545-293">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="97545-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="97545-294">Ad esempio, un chip del processore non aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="97545-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="97545-295">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="97545-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-296">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="97545-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-297">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="97545-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97545-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-299">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="97545-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="97545-300">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="97545-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="97545-301">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="97545-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="97545-302">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="97545-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="97545-303">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="97545-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-304">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="97545-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-307">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97545-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97545-308">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="97545-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="97545-309">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-310">**SKU**</span><span class="sxs-lookup"><span data-stu-id="97545-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-311">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-313">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97545-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97545-314">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="97545-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="97545-315">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-316">**Status**</span><span class="sxs-lookup"><span data-stu-id="97545-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-319">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="97545-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="97545-320">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="97545-320">Current status of the object.</span></span>

<span data-ttu-id="97545-321">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="97545-322">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="97545-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="97545-323">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="97545-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="97545-324">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="97545-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="97545-325">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="97545-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="97545-326">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="97545-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="97545-327">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="97545-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="97545-328">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="97545-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="97545-329">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="97545-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="97545-330">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="97545-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="97545-331">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="97545-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="97545-332">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="97545-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="97545-333">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="97545-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="97545-334">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="97545-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="97545-335">**Tag**</span><span class="sxs-lookup"><span data-stu-id="97545-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-338">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97545-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97545-339">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="97545-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="97545-340">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="97545-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="97545-341">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="97545-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="97545-342">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="97545-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="97545-343">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="97545-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="97545-344">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="97545-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="97545-345">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-346">**Versione**</span><span class="sxs-lookup"><span data-stu-id="97545-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="97545-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97545-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97545-349">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97545-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97545-350">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="97545-350">Version of the physical element.</span></span>

<span data-ttu-id="97545-351">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97545-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97545-352">**WriteProtectOn**</span><span class="sxs-lookup"><span data-stu-id="97545-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97545-353">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="97545-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97545-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="97545-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97545-355">Se **true**, il supporto è attualmente protetto da scrittura da un meccanismo fisico, ad esempio una scheda Proteggi su un disco floppy.</span><span class="sxs-lookup"><span data-stu-id="97545-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97545-356">Commenti</span><span class="sxs-lookup"><span data-stu-id="97545-356">Remarks</span></span>

<span data-ttu-id="97545-357">La classe **CIM \_ PhysicalMedia** è derivata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="97545-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="97545-358">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="97545-358">WMI does not implement this class.</span></span>

<span data-ttu-id="97545-359">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="97545-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="97545-360">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="97545-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97545-361">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97545-361">Requirements</span></span>



| <span data-ttu-id="97545-362">Requisito</span><span class="sxs-lookup"><span data-stu-id="97545-362">Requirement</span></span> | <span data-ttu-id="97545-363">Valore</span><span class="sxs-lookup"><span data-stu-id="97545-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97545-364">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97545-364">Minimum supported client</span></span><br/> | <span data-ttu-id="97545-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97545-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97545-366">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97545-366">Minimum supported server</span></span><br/> | <span data-ttu-id="97545-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97545-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97545-368">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97545-368">Namespace</span></span><br/>                | <span data-ttu-id="97545-369">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="97545-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97545-370">MOF</span><span class="sxs-lookup"><span data-stu-id="97545-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97545-371"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97545-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97545-372">DLL</span><span class="sxs-lookup"><span data-stu-id="97545-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97545-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97545-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97545-374">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97545-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97545-375">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="97545-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

